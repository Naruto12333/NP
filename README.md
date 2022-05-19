# NP
NP Manual
Exp 5: Configure the telnet protocol using cisco packet tracer
Router------>CLI
(config-if)#exit
(config)#enable password 1234
        #line vty 0 4
        password cse-----exit
ping ip(router)--->telnet(router ip addr)
passwrod cse
#########################################################
Exp 2: Configuration of Switch using cisco packet tracer 
enable 
conf t
erase sartup-config
switch#reload
switch#show flash
switch#show version
switch#show clock
switch(config)#clock_set_15:08:00 aug 16 2011
switch(config)#banner mod#
switch(config)#hostname S1
########################################################
Exp 3: Configure the privilege level password and user authentication in switch.
1. To set the host name
Switch(config)# hostname CISCO
2. To set console password
CISCO(config)#
CISCO(config)#line console 0
CISCO(config-line)#password cisco123
CISCO(config-line)#login
CISCO(config-line)#exit
CISCO(config)#exit
CISCO#exit
Check the Console Password
II How to Set Privilege level password
1)Set a privilege password
!!! Clear Text Password not encrypted(less priority)
CISCO(config)# enable password muscat
!!! Encrypted password (more Priority)
CISCO(config)# enable secret nizwa
2) Verify the privilege Password
CISCO(config)# exit
CISCO# exit
CISCO con0 is now available
Press RETURN to get started.
User Access Verification
!!! TYPE HERE LINE CONSOLE Password
Password:
CISCO>enable
!!! TYPE HERE Privilege Level Password
Password:
III How to Set User Authentication in Switch
1)Set user authentication
CISCO# conf t
CISCO(config)# line console 0
CISCO(config-line)# login local
CISCO(config-line)# exit
CISCO(config)#username network password pwd
2) Verify the Authentication
CISCO(config)# exit
CISCO# exit
User Access Verification
Username: network
Password:
CISCO> enable
Password:

#########################################################
Exp-8 Configuration of Static Nat
Commmands
Step 4:To set up Static NAT:
Router# sh ip nat translation
Router# config t
Router(config)#ip nat inside source static 10.0.0.2 192.168.1.3
Provide interface for NAT cable
Router(config)# int fa0/0
Router(config-if)# ip nat inside
exit
Router(config)# int serial2/0
Router(config-if)# ip nat outside
exit
exit
Router#sh ip nat translation
Step 5 :To Check Connectivity between two network
Click on any PC>click on desktop>select command prompt and then type below commands
PC>ping 192.168.2.1
###########################################################
Exp 9: Configure the Dynamic NAT using cisco packet tracer.
Step 4:To set up Dynamic NAT:
router(config)#access-list 1 permit 10.0.0.2 0.0.0.0
router(config)#access-list 1 permit 10.0.0.3 0.0.0.0
router(config)#ip nat pool nslab 192.168.2.3 192.168.2.4 netmask 255.255.255.0
router(config)#ip nat inside source list 1 pool nslab
router(config)#int fa0/0
router(config-if)#ip nat inside
router(config-if)#exit
router(config)#int serial2/0
router(config-if)ip nat outside
router#sh ip nat translation
Step 5 :To Check Connectivity between two network
Click on any PC>click on desktop>select command prompt and then type below commands
PC>ping 192.168.2.1
Pinging 192.168.2.1 with 32 bytes of data:
Reply from 192.168.2.1: bytes=32 time=147ms TTL=254
