Розміри
================

Отримання списку всіх розмірів
------------------

.. http:get:: /kw_api/integration/sizes

    У результаті запиту отримуємо списку всіх розмірів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/sizes

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/sizes'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "content":[
                 {
                    "id":1,
                    "name":"string",
                    "active":true,
                    "product_size_chart_id":1,
                    "primary_product_size_id":false,
                    "min_dimension_1":0.0,
                    "max_dimension_1":0.0,
                    "min_dimension_2":0.0,
                    "max_dimension_2":0.0
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


Отримання розміру за id номером
--------------------------------------------------

.. http:get:: /kw_api/integration/sizes/(int:kw_product_size_id)

    У результаті запиту отримуємо продукт за id номером.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/sizes/(int:kw_product_size_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/sizes/(int:kw_product_size_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
                "id":1,
                "name":"string",
                "active":true,
                "product_size_chart_id":1,
                "primary_product_size_id":false,
                "min_dimension_1":0.0,
                "max_dimension_1":0.0,
                "min_dimension_2":0.0,
                "max_dimension_2":0.0
             }
        }

    :query int product_size_id: параметр ідентифікатор розміру


Створення списку розмірів
--------------------------------------------------

.. http:post:: /kw_api/integration/sizes

    У результаті запиту створюємо розміри.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/sizes

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/sizes'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "sizes":[
             {
                "name":"string",
                "product_size_chart_id":1,
                "primary_product_size_id":false,
                "min_dimension_1":0.0,
                "max_dimension_1":0.0,
                "min_dimension_2":0.0,
                "max_dimension_2":0.0
              }
           ]
        }


    **Example response**:

    .. sourcecode:: json

        {
            "jsonrpc": "2.0",
            "id": null,
            "result": [
               {
                    "id":1,
                    "name":"string",
                    "active":true,
                    "product_size_chart_id":1,
                    "primary_product_size_id":false,
                    "min_dimension_1":0.0,
                    "max_dimension_1":0.0,
                    "min_dimension_2":0.0,
                    "max_dimension_2":0.0
                }
            ]
        }

    **Обов'язкові поля відмічені '*'**


    :>json string name: ім’я стадії*
    :>json int product_size_chart_id: ідентифікатор розмірної сітки
    :>json boolean primary_product_size_id: ідентифікатор головного розміру
    :>json float min_dimension_1: мінімальний розмір 1
    :>json float max_dimension_1: максимальний розмір 1
    :>json float min_dimension_2: мінімальний розмір 2
    :>json float max_dimension_2: максимальний розмір 2


Редагування розміра за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/sizes/(int:kw_product_size_id)

    У результаті запиту створюємо розміри.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/sizes/(int:kw_product_size_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/sizes/(int:kw_product_size_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
            "name":"string",
            "product_size_chart_id":1,
            "primary_product_size_id":false,
            "min_dimension_1":0.0,
            "max_dimension_1":0.0,
            "min_dimension_2":0.0,
            "max_dimension_2":0.0
        }


    **Example response**:

    .. sourcecode:: json

       {
            "jsonrpc": "2.0",
            "id": null,
            "result":  {
                 "id":1,
                 "name":"string",
                 "active":true,
                 "product_size_chart_id":1,
                 "primary_product_size_id":false,
                 "min_dimension_1":0.0,
                 "max_dimension_1":0.0,
                 "min_dimension_2":0.0,
                 "max_dimension_2":0.0
            }
       }

    **Обов'язкові поля відмічені '*'**


    :>json string name: ім’я стадії*
    :>json int product_size_chart_id: ідентифікатор розмірної сітки
    :>json boolean primary_product_size_id: ідентифікатор головного розміру
    :>json float min_dimension_1: мінімальний розмір 1
    :>json float max_dimension_1: максимальний розмір 1
    :>json float min_dimension_2: мінімальний розмір 2
    :>json float max_dimension_2: максимальний розмір 2
    :query int kw_product_size_id: параметр ідентифікатор розміра