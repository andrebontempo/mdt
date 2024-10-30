## Configurando o MDT

Link com o tutorial usado como base para este procedimento: https://www.youtube.com/watch?v=bEqxm6H8apw&list=PLrpD46tdAA00AtkOX3SQ3gw4JWaZ72xLq

Ingressar um computador com **Ubuntu Linux** no **Active Directory** (AD) é um processo que permite que o sistema Linux participe da mesma rede gerenciada centralmente pelo AD, permitindo que os usuários façam login com suas credenciais do AD. O Active Directory é amplamente utilizado em ambientes empresariais, e a integração de sistemas Linux pode ser útil para garantir uma administração centralizada.

A seguir está um guia passo a passo para ingressar um Ubuntu Linux no Active Directory, utilizando ferramentas como o **Realmd**, **SSSD** (System Security Services Daemon) e o **Winbind**.

### Requisitos
- Um servidor Windows funcional, geralmente rodando o Windows Server, e configurado corretamente.
- dfd
- Baixar o MDT. Link: https://www.microsoft.com/en-us/download/details.aspx?id=54259

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
