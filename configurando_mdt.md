## Configurando o MDT

Link com o tutorial usado como base para este procedimento: https://www.youtube.com/watch?v=bEqxm6H8apw&list=PLrpD46tdAA00AtkOX3SQ3gw4JWaZ72xLq

### Requisitos
- Um servidor Windows funcional, geralmente rodando o Windows Server, e configurado corretamente.
- dfd
- Baixar o MDT. Link: https://www.microsoft.com/en-us/download/details.aspx?id=54259
- Ao rodar o Deployment Workbench ele vai solicitar a instalação do Windows ADK
- Instalar o Windows ADK. Link: https://learn.microsoft.com/pt-br/windows-hardware/get-started/adk-install
- DICA: quando for usar na produção use a segunda opção: baixar todo o pacote e depois faz a instalação.

- Cria o primeiro Deployment Share, provavelmente vai dar um erro por falta do componente Windows PE.
- Faça o download : link https://learn.microsoft.com/pt-br/windows-hardware/manufacture/desktop/winpe-intro?view=windows-11

### Passos

#### 1. Scritp de Instalação

 Instalar silenciosamente

```bash
7-zip.exe /S
Firefox.exe /S
vlc.exe /S

```

#### 2. Instalar o windows 11
Para

```bash
sudo apt install realmd sssd sssd-tools libnss-sss libpam-sss adcli samba-common-bin krb5-user chrony
```
