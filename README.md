# ПРЗ 1. Сбор логов
Чадов Виктор Тимофеевич ББМО-01-22

## 1. Создать 2 виртуальные машины на базе ОС Debian 12

Две виртуальные машины debian

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/70675827-1f09-45fc-99b0-f83917f6cf19)

## 2. Обеспечить между ними сетевой обмен

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/1a35823f-a7d4-43b2-b36a-7513d328b698)

## 3. Включить на 1й из ВМ передачу логов по протоколу rsyslog на 2ю ВМ

Запуск rsyslog

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/805e833f-9798-4636-ab71-2bf5141e273b)

Изменение конфига rsyslog машины получателя sudo nano /etc/rsyslog.conf

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/6f30f09a-c83d-48f1-b7d9-b16cfbb3697a)

На машине отправителя создадим файл конфигурации rsyslog, запишем туда правило перенаправляющее все логи на получателя.

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/e6f0c23e-d43e-40ab-b4a2-9c1e9ccdbdd3)

Проверим работу

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/8b23221e-dc52-4be0-b6ec-adfae3a9f2b4)


## 4. Установить и настроить получение логов на сервер с использованием Loki

Установим loki

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/266173aa-a033-48d5-bc54-62ee075118d3)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/133cb5ef-ddb5-4861-b0a0-f22b29a8d02b)

Запустим loki

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/c1fe4c07-ce72-4ce6-9a98-afc7edbf5805)

Проверим в браузере

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/57510713-5319-4949-8ea9-1178102032fa)

Установим приемник promtail

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/99cdd59d-3e8a-465b-8c6b-a44d90f4ca99)

Изменим конфиг promtail для передачи данных на получателя

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/ec75495b-5333-4b1a-9646-45a8d48c2a20)

Запустим promtail 

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/fc51b3ac-6c9d-4220-b318-2408bb3e5c58)

Проверим в браузере

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/0f098ea5-0908-47c1-b431-98bb7570ce65)

Установим SigNoz

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/0d17f7ba-3815-4ab0-af6d-f15c5ee3c92d)

Проверим в браузере

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/d1234847-9fb0-49e4-9159-b9f997b782af)


