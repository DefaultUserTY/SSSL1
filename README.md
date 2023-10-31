# ПРЗ 3. Wazuh
Чадов Виктор Тимофеевич ББМО-01-22

## 1. Развернем 2 виртуальные машины (сервер и клиент)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/4f9f5084-2631-4109-b90e-34a235f8de11)

## 2. Обеспечить между ними сетевой обмен

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/081f6046-871a-457c-96bb-e5f170da7323)

## 3. Развернем на сервере Wazuh

Скачаем и установим Wazuh

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/c2a177d9-8126-437e-b676-4f227b5bb878)

## 4. Подключим агента

Устанавливаем агент

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/86dc8e9c-7db8-4f46-81eb-6a84e47681a9)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/2f64c754-32f9-4e3d-9cfb-d2a046616d18)

## 5. Подключимcя к Wazuh

Проверим подключение и посмотрим данные о агенте

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/8a5329d5-3805-40a2-96e9-0c2c33756ee8)

Общая вкладка о агенте

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/31b833ec-942c-42cf-9ca1-a6dc8652e910)

### Большая часть вкладок изначально пусты, однако уже можно посмотреть на часть из них

Cобытия безопасности

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/d29f8484-e610-49f2-b7d2-8ea8a3fb95e3)

Mitre Attack

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/2b967947-51c5-470f-8eae-9c1739a8772b)

Nist

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/68db3abe-a4b8-440e-b23d-aafec8571621)

## 6. Создадим проверку целостности файлов

Отредактируем конфигурацию агента /var/ossec/etc/ossec.conf добавив в список проверяемых папок в реальном времени /home

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/083f256a-8895-4ad2-8bd8-d37000a5d3a7)

Видим добавленные файлы из папки /home

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/63fa16b0-a501-4264-9867-d85320a72067)

Создадим файл 1111 для показа возможностей Wazuh

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/02403912-9b24-4ab8-baf6-87cf7ca41ee3)

## 7. Создадим настройку выявления уязвимостей

Сконфигурируем общего агента на сервере

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/9a1eeb49-64fc-4a35-a33c-bdbb705f871e)

Включим обнаружение уязвимостей для Ubuntu

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/b4f48464-a81d-48e7-b089-ef53d7de95a9)

Видим список уязвимостей

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/3fa3bb12-6e0a-4a8c-8f40-a9dde6878426)

## 8. Создадим выявление скрытых процессов

Установим rootkit

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/b251a5e3-c294-4bb1-91d5-2a8598508f30)

Изменим частоту проверок агента до 30 секунд

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/042388d1-b750-4a49-b90c-0169b46baa4f)

Имитация атаки

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/c5692a2f-0717-4489-a54f-fc3f45c9372e)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/1d296d24-a713-44d4-9ecb-7eb428f71272)

Посмотрим результат

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/04d34a89-d459-48a5-b414-f9aa6ddb48b8)

## 9. Создадим выявление sql иньекций

Добавим отслеживание apache

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/54fd37b4-69c9-40e0-afcc-57dc1e46c0b9)

Установим apache

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/36fe22cc-689c-4ac1-9278-be93e23109aa)

Сделаем иньекцию 

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/f36bac15-94f9-48cc-9f6b-6f81f6625925)

Видим sql иньекцию

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/99e10979-1cd9-4ad2-b2c6-88c506231e1c)

## 10. Выводы

В процессе выполнения данной работы был изучен функционал Wazuh, настроены и показаны механизмы его работы.
