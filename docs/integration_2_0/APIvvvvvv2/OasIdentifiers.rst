######################################################################
**Отримання інформації про організацію по Назві/ІПН/КПП/GLN**
######################################################################

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/integration_2_0/APIv2/Authorization.html>`__ .

Метод дозволяє користувачеві переглядати додаткову інформацію про інших користувачів на рівні одного загального аккаунта.

+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|                       **Метод запиту**                       |                                                        **HTTP GET**                                                         |
+==============================================================+=============================================================================================================================+
| **Content-Type**                                             | application/json (тіло HTTP запиту / відповіді в json форматі)                                                              |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| **URL запиту**                                               | https://edo-v2.edi-n.com/api/oas/identifiers                                                                                |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)** | У рядку заголовка (Header) "Authorization" обов'язково передається **SID** - токен отриманий при авторизації                |
|                                                              | **Обов'язкові url-параметри:**                                                                                              |
|                                                              |                                                                                                                             |
|                                                              | **gln** - рядок (13); номер GLN організації, яка пов'язана з авторизованим користувачем платформи EDIN 2.0 на рівні акаунта |
|                                                              |                                                                                                                             |
|                                                              | **query** - рядок; назва/ІПН/КПП/GLN організації; "Над яким здійснюється дія"                                               |
|                                                              |                                                                                                                             |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+

.. hint:: Також можливо виконати запит у вигляді curl-рядка:
          
          curl -X GET 'https://edo-v2.edi-n.com/api/oas/identifiers?gln=9864065702429&query=EDS_1' -b 'SID=458a0d38-5b56-4b8e-8998-009a1edd31eb'

Специфікація для розшифровки ключів curl запиту: https://curl.haxx.se/docs/manpage.html

--------------

**JSON-параметри в тілі HTTP запиту/відповіді**

--------------

**REQUEST**

--------------

У цьому методі json-тіло **запиту** відсутнє (інші дані передавати не потрібно).

--------------

**RESPONSE**

--------------

Таблиця 1 - Опис json-параметрів, які можуть передаватися у **відповідь** на метод API

.. csv-table:: 
  :file: for_csv/Identificator.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 2 - Опис параметрів об'єкта **Account**)

.. csv-table:: 
  :file: for_csv/Account.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 1

Таблиця 3 - Опис параметрів об'єкта **Company**)

.. csv-table:: 
  :file: for_csv/Company.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 4 - Опис параметрів об'єкта **User**)

.. csv-table:: 
  :file: for_csv/User.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

--------------

**Приклади**

--------------

**При використанні методу json-тіло запиту відсутнє (дані передавати не потрібно)**

--------------

**Приклад тіла відповіді (json):**

.. code:: ruby

    [
  {
    "guid": {},
    "manager": "#",
    "id": 133187,
    "gln": "9864065702429",
    "companyId": 29824,
    "retailerId": 0,
    "name": "EDS_1",
    "companyType": "jur",
    "companyInn": "1010101010",
    "companyKpp": "90000031",
    "zip": "112233",
    "city": "г. Львов",
    "street": "ул. Хмурится, 6",
    "phone": "#",
    "otherInfo": "[]",
    "account": {
      "platform": "EVO",
      "id": 29824,
      "name": "Test_EDS1",
      "ownership": "#",
      "inn": "1010101010",
      "kpp": "100000001",
      "mail": "test@qw.we",
      "phone": "12345678901",
      "ndsNumber": "#",
      "bankAccount": "#",
      "bankName": "#",
      "bankMfo": "#",
      "bankAddress": "#",
      "identificators": [],
      "companies": [],
      "users": []
    }
  }
  ] 

