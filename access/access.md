
<details>
  <summary> ZTE ko-romankiv-sondol-f-zt5s1>  </summary>

| Command                                       |               | Notes     |      |
| :--------                                     | :--------     | :-------- | :--- |
| enable
|                              | Стан інтерфейсів   ||
| show port ||  + оптичні показники||
|                              | МАС-адреси         ||
| show mac dynamic port 1/2                         || Перегляд МАС-адреси по порту ||
| show mac dynamic vlan 602                         || Перегляд МАС-адреси по vlan  ||
|                              | логи               ||
| show terminal log 

</details>
---


ZTE 
ko-romankiv-sondol-f-zt5s1>show port ½ 
Примітка. Також отримуємо оптичні показники. 
Перегляд МАС-адрес. 
ko-romankiv-sondol-f-zt5s1>show mac dynamic port 1/2 
ko-romankiv-sondol-f-zt5s1>show mac dynamic vlan 602 
Перегляд логів. 
ko-romankiv-sondol-f-zt5s1>show terminal log 

 

PON ZTE 
Перегляд портів. 
rv-mickevycha2-ats26-pon-zt7s1#show pon onu information gpon_olt-1/1/15 
rv-mickevycha2-ats26-pon-zt7s1#show pon onu information gpon_olt-1/3/3 
	Примітка. 1/1 або 1/3 прописуємо та 15 або 3 підставляємо згідно інформації в АРМ УС. 
		Якщо в графі State working – порт піднятий, Los – впав по фізиці, DyingGasp – «Доживає останнє», працює, але йому погано. 
Якщо необхідно переглянути МАС-адресу на порті. (переглядаємо на всіх портах) 
rv-mickevycha2-ats26-pon-zt7s1# show mac dynamic 
Перегляд маків по влану
show mac vlan xxx
Перегляд логів. 
rv-mickevycha2-ats26-pon-zt7s1#show logging alarm 
Перегляд аптайм обладнання
Show software 

PON RAISECOM – в назві обладнання є -pon- 
Необхідно зайти в режим Enable. 
cg-olysh-cherngv29-pon-rc5s1>enable 
Перегляд інформації по всім портам 
cg-olysh-cherngv29-pon-rc5s1#show interface gpon-onu online-information 
hr-zolochiv-centr27a-pon-rc5s1#show gpon-onu 1/1/4 uni eth info 
Перегляд МАС-адреси на порті 
cg-olysh-cherngv29-pon-rc5s1#show mac-address-table l2-address interface gpon-onu 1/1/10 
cg-olysh-cherngv29-pon-rc5s1#show mac-address-table l2-address vlan 602 
Перегляд логів 
cg-olysh-cherngv29-pon-rc5s1#show logging history | include x/x/x 
Перегляд оптичних показників 
cg-olysh-cherngv29-pon-rc5s1#show transceiver [ddm gigaEthernte 1/1/0] 
show interface gpon-olt transceiver rx-onu-power  
show gpon-onu 1/2/113 transceiver 

Iskratel (mban - SI2000)
Отримання інформації про порт. 
mBAN> show dsl port 18 
Примітка. Піднятий чи лежить порт Operational State (Up/Down). 
Перегляд МАС-адрес на порті. 
mBAN> show bridge mactable interface dsl5:1_33 
mBAN> show bridge mactable interface dsl5:1_40 
Примітка. Додати коли 1_33 або 1_40 для DHCP та PPPoE (вказується в АРМУС). Може бути лише в одному з них, в разі відсутності в обох командах – МАС-адреса відсутня. 
Переглянути логи на обладнанні. 
mBAN> show alarm 


Iskratel (SI3000)
Перегляд інформації по інтерфейсу
show port all
show port 0/12/1
Перегляд статистики по порту
show interface 0/12/1
Перегляд мак адреси по влану
show mac-addr-table vlan 604
Перегляд мак адреси по порту
show mac-addr-table interface 0/12/1
Перегляд логів 
dc-svyatogirsk-maz54-pon-ik1s1#show logging file MsgErr 

PON ISkratel 
rv-zdolbun-grush15-pon-ik1s2#show port all 
Якщо нам потрібно перевірити х/y/z, то спочатку перевіряємо x/y аби були в Up. Якщо Down – нема сенсу далі перевіряти. 
rv-zdolbun-grush15-pon-ik1s2#show port 0/6/2 
Переглядаємо МАС-адрес на порту. 
rv-zdolbun-grush15-pon-ik1s2#show mac-addr-table interface 0/6/35 
Переглядаємо інформацію по пристрою(час роботи). 
rv-zdolbun-grush15-pon-ik1s2#show sysinfo 
Перегляд логів
dc-svyatogirsk-maz54-pon-ik1s1#show logging file MsgErr 


---
<details>
  <summary> HW-56 - доступ </summary>

| Command                                       |               | Notes     |      |
| :--------                                     | :--------     | :-------- | :--- |
|||||
| display board 0/16 | | Переглянути стан інтерфейсу             |       
||перегляд МАС-адреси|||
|enable||||
|display mac-address port 0/11/1||||
|mac-address port 0/11/1 ont 11 || Відібрати по ONT ||
|display mac-address vlan 602 || Відібрати по vlan ||
||Перегляд логів|||
|display alarm history all |
|display alarm active all||||
	
</details>

--- 
<details>
  <summary>  FTTB RAISECOM – в назві обладнання є -f-  ck-zvenygor-shevch28-f-rc2s1 </summary>

| Command                                       |               | Notes     |      |
| :--------                                     | :--------     | :-------- | :--- |
|show interface brief ||Перегляд інформації по всіх портах. ||
||Перегляд МАС-адреси
|show mac-address dynamic gigaethernet 1/1/23  ||Перегляд МАС-адреси по порту ||
|show mac-address dynamic vlan 602             ||Перегляд МАС-адреси по vlan  ||
||Перегляд логів ||
|show logging history 
|show logging buffer 
|show logging buffer \| include 1/1/23 
|show alarm log \| include 1/18 
||Перегляд оптичних показників порту ||
| show transceiver ddm gigaethernet 1/1/28 
| show transceiver ddm alarm history ||Перегляд історії помилок оптичних показників ||

</details>

--- 
<details>
  <summary>  D-LINK mk-pervomaj-d3s1 </summary>

| Command                                       |               | Notes     |      |
| :--------                                     | :--------     | :-------- | :--- |
|                              | Стан інтерфейсів   ||
| show ports || 1000/full/none LinkDown ||
|                              | МАС-адреси         ||
| show fdb  port 2                ||Перегляд МАС-адреси по порту ||
| show fdb vlanid 604             ||Перегляд МАС-адреси по vlan  ||
|                              | логи               ||
| show log 
| show logging buffer 
| show logging buffer \| include 1/1/23 
| show alarm log \| include 1/18 
|                              | оптичні показникі  ||
| show ddm ports status 

</details>

--- 
<details>
  <summary>  BDCOM  zt-krasnobirka-druzhby1-bd1s1 </summary>

| Command                                       |               | Notes     |      |
| :--------                                     | :--------     | :-------- | :--- |
| enable
|                              | Стан інтерфейсів   ||
| show interface brief ||  ||
| show interface ePON 0/4:42
|                              | МАС-адреси         ||
| show mac address-table interface epoN 0/2:32        ||Перегляд МАС-адреси по порту ||
| show mac address-table vlan 604                     ||Перегляд МАС-адреси по vlan  ||
|                              | логи               ||
| show log 
| show logging
| show logging \| include EPON0/1:5
|                              | оптичні показникі  ||
|  

</details>
