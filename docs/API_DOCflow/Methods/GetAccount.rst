#############################################################
**Отримання даних аккаунту**
#############################################################

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/API_DOCflow/Methods/Authorization.html>`__ .

+--------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
|                       **Метод запиту**                       |                                              **HTTP GET**                                              |
+==============================================================+========================================================================================================+
| **Content-Type**                                             | application/json (тіло запиту/відповіді в json форматі в тілі HTTP запиту)                             |
+--------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
| **URL запиту**                                               | https://doc.edi-n.com/bdoc/account                                                                     |
+--------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)** | В рядку заголовка (Header) "Set-Cookie" обов'язково передається SID - токен, отриманий при авторизації |
+--------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+

**JSON-параметри в тілі HTTP запиту/відповіді**
***********************************************************

``REQUEST``

В цьому методі json-тіло **запиту** відсутнє (інші дані передавати не потрібно).

``RESPONSE``

У **відповідь** передаються дані аккаунта (об'єкт **Account**).

Таблиця 1 - Опис параметрів об'єкта **Account**

.. csv-table:: 
  :file: for_csv/Account.csv
  :widths:  1, 12, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 2 - Опис параметрів об'єкта **Company**

.. csv-table:: 
  :file: for_csv/Company.csv
  :widths:  1, 12, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 3 - Опис параметрів об'єкта **AdminAccount**

.. csv-table:: 
  :file: for_csv/AdminAccount.csv
  :widths:  1, 12, 41
  :header-rows: 1
  :stub-columns: 0

**Приклади**
*********************************

**При використанні методу json-тіло запиту відсутнє (дані передавати не потрібно)**

--------------

Приклад тіла **відповіді** в json форматі 

.. code:: ruby

  {
    "accountId": 8,
    "activityBase": "Царь царей",
    "addInfo": "kjkjаыавы",
    "adminAccount": {
      "address_fact": "Фактический адрес",
      "address_legal": "Юридический адрес",
      "agreement_date": "2018-09-10 00:00:00",
      "agreement_number": "15.08.2018",
      "bank_account": "4634653654665",
      "bank_mfo": "56456",
      "bank_name": "6436",
      "category_id": "0",
      "director_name": "443643646ggg",
      "director_position": "5688888іваіваіва",
      "edrpou": "00000000",
      "email": "alieva@edi.su",
      "id": 1232,
      "inn": "11111111111100",
      "name": "Тесте",
      "nds_cert_num": "-",
      "operation": "111111100000000",
      "own_type": "ТОВАРИСТВО З ОБМЕЖЕНОЮ ВІДПОВІДАЛЬНІСТЮ",
      "phone": "32623626526",
      "status": "test"
    },
    "adminAccountId": 1232,
    "company": {
      "accountId": 8,
      "atCode": "12363",
      "certNum": "456",
      "certificates": [],
      "code": "34554355",
      "companyId": 4,
      "dictionaries": [],
      "info": "ewdw",
      "inn": "123456789043",
      "isActive": 1,
      "isApproved": 1,
      "isSignedOffer": 1,
      "legalName": "ПрАТ \"Літак\"",
      "name": "Царь Царей",
      "notifySettings": [],
      "ownershipTypeId": 6,
      "phone": "4234234324",
      "prsNum": "43242352",
      "type": 1,
      "uuid": "a903de62-5b34-43c9-b73a-fb2b8ee4efc1"
    },
    "companyId": 4,
    "decryptType": 1,
    "dirPosition": "Оплачено",
    "email": "dfsjfjdsji@meta.ua",
    "fullName": "Ляшенко Евгений",
    "isIndivOffer": 1,
    "phone": "2",
    "status": 1,
    "tariffId": 0,
    "whiteList": []
  }


