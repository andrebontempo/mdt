## Configurando o MDT

Link para ajudar o entendimento: https://www.server-world.info/en/note?os=Ubuntu_24.04&p=realmd

Ingressar um computador com **Ubuntu Linux** no **Active Directory** (AD) é um processo que permite que o sistema Linux participe da mesma rede gerenciada centralmente pelo AD, permitindo que os usuários façam login com suas credenciais do AD. O Active Directory é amplamente utilizado em ambientes empresariais, e a integração de sistemas Linux pode ser útil para garantir uma administração centralizada.

A seguir está um guia passo a passo para ingressar um Ubuntu Linux no Active Directory, utilizando ferramentas como o **Realmd**, **SSSD** (System Security Services Daemon) e o **Winbind**.

### Requisitos
- Um servidor Active Directory funcional, geralmente rodando o Windows Server, e configurado corretamente.
- Credenciais de administrador de domínio ou de uma conta que tenha permissão para adicionar computadores ao domínio.
- Um servidor DNS configurado corretamente, permitindo que o Ubuntu resolva o domínio AD.

### Passos

#### 1. Atualizar o sistema
Primeiro, você precisa garantir que o seu sistema esteja atualizado. Execute os seguintes comandos para atualizar os pacotes do Ubuntu:

```bash
sudo apt update
sudo apt upgrade
```

#### 2. Instalar os pacotes necessários
Para ingressar no domínio Active Directory, instale o **Realmd**, o **SSSD**, o **Kerberos**, o **Winbind**, o **Samba** e algumas dependências adicionais que facilitarão o processo.

```bash
sudo apt install realmd sssd sssd-tools libnss-sss libpam-sss adcli samba-common-bin krb5-user chrony
```
