# Alterar Status do SELinux (Permissivo/Enforcing)

<p align="center">
<img alt="Imagem de CriptoApp" width="300px" src="https://imgur.com/H0Fekh6.png">
</p>

Este repositório contém um script de shell simples e interativo para alterar o status do SELinux em dispositivos Android entre os modos `Permissive` e `Enforcing` diretamente pelo Termux.

## 📝 Sobre

O SELinux (Security-Enhanced Linux) é um módulo de segurança no kernel do Linux que fornece mecanismos de suporte a políticas de segurança de controle de acesso. Em alguns cenários, como ao usar certas modificações ou aplicativos que requerem permissões elevadas, pode ser necessário alterar seu modo de `Enforcing` (padrão, mais seguro) para `Permissive`. Este script facilita essa troca de forma rápida e segura.

## ✨ Funcionalidades

* **Menu Interativo:** Interface de linha de comando fácil de usar.
* **Alterar para Permissivo:** Muda o status do SELinux para `Permissive` (`setenforce 0`).
* **Alterar para Enforcing:** Restaura o status do SELinux para `Enforcing` (`setenforce 1`).
* **Verificar Status:** Mostra o modo atual do SELinux.
* **Verificação de Root:** Garante que o script seja executado com privilégios de superusuário.

## ⚠️ Aviso

Alterar o status do SELinux para `Permissive` pode reduzir a segurança do seu dispositivo. Use este script por sua conta e risco e apenas se souber o que está fazendo. Recomenda-se manter o SELinux no modo `Enforcing` para uso diário.

## 🚀 Pré-requisitos

* Android com acesso **root**.
* [Termux](https://f-droid.org/en/packages/com.termux/) instalado.
* `git` instalado no Termux (`pkg install git`).

## ⚙️ Instalação

1.  Abra o Termux e conceda acesso ao armazenamento:
    ```sh
    termux-setup-storage
    ```

2.  Clone este repositório:
    ```sh
    git clone [https://github.com/RaphaelStinson/change-kernel-between-permissive-and-enforcing](https://github.com/RaphaelStinson/change-kernel-between-permissive-and-enforcing)
    ```

3.  Navegue até o diretório do projeto:
    ```sh
    cd change-kernel-between-permissive-and-enforcing
    ```

4.  Conceda permissão de execução ao script:
    ```sh
    chmod +x selinux_menu.sh
    ```

## ▶️ Como Usar

1.  Dentro do diretório do projeto no Termux, execute o script com privilégios de superusuário:
    ```sh
    su -c ./selinux_menu.sh
    ```

2.  O menu a seguir será exibido. Digite o número da opção desejada e pressione Enter.
    ```
    Escolha uma opção:
    1) Alterar para permissivo
    2) Alterar para enforcing
    3) Checar status
    4) Sair
    Digite sua escolha [1-4]:
    ```

## 🧪 Testado em

* Kernel Extreme

Sinta-se à vontade para abrir uma *issue* se testar em outros kernels com sucesso.

## 👨‍💻 Créditos

Criado e mantido por [RaphaelStinson](https://github.com/RaphaelStinson).
