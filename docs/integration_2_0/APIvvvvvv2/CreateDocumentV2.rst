######################################################################
**Створення чернетки документа**
######################################################################

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/integration_2_0/APIv2/Authorization.html>`__ .

За допомогою POST методу **api/eds/doc** можливо швидко створити чернетку документа конкретного зазначеного типу для конкретного одержувача.

+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|                       **Метод запиту**                       |                                                        **HTTP POST**                                                        |
+==============================================================+=============================================================================================================================+
| **Content-Type**                                             | application/json (тіло HTTP запиту / відповіді в json форматі)                                                              |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| **URL запиту**                                               | **https://edo-v2.edi-n.com/api/v2/eds/doc**?gln=9864065702429&doc_type=orders                                               |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)** | У рядку заголовка (Header) "Authorization" обов'язково передається **SID** - токен отриманий при авторизації                |
|                                                              |                                                                                                                             |
|                                                              | **Обов'язкові url-параметри:**                                                                                              |
|                                                              |                                                                                                                             |
|                                                              | **gln** - рядок (13); номер GLN організації, яка пов'язана з авторизованим користувачем платформи EDIN 2.0 на рівні акаунта |
|                                                              |                                                                                                                             |
|                                                              | **doc_type** - рядок; конкретний тип документа (опис_параметрів_)                                                           |
+--------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+

.. hint:: Також можливо виконати запит у вигляді curl-рядка:
          
          curl -X POST 'https://edo-v2.edi-n.com/api/v2/eds/doc?gln=9864065702429&doc_type=orders' -d {json - тело документа} -b 'SID=458a0d38-5b56-4b8e-8998-009a1edd31eb'

Специфікація для розшифровки ключів curl запиту: https://curl.haxx.se/docs/manpage.html

--------------------------------------

**JSON-параметри в тілі HTTP запиту/відповіді**

--------------------------------------

``REQUEST``

У цьому методі в json-тілі **запиту** передаються поля документа (зі `специфікацією документів <https://wiki.edi-n.com/uk/latest/XML/XML-structure.html>`__ ви можете ознайомитися у відповідному розділі).

``RESPONSE``

