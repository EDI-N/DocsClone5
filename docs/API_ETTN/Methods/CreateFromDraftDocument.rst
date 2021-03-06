###########################################################################
**Створення документу еТТН на основі чернетки, створеної контрагентом**
###########################################################################

.. hint:: 
    Зі схемою документообігу, в якій ініціаторами документообігу еТТН виступають **"Перевізники"** чи **"Вантажоотримувачі"** можливо ознайомитись в `наступній інструкції <https://wiki.edi-n.com/uk/latest/ETTN_2_0/Creation_sending_ETTN_carrier_consignee.html>`__.

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/API_ETTN/Methods/Authorization.html>`__ .

.. csv-table:: 
  :file: CreateFromDraftDocument.csv
  :widths:  10, 41
  :stub-columns: 0

**RESPONSE**

В тілі **відповіді** (json) передається **doc_uuid** - унікальний ідентифікатор документа на платформі: 

.. code:: json

  {doc_uuid:"e3dbf6e8-029e-4c3b-804b-9b2741d9f37d"}

