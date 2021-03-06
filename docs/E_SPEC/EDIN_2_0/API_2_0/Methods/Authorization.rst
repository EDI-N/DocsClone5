######################
**Авторизація**
######################

Після підключення послуги для роботи з API, користувач отримує логін, пароль і api_key для авторизації.

.. csv-table:: 
  :file: Authorization.csv
  :widths:  10, 41
  :stub-columns: 0

**Приклад запиту:**

.. code:: none

  email=senderx&password=1234x

**RESPONSE**

В **тілі відповіді** в json-форматі передається "ключ сесії", необхідний для подальшої роботи. В кожному наступному запиті (виклику методу) повинен бути присутнім HTTP-заголовок (Header) "Authorization", який для коректного виконання запитів повинен містити токен "SID" зі значенням, отриманим при авторизації.

**Приклад відповіді (JSON):**

.. code:: json

  {"SID": "65daxx25-74ba-4c85-8183-71b404a3xxc0"}

.. hint::
  Тривалість сесії при бездіяльності користувача становить 20 хвилин (мається на увазі, що ключ буде видалено через 20 хвилин, якщо користувач не буде активним (не буде відправляти HTTP запити)).


