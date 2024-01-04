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

## 6. Скачаем и добавим пользовательские правила в Snort

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/b082cb70-7343-4ba3-83cc-657120dbd813)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/4e3335b6-81fc-48fc-aef8-c962a62ea694)

## 7. Добавим Snort клиента в Wazuh

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/f6ab592e-cffb-4a21-bf1a-a104b120d09c)

## 8. Проверим появление IDS событий в Wazuh

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/dd8e1e3e-b3ab-46c3-9369-3de17a20985d)

## 9. Установим Yara на client

sudo apt update
sudo apt install -y make gcc autoconf libtool libssl-dev pkg-config
sudo curl -LO https://github.com/VirusTotal/yara/archive/v4.2.3.tar.gz
sudo tar -xvzf v4.2.3.tar.gz -C /usr/local/bin/ && rm -f v4.2.3.tar.gz
cd /usr/local/bin/yara-4.2.3/
sudo ./bootstrap.sh && sudo ./configure && sudo make && sudo make install && sudo make check

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/cdcf5da5-7e55-440f-b3de-17662626addb)

Правила YARA

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/b082cb70-7343-4ba3-83cc-657120dbd813)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/d4b04a9f-723d-470f-b3a2-3f0f59303786)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/c97d04bb-67e2-488f-b52b-4d52d746cfe0)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/f555059e-ed64-4072-a049-9e238eb73560)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/1f4ddd69-32af-449a-9f05-772582119453)

## 10. Подключим Yara к Wazuh

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/5c446086-eade-4bd2-9a50-1421fd57cf8d)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/6f80a73a-beac-494e-8b90-0175d39eb72f)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/150c3399-752a-4e14-8191-650f0c4bb477)

## 10. Проверим работу Yara

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/620260a9-5554-4031-b429-d58a4343cb5a)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/f1eb52ab-82d4-40bd-ac82-dc3e0576c975)

## 11. Установим сервер OpenVAS на дистрибутив Kali Linux

Для этого была установлена Kali Linux


![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/c8fa0aae-ba74-4742-9c9b-d397c8090ea3)

## 12. Настройка сервиса OpenVAS

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/75f23159-c797-4ef4-8c7c-ad73232bd78e)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/9a438824-00b8-49d2-a0d4-b44a1627efdf)

Обновление базы данных

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/fc100483-006a-4002-8eea-fc4aa95f6f75)

## 13. Проверка GreenBone

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/7743946d-ab99-4c1c-9150-f9a8b7d81021)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/977872b4-8900-4dff-bc74-545f943b2f9b)

## 14. Проверка GreenBone
