# ПРЗ 5. Threat Hunting
Чадов Виктор Тимофеевич ББМО-01-22

## 1. Развернем 2 виртуальные машины (сервер и клиент)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/06a81c3c-041a-4435-817d-a7c9f3f29e58)

## 2. Обеспечим между ними сетевой обмен

Server 192.168.23.152

Client 192.168.23.153

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/c74c59e5-19a7-4efb-9120-64766608cf78)


## 3. Развернем на сервере Wazuh и подключим клиента

Проверим подключение 

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/2f4e48e6-ae6a-4611-9bb2-152c4815b405)

## 4. Установим и запустим Snort на клиенте

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/60fe4269-447d-4ba3-8f2a-fb7e280e6c56)

## 5. Включим отправку Snortом сообщений в syslog

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/416e0468-cc9b-46dc-a271-e73651751f10)

## 6. Добавим пользовательские правила в Snort

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/4e3335b6-81fc-48fc-aef8-c962a62ea694)

## 7. Добавим Snort клиента в Wazuh

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/f6ab592e-cffb-4a21-bf1a-a104b120d09c)

## 8. Проверим появление IDS событий в Wazuh

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/0461eb7d-d14f-4321-a72f-07155068fbe0)


