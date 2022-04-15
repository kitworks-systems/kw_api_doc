Бренди товарів
================

Отримання списку всіх брендів
------------------

.. http:get:: /kw_api/integration/product_brands

    Отримання списку всіх картинок за id продукта

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/product_brands

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/product_brands'
            response = requests.get(URL, headers=headers)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "content":[
                 {
                    "id":1,
                    "name":"string",
                    "description":"string",
                    "partner_id":1,
                    "products_count":1,
                    "product_ids":[
                       {
                          "id":1,
                          "name":"string"
                       },
                       {
                          "id":2,
                          "name":"string"
                       }
                    ]
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


Отримання бренду за id
------------------

.. http:get:: /kw_api/integration/product_brands/(int:product_brand_id)

    У результаті запиту отримуємо бренд за id.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/product_brands/(int:product_brand_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/product_brands/(int:product_brand_id)'
            response = requests.get(URL, headers=headers)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

       {
           "result":{
              "id":1,
              "name":"string",
              "description":"string",
              "partner_id":1,
              "products_count":1,
              "product_ids":[
                 {
                    "id":1,
                    "name":"string"
                 },
                 {
                    "id":2,
                    "name":"string"
                 }
              ]
           }
        }


    :query int product_brand_id: параметр ідентифікатор бренда


Створення брендів
--------------------------------------------------

.. http:post:: /kw_api/integration/product_brands

    У результаті запиту створюємо бренди.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)
        
    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Authorization: Bearer_ + Your Api Key" \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/product_brands

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/product_brands'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "product_brands":[
              {
                   "name":"string",
                   "description":"string",
                   "partner_id":1
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
                    "description":"string",
                    "partner_id":1,
                    "products_count":0,
                    "product_ids":[]
             }]
        }


     **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я бренда*
    :>json string description: опис бренда
    :>json int partner_id: ідентифікатор партнера


Редагування бренд за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/product_brands/(int:product_brand_id)

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)
        
    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Authorization: Bearer_ + Your Api Key" \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/product_brands/(int:product_brand_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/product_brands/(int:product_brand_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
             "name":"string",
             "description":"string",
             "partner_id":1
        }


    **Example response**:

    .. sourcecode:: json

       {
            "jsonrpc": "2.0",
            "id": null,
            "result": {
                "id":1,
                "name":"string",
                "description":"string",
                "partner_id":1,
                "products_count":0,
                "product_ids":[]
            }
        }


     **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я бренда*
    :>json string description: опис бренда
    :>json int partner_id: ідентифікатор партнера
    :query int product_brand_id: параметр ідентифікатор бренда


