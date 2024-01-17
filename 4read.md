### lab1

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/288bb6c6-2258-493a-9137-a9d447619c5b)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/22ecd651-f235-44c5-a922-7d59e88ad1d8)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/4f7d063c-24ce-455b-8c93-d7dbc6770e75)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/862fcf25-f959-42ca-a285-71dbe1631e89)

Из 6 записей не ясно безопасна ли первая остальные 5 безопасные службы
пример 1 из 5

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/42a4428b-a6a6-4bb0-998f-b751feeb1d27)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/85aaeab0-a5f5-40bd-a558-c7eb5a4df9df)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/63a4c742-ebeb-4565-a0d9-1d79951c1f0e)

Первая

windows 7

нет доменного имени fqdn

очень равномерные запросы, причем это резкие всплеские через похожие(одинаковые) промежутки времени

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/aecb2d69-0500-4105-8caa-f3e6cafc6dcd)

перепроверим на угрозу c2

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/36775872-10bf-4cd6-934f-4f736962a170)

первая команда смотрим был ли запрос через fqdn

вторая смотрим http файл видим вновь отсутствие fqdn

третья смотрим что использовалось в основном win10 win7 в одном случае

четвертая видим что 3011 подключений по подозрительной длинной ссылке скорее всего подключение вредоносное

----------------------------------------------------------------------------------------------------------

подключения перепроверим через virustotal

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/d05e6058-b1ba-4c18-a0c8-425fba7c8abc)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/53be3074-8c01-401e-8110-3ad4d0b4ac6f)

### lab 2

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/3ebafb70-b8b8-4525-8916-1b54f0182ca8)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/25807ffc-8f38-4acc-9ea8-36f227bef16e)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/1d605151-cb4d-4013-8e68-db94efb1267b)

Странные имена вероятность c2 огромна

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/5f385f98-24e6-4966-9d28-23284cfa357c)

### lab 3

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/a0891081-d5b7-420d-ab42-3512c2a69ad4)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/c0f12a7d-d355-430a-af9d-70989450c52d)

Проверим записи 

Первая вредоносная следует устранить инцидент, последующие "чистые"

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/a5e8d76c-da78-494f-8091-145534410978)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/56707cad-7a29-4c37-a00b-2e5979a2d67b)

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/d2dc1efb-2004-42b2-9d5d-c3dfc500791d)

В разделе beacons есть два dns запроса требуется проверить были ли они запланированы и проверить конечные точки

![image](https://github.com/DefaultUserTY/SSSL1/assets/131360754/2364f2fc-065d-4455-b7bf-d5b2cf4df55f)

