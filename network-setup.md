router gigabitethernet 0/0/0 168.90.0.1
gigabitethernet 0/0/1 210.3.14.1

switch 1
pc 2 168.90.0.11
server 1 168.90.0.12
server 2 168.90.0.14
pc 3 168.90.0.15


switch 2
pc 0 210.3.14.11
pc 1 210.3.14.12
laptop 0 210.3.14.14
server 0 210.3.14.13
pc 4 210.3.14.15


ip addresses assigned to hosts:
pc 2 168.90.0.11
server 1 168.90.0.12
server 2 168.90.0.14
pc 0 210.3.14.11
pc 1 210.3.14.12
laptop 0 210.3.14.14
server 0 210.3.14.13



I first used the command: ip dhcp excluded-adress 168.90.0.1 168.90.0.10 on one 
second step i created a dhcp pool: ip dhcp pool FIRST_POOL network 169.90.0.0 default-router 168.90.0.1  i did the same for the second but with different addresses
third step i actiavted dhcp: interface gigabitethernet0/0/0 ip address 168.90.0.1 255.255.0.0 no shutdown 
and after everything i just saved the configuation
This was just a small explination on how i did this task.