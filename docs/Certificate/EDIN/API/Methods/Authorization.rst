######################
**Авторизація**
######################

Після підключення послуги для роботи з API, користувач отримує логін та пароль для авторизації. Авторизація API відбувається за допомогою передачі цих ключових параметрів в HTTPS запиті:

- **varLogin​** - рядок; логін користувача
- **varPassword​** - рядок; пароль користувача

Після авторизації відбувається передача унікального токена "varToken" для подальшої роботи. Отримане значення varToken потрібно враховувати у всіх подальших запитах API разом з іншими параметрами в тілі запиту (json). Після авторизації час життя сесії при бездіяльності користувача становить 30 хвилин.

+----------------------------------------------------------------+----------------------------------------------------------------+
|                        **Метод запиту**                        |                         **HTTP POST**                          |
+================================================================+================================================================+
| **Content-Type**                                               | application/json (тіло HTTP запиту / відповіді в json форматі) |
+----------------------------------------------------------------+----------------------------------------------------------------+
| **URL запиту**                                                 | **https://edo.edi-n.com/Api/V1/User/Authorize**                |
+----------------------------------------------------------------+----------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)**   | -//-                                                           |
+----------------------------------------------------------------+----------------------------------------------------------------+
| **Обов'язкові параметри, що передаються в тілі запиту (json)** | **varLogin​** - рядок; логін користувача                       |
|                                                                |                                                                |
|                                                                | **varPassword​** - рядок; пароль користувача                   |
+----------------------------------------------------------------+----------------------------------------------------------------+


При авторизації json-тіло **запиту** відсутнє (інші дані передавати не потрібно).
При успішній авторизації отримуємо у відповідь "токен", необхідний для подальшої роботи, наприклад:

.. code:: ruby

  {
    "varToken": "jttk01diftvnbq2l2dgr5eib03",
    "varMessage": "Success!",
    "intCode": 200
  }








