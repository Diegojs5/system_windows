# system_windows
Target Microsoft windows

# Requisitos mínimos para automoção do Windows 

Versões para desktops do Windows 7,8.1 e 10
Versoes para servidores do windows server 2008, 2008 R2, 2012, 2012 R2 e 2016
Powershell 3.0
.NET 4.0
WinRM ativo
O Ansible usa o pacote pywinrm para se comunicar com os servidores Windows pelo WinRM. Não é instalado por padrão com o pacote Ansible, mas pode ser instalado executando o seguinte:
pip install "pywinrm>=0.3.0"

# WinRM
