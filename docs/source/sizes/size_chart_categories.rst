Категорії Розмірних Сіток
================

Отримання списку всіх категорій розмірних сіток
------------------

.. http:get:: /kw_api/integration/size_chart_categories

    У результаті запиту отримуємо списку всіх категорій розмірних сіток.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/size_chart_categories

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/size_chart_categories'
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
                    "product_size_chart_id":1
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


Отримання категорії розмірної сітки за id номером
--------------------------------------------------

.. http:get:: /kw_api/integration/size_chart_categories/(int:size_chart_category_id)

    У результаті запиту отримуємо розмірну сітку за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/size_chart_categories/(int:size_chart_category_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/size_chart_categories/(int:size_chart_category_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

       {
           "result":{
                "id":1,
                "name":"string",
                "active":true,
                "product_size_chart_id":1
           }
       }


    :query int size_chart_category_id: параметр ідентифікатор категорії розмірної сітки


Створення списку категорії розмірної сітки
--------------------------------------------------

.. http:post:: /kw_api/integration/size_chart_categories

    У результаті запиту створюємо категорії розмірної сітки.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/size_chart_categories

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/size_chart_categories'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "size_chart_categories":[
              {
                "name":"string",
                "product_size_chart_id":1
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
                "active":true,
                "product_size_chart_id":1
            }]
        }


    **Обов'язкові поля відмічені '*'**


    :>json string name: ім’я розмірної сітки*
    :>json int product_size_chart_id: ідентифікатор розміру продукту


Редагування категорії розмірної сітки за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/size_chart_categories/(int:size_chart_category_id)

    У результаті запиту редагуємо розмірну сітку.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/size_chart_categories/(int:size_chart_category_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/size_chart_categories/(int:size_chart_category_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
             "name":"string",
             "product_size_chart_id":1
        }


    **Example response**:

    .. sourcecode:: json

        {
            "jsonrpc": "2.0",
            "id": null,
            "result": {
                "id":1,
                "name":"string",
                "active":true,
                "product_size_chart_id":1
            }
        }


    **Обов'язкові поля відмічені '*'**


    :>json string name: ім’я розмірної сітки*
    :>json int product_size_chart_id: ідентифікатор розміру продукту
    :query int size_chart_category_id: параметр ідентифікатор категорії розмірної сітки