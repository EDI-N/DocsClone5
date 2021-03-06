#############################################################################################################
**Допоміжний метод. Показує доступні дії для надання прав доступу до сертифіката (властивість сертифіката)**
#############################################################################################################

Для роботи з цим методом користувач повинен бути `авторизованим <https://wiki.edi-n.com/uk/latest/API_EDIN_Certificate/Methods/Authorization.html>`__ .

+--------------------------------------------------------------+--------------------------------------------------------------+
|                       **Метод запиту**                       |                         **HTTP GET**                         |
+==============================================================+==============================================================+
| **Content-Type**                                             | application/json (тіло HTTP запиту/відповіді в json форматі) |
+--------------------------------------------------------------+--------------------------------------------------------------+
| **URL запиту**                                               | **https://edo.edi-n.com/Api/V1/Certificate/ShowAccessTypes** |
+--------------------------------------------------------------+--------------------------------------------------------------+
| **Параметри, що передаються в URL (разом з адресою методу)** | -//-                                                         |
+--------------------------------------------------------------+--------------------------------------------------------------+

**JSON-параметри в тілі HTTP запиту/відповіді**
*******************************************************************

``REQUEST``

В цьому методі в json-тілі **запиту** обов'язково передається лише токен **varToken​**, отриманий при `авторизації <https://wiki.edi-n.com/uk/latest/API_EDIN_Certificate/Methods/Authorization.html>`__ 

``RESPONSE``

Таблиця 1 - Опис json-параметрів **відповіді** метода API

+-------------------------------+--------------------+---------+-------------------------------------------------------+
|           Параметр            | Mandatory/Optional | Формат  |                         Опис                          |
+===============================+====================+=========+=======================================================+
| ​**certificate_access_types** |                    | [{...}] | масив об'єктів; наданий доступ до сертифіката         |
+-------------------------------+--------------------+---------+-------------------------------------------------------+
| ​varMessage​                  |                    | String  | повідомлення сервера                                  |
+-------------------------------+--------------------+---------+-------------------------------------------------------+
| ​intCode​                     |                    | int     | код відповіді сервера                                 |
+-------------------------------+--------------------+---------+-------------------------------------------------------+
| code                          |                    | int     | код доступу; 1 - Доступний усім, 2 - Обмежений доступ |
+-------------------------------+--------------------+---------+-------------------------------------------------------+
| name                          |                    | String  | назва доступу                                         |
+-------------------------------+--------------------+---------+-------------------------------------------------------+


--------------

**Приклади**
*****************

Приклад тіла **запиту** в json форматі:

.. code:: ruby

  {
    "​ varToken​ ": "​ 8q0hu05o59vmmrpo4t5slfedj2​ "
  }

--------------

Приклад тіла **відповіді** в json форматі: 

.. code:: ruby

	{
	  "certificate_access_types": [
	    {
	      "code": 1,
	      "name ": "Доступен всем"
	    },
	    {
	      "code": 2,
	      "name ": "Ограниченный доступ"
	    }
	  ],
	  "varMessage": "Success!",
	  "intCode": 200
	}


