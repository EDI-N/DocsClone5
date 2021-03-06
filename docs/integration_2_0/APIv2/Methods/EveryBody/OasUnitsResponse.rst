#############################################################
**Довідник одиниць виміру (масив об'єктів)**
#############################################################

**JSON:**

.. code:: json

	[
	  {
	    "id": 1,
	    "name": "GRM",
	    "nameOKEI": "Грамм",
	    "shortNameOKEI": "г",
	    "OKEI": "163",
	    "KSPOVO": "0303"
	  },
	  {
	    "id": 2,
	    "name": "KGM",
	    "nameOKEI": "Килограмм",
	    "shortNameOKEI": "кг",
	    "OKEI": "166",
	    "KSPOVO": "0301"
	  },
	  {
	    "id": 3,
	    "name": "LTR",
	    "nameOKEI": "Литр",
	    "shortNameOKEI": "л",
	    "OKEI": "112",
	    "KSPOVO": "0138"
	  },
	  ...
	  {
	    "id": 45,
	    "name": "OD",
	    "nameOKEI": "Единица (продукции)",
	    "shortNameOKEI": "од",
	    "KSPOVO": "2431"
	  }
	]

Таблиця 1 - Опис json-параметрів **відповіді** методу

+---------------+--------+----------------------------------------------+
|   Параметр    | Формат |                     Опис                     |
+===============+========+==============================================+
| id            | long   | ідентифікатор одиниці виміру                 |
+---------------+--------+----------------------------------------------+
| name          | String | найменування                                 |
+---------------+--------+----------------------------------------------+
| nameOKEI      | String | найменування згідно державного класифікатора |
+---------------+--------+----------------------------------------------+
| shortNameOKEI | String | сокращение згідно державного класифікатора   |
+---------------+--------+----------------------------------------------+
| OKEI          | String | код державного класифікатора                 |
+---------------+--------+----------------------------------------------+
| KSPOVO        | String | код КСПОВО                                   |
+---------------+--------+----------------------------------------------+
