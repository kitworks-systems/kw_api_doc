Таблиці розмірів
================

Отримання списку всіх розмірних сіток
------------------

.. http:get:: /kw_api/integration/size_charts

    У результаті запиту отримуємо списку всіх розмірних сіток.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/size_charts

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/size_charts'
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
                    "display_name":"string",
                    "active":true,
                    "is_primary":true,
                    "is_computable":false,
                    "formula":"string",
                    "chart_category_id":1,
                    "primary_size_chart_id":1
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


Отримання розмірної сітки за id номером
--------------------------------------------------

.. http:get:: /kw_api/integration/size_charts/(int:kw_product_size_chart_id)

    У результаті запиту отримуємо розмірну сітку за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/size_charts/(int:kw_product_size_chart_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/size_charts/(int:kw_product_size_chart_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
                "id":1,
                "name":"string",
                "display_name":"string",
                "active":true,
                "is_primary":true,
                "is_computable":false,
                "formula":"string",
                "chart_category_id":1,
                "primary_size_chart_id":1
            }
        }

    :query int kw_product_size_chart_id: параметр ідентифікатор розмірної сітки


Створення списку розмірної сітки
--------------------------------------------------

.. http:post:: /kw_api/integration/size_charts

    У результаті запиту створюємо розміри.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/size_charts

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/size_charts'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "size_charts":[
              {
                "name":"string",
                "is_primary":true,
                "is_computable":false,
                "formula":"string",
                "chart_category_id":1,
                "primary_size_chart_id":1
              }
           ]
        }


    **Example response**:

    .. sourcecode:: json

        {
            "jsonrpc": "2.0",
            "id": null,
            "result": [{
                "id":1,
                "name":"string",
                "display_name":"string",
                "active":true,
                "is_primary":true,
                "is_computable":false,
                "formula":"string",
                 "chart_category_id":1,
                 "primary_size_chart_id":1
            }]
        }

    **Обов'язкові поля відмічені '*'**


    :>json string name: ім’я розмірної сітки*
    :>json boolean is_primary: флаг головної сітки
    :>json boolean is_computable: флаг вирахувань
    :>json string formula: формула вирахувань
    :>json int chart_category_id: ідентифікатор категорії розмірної сітки
    :>json int primary_size_chart_id:  ідентифікатор головної розмірної сітки


Редагування розмірної сітки за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/size_charts/(int:kw_product_size_chart_id)

    У результаті запиту редагуємо розмір.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/size_charts/(int:kw_product_size_chart_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/size_charts/(int:kw_product_size_chart_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
            "name":"string",
            "is_primary":true,
            "is_computable":false,
            "formula":"string",
            "chart_category_id":1,
            "primary_size_chart_id":1
        }




    **Example response**:

    .. sourcecode:: json

        {
            "jsonrpc": "2.0",
            "id": null,
            "result": {
                "id":1,
                "name":"string",
                "display_name":"string",
                "active":true,
                "is_primary":true,
                "is_computable":false,
                "formula":"string",
                 "chart_category_id":1,
                 "primary_size_chart_id":1
            }
        }


    **Обов'язкові поля відмічені '*'**


    :>json string name: ім’я розмірної сітки*
    :>json boolean is_primary: флаг головної сітки
    :>json boolean is_computable: флаг вирахувань
    :>json string formula: формула вирахувань
    :query int kw_product_size_chart_id: параметр ідентифікатор розмірної сітки



