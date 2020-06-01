# system_windows
Target Microsoft windows para Ansible

# Requisitos mínimos para automoção do Windows 

Versões para desktops do Windows 7,8.1 e 10
Versoes para servidores do windows server 2008, 2008 R2, 2012, 2012 R2 e 2016
Powershell 3.0
.NET 4.0
WinRM ativo
O Ansible usa o pacote pywinrm para se comunicar com os servidores Windows pelo WinRM. Não é instalado por padrão com o pacote Ansible, mas pode ser instalado executando o seguinte:
pip install "pywinrm>=0.3.0"

# WinRM

O WinRM é um protocolo de gerenciamento usado pelo Windows para se comunicar remotamente com outro servidor. É um protocolo baseado em SOAP que se comunica por HTTP / HTTPS e está incluído em todos os sistemas operacionais Windows recentes. Desde o Windows Server 2012, o WinRM foi ativado por padrão, mas na maioria dos casos é necessária uma configuração extra para usar o WinRM com Ansible.
Executar o powershell com privilegio de adminsitrador executar o comando  "WinRM quickconfig" , este comando valida se o serviço esta em execução.
Executar o comando "Set-ExecutionPolicy Unrestricted" executa qualquer script não assinado. ( Com grandes poderes vem grandes responsabilitades) 

Executar o script  ConfigureRemotingForAnsible.ps1, basicamente vai executar as configuraçoes necessarias para o winrm
Link: https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1
Executar o comando "winrm enumerate winrm/config/Listener" Transport = HTTP
    Port = 5985 e Transport = HTTPS Port = 5986

#link

Link: https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-7
Link: https://docs.microsoft.com/en-us/windows/win32/winrm/installation-and-configuration-for-windows-remote-management
Link: https://chocolatey.org/
