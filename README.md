# vlan
Домашнее задание

Строим бонды и вланы
в Office1 в тестовой подсети появляется сервера с доп интерфесами и адресами
в internal сети testLAN
- testClient1 - 10.10.10.254
- testClient2 - 10.10.10.254
- testServer1- 10.10.10.1
- testServer2- 10.10.10.1

равести вланами
testClient1 <-> testServer1
testClient2 <-> testServer2

между centralRouter и inetRouter
"пробросить" 2 линка (общая inernal сеть) и объединить их в бонд
проверить работу c отключением интерфейсов

____

Между centralRouter и inetRouter созданы 2 линка и объединины с помощью **team-интерфейса** `team0` в режиме loadbalance

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/1.png)

Отключаем линк

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/2.png)

Проверим изоляцию testClient1 и testServer1 в vlan100

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/3.png)

Изоляция testClient2 и testServer2 в vlan101

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/4.png)

Проверим доступность сети

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/5.png)

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/6.png)

Созданы два netns

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/7.png)

Так же созданы vlan100 и vlan101 на VRF100 и VRF101

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/8.png)

Трансляция сети 10.10.10.0/24 в сеть 10.10.100(101)

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/9.png)

И доступ для тест хостов интернет

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/10.png)

![Image alt](https://github.com/Sergey-SSA/vlan/blob/master/printscreen/11.png)
