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
