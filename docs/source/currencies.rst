Currencies
================

Отримання списку всіх валют
-----------------------------

GET /kw_api/integration/currencie

У результаті запиту отримуємо списку всіх валют.

Parameters

Request body

Responses

200 - Successful Response

.. code-block:: console

    {
      "result": [
        {
          "id": 1,
          "name": "EUR",
          "symbol": "€",
          "rate": 1,
          "rate_ids": [
            129
          ],
          "rounding": 0.01,
          "decimal_places": 2,
          "position": "after",
          "date": "2010-01-01",
          "currency_unit_label": "Euros",
          "currency_subunit_label": "Cents"
        }
      ]
    }


Отримання валюту за id номером
---------------------------------

GET /kw_api/integration/currencies/<int:currency_id>

Request body

Responses

200 - Successful Response

.. code-block:: console

    {
      "result": {
        "id": 1,
        "name": "EUR",
        "symbol": "€",
        "rate": 1,
        "rate_ids": [
          129
        ],
        "rounding": 0.01,
        "decimal_places": 2,
        "position": "after",
        "date": "2010-01-01",
        "currency_unit_label": "Euros",
        "currency_subunit_label": "Cents"
      }
    }


