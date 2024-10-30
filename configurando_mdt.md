## Configurando o MDT

Link com o tutorial usado como base para este procedimento: https://www.youtube.com/watch?v=bEqxm6H8apw&list=PLrpD46tdAA00AtkOX3SQ3gw4JWaZ72xLq

### Requisitos
- Um servidor Windows funcional, geralmente rodando o Windows Server, e configurado corretamente.
- dfd
- Baixar o MDT. Link: https://www.microsoft.com/en-us/download/details.aspx?id=54259
- Ao rodar o Deployment Workbench ele vai solicitar a instalação do Windows ADK
- Instalar o Windows ADK. Link: https://learn.microsoft.com/pt-br/windows-hardware/get-started/adk-install

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
