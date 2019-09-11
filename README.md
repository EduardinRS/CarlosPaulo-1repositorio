# CarlosPaulo-1repositorio
enable
configure terminal
hostname RT-00
banner motd "ACESSO APENAS PARA O DEPARTAMENTO DE TI"
enable secret SenhaEnable
line console 0
password SenhadaConsole
login
exit
line vty 0 15
password SenhadaVTY
login
exit
service password-encryption
interface gigabitEthernet 0/0
ip address 192.168.0.1 255.255.255.0
description REDE 192.168.0.0/24
no shutdown
exit
interface gigabitEthernet 0/1
ip address 172.16.0.1 255.255.0.0
description REDE 172.16.0.0/16
no shutdown
do wr



enable
configure terminal
interface gigabitEthernet 0/2
ip address 10.0.0.1 255.255.192.0
description REDE 10.0.0.0/18
no shutdown
do wr