Таблиця 1 - Опис json-параметрів, що можуть передаватися у **відповідь** (об'єкт створеного документа-чернетки) на метод API.

.. csv-table:: 
  :file: for_csv/XDoc.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 2 - Опис параметрів об'єкта **XTag**

.. csv-table:: 
  :file: for_csv/XTag.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 3 - Опис параметрів об'єкта **XStatus**

.. csv-table:: 
  :file: for_csv/XStatus.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 4 - Опис параметрів об'єкта **XDocSignInfo**

.. csv-table:: 
  :file: for_csv/XDocSignInfo.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 5 - Опис параметрів об'єкта **XDocCommentsList**

.. csv-table:: 
  :file: for_csv/XDocCommentsList.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 6 - Опис параметрів об'єкта **XDocComment**

.. csv-table:: 
  :file: for_csv/XDocComment.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 7 - Опис параметрів об'єкта **XDocAttachment**

.. csv-table:: 
  :file: for_csv/XDocAttachment.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 8 - Опис параметрів об'єкта **XDocBodyForms**

.. csv-table:: 
  :file: for_csv/XDocBodyForms.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 9 - Опис параметрів об'єкта **XDocBody**

.. csv-table:: 
  :file: for_csv/XDocBody.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 10 - Опис параметрів об'єкта **XDocBodyType**

.. csv-table:: 
  :file: for_csv/XDocBodyType.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 11 - Опис параметрів об'єкта **XDocType**

.. csv-table:: 
  :file: for_csv/XDocType.csv
  :widths:  1, 7, 12, 41
  :header-rows: 1
  :stub-columns: 0

.. _опис_параметрів:

Таблиця 12 - Опис **DocType** параметрів (об'єкт XDocType_)

.. csv-table:: 
  :file: for_csv/xdoctype_p.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблиця 13 - Опис параметрів об'єкта **XDocStatus**

.. csv-table:: 
  :file: for_csv/XDocStatus.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

.. _детальніше:

Таблиця 14 - Опис **DocStatus** параметрів (об'єкт XDocStatus_)

.. csv-table:: 
  :file: for_csv/xdocstatus_p.csv
  :widths:  1, 60
  :header-rows: 1
  :stub-columns: 0

--------------

**Приклади**

--------------

**Приклад тіла запиту (json):**

.. code:: ruby

   {
	"NUMBER": "6422722fb78c4509b06eac43758e1545",
	"DATE": "2019-02-15",
	"TIME": "00:00",
	"ORDERNUMBER": "6422722fb78c4509b06eac43758e1545",
	"ORDERDATE": "2019-02-15",
	"DELIVERYDATE": "2019-02-30",
	"DELIVERYTIME": "10:00",
	"CAMPAIGNNUMBER": "334455",
	"CURRENCY": "UAH",
	"LIMES": [],
	"HEAD": [
		{
			"BUYER": "4820128010004",
			"SUPPLIER": "9864065702429",
			"DELIVERYPLACE": "4820128019007",
			"INVOICEPARTNER": "4820128010004",
			"SENDER": "4820128010004",
			"RECIPIENT": "9864065702429",
			"POSITION": [
				{
					"POSITIONNUMBER": "1",
					"PRODUCT": "5029053540900",
					"PRODUCTIDBUYER": "527209",
					"DESCRIPTION": "пироженко",
					"PRICE": 510,
					"PRICEWITHVAT": 571.2,
					"VAT": "12.00",
					"AMOUNT": 0,
					"AMOUNTWITHVAT": 0,
					"ORDEREDQUANTITY": 64,
					"ACCEPTEDQUANTITY": 64,
					"PRODUCTTYPE": "1"
				},
				{
					"POSITIONNUMBER": "2",
					"PRODUCT": "5029053540924",
					"PRODUCTIDBUYER": "527215",
					"DESCRIPTION": "мороженко",
					"PRICE": 510,
					"PRICEWITHVAT": 571.2,
					"VAT": "12.00",
					"AMOUNT": 0,
					"AMOUNTWITHVAT": 0,
					"ORDEREDQUANTITY": 32,
					"ACCEPTEDQUANTITY": 32,
					"PRODUCTTYPE": "1"
				},
				...
				{
					"POSITIONNUMBER": "48",
					"PRODUCT": "5029053543987",
					"PRODUCTIDBUYER": "100307632",
					"DESCRIPTION": "водочка",
					"PRICE": 1751.6,
					"PRICEWITHVAT": 1961.79,
					"VAT": "12.00",
					"AMOUNT": 0,
					"AMOUNTWITHVAT": 0,
					"ORDEREDQUANTITY": 12,
					"ACCEPTEDQUANTITY": 12,
					"PRODUCTTYPE": "1"
				}
			]
		}
	],
	"ACTION": "29"
	}

--------------

**Приклад тіла відповіді (json):**

Повертаємий текст - об'єкт створеного документа-чернетки:

.. code:: ruby

    {
      "attachments": [],
      "body": {
        "forms": {
          "json": {
            "type": {
              "id": 2,
              "name": "json"
            }
          }
        }
      },
      "chain_id": 0,
      "comments": [],
      "dateChanged": 0,
      "dateCreated": 1574421527,
      "dateRead": 0,
      "docDate": 1565211600,
      "docNumber": "2019-08-08-TEST-001",
      "doc_id": 143,
      "doc_uuid": "6ffc8dfa-1cd5-4137-82cf-29b5969c2e74",
      "extraFields": {
        "basis_doc_date": "1565211600",
        "basis_doc_number": "1",
        "basis_doc_subtype": "007",
        "doc_date": "1565211600",
        "doc_num": "2019-08-08-TEST-001",
        "order_number": "1",
        "recipient": "9864232319979",
        "sender": "9864232319962",
        "sub_doc_type_id": "006"
      },
      "family": 1,
      "hash": "D4733FDDDEBE23B4E38DC5F257604234",
      "is_archive": false,
      "multiExtraFields": {},
      "status": {
        "status": 1,
        "title": "open"
      },
      "statuses": [],
      "tags": [],
      "type": {
        "description": "Коммерческий документ",
        "title": "comdoc",
        "type": 28
      },
      "uuidReceiver": "9864232319979",
      "uuidSender": "9864232319962"
    }


