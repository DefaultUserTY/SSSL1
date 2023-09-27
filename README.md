# ПРЗ 1. Сбор логов
Чадов Виктор Тимофеевич ББМО-01-22

## 1. Создать 2 виртуальные машины на базе ОС Debian 12

Две виртуальные машины debian

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/c04e8514-6a91-4103-8157-d620350a09f4)

## 2. Обеспечить между ними сетевой обмен

## 3. Включить на 1й из ВМ передачу логов по протоколу rsyslog на 2ю ВМ

Запуск rsyslog

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/805e833f-9798-4636-ab71-2bf5141e273b)

ip адрес машины получателя

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/603b862b-4d89-48bd-9269-0f0bd88d9fab)

Изменение конфига rsyslog машины отправителя sudo nano /etc/rsyslog.conf

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/9c49cddf-8f11-4e92-a546-c12a0ed1d5b5)

Изменение конфига rsyslog машины получателя sudo nano /etc/rsyslog.conf

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/dd74df72-be6d-4f5b-96dd-b8bd5183724c)

## 4. Установить и настроить получение логов на сервер с использованием Loki

