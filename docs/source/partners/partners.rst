партнери
================

Отримання списку всіх партнерів
------------------
.. http:get:: /kw_api/integration/partners

    У результаті запиту отримуємо списку всіх партнерів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/partners

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/partners'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":[
              {
                 "id":1,
                 "name":"string",
                 "ref":"string",
                 "lang":"en_US",
                 "website":"http://www.example.com",
                 "phone":"(000)-000-0000",
                 "email":"example@example.com",
                 "city":"Fremont",
                 "street":"string",
                 "street2":"string"
              }
           ]
        }


Отримання партнера за id номером
------------------
.. http:get:: /kw_api/integration/partners/(int:partner_id)

    У результаті запиту отримуємо користувача за id номером.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/partners/(int:partner_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/partners/(int:partner_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

       {
           "result":{
              "id":1,
              "name":"string",
              "ref":"string",
              "lang":"en_US",
              "website":"http://www.example.com",
              "phone":"(000)-000-0000",
              "email":"example@example.com",
              "city":"Fremont",
              "street":"string",
              "street2":"string"
           }
        }


    :query int partner_id: url параметр ідентифікатор партнера


Створення списку партнерів
--------------------------------------------------

.. http:post:: /kw_api/integration/partners

    У результаті запиту створюємо партнерів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/partners

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/partners'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "partners":[
              {
                 "name":"string",
                 "ref":"string",
                 "website":"http://www.example.com",
                 "phone":"(000)-000-0000",
                 "email":"example@example.com",
                 "city":"string",
                 "street":"string",
                 "street2":"string"
              }
           ]
        }

    **Example response**:

    .. sourcecode:: json

        {
           "jsonrpc":"2.0",
           "id":null,
           "result":[
              {
                 "id":0,
                 "name":"string",
                 "sale_ok":false,
                 "description":"string",
                 "description_purchase":"string",
                 "description_sale":"string",
                 "type":"product",
                 "rental":false,
                 "categ_id":"product.category()",
                 "list_price":0.0,
                 "standard_price":0.0,
                 "price_extra":0.0,
                 "taxes_id":"account.tax()",
                 "purchase_ok":false,
                 "active":true,
                 "color":0,
                 "is_product_variant":true,
                 "default_code":"string",
                 "barcode":"string",
                 "images_url":"http://url/kw_api/integration/image/product.image/68/image_1920/",
                 "currency_id":0
              }
           ]
        }


    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я  партнера*
    :>json string ref: опис
    :>json string website: сайт
    :>json string phone: телефон партнера*
    :>json string email: електронна почта партнера*
    :>json string city: місто партнера
    :>json string street: адреса партнера
    :>json string street2: додаткова адреса партнера


Редагування партнера за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/partners/(int:partner_id)

    У результаті запиту отримуємо партнера за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/partners/(int:partner_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/partners/(int:partner_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "partners":[
              {
                 "name":"string",
                 "ref":"string",
                 "website":"http://www.example.com",
                 "phone":"(000)-000-0000",
                 "email":"example@example.com",
                 "city":"string",
                 "street":"string",
                 "street2":"string"
              }
           ]
        }

    **Example response**:

    .. sourcecode:: json

        {
           "jsonrpc":"2.0",
           "id":null,
           "result":[
              {
                 "id":0,
                 "name":"string",
                 "sale_ok":false,
                 "description":"string",
                 "description_purchase":"string",
                 "description_sale":"string",
                 "type":"product",
                 "rental":false,
                 "categ_id":"product.category()",
                 "list_price":0.0,
                 "standard_price":0.0,
                 "price_extra":0.0,
                 "taxes_id":"account.tax()",
                 "purchase_ok":false,
                 "active":true,
                 "color":0,
                 "is_product_variant":true,
                 "default_code":"string",
                 "barcode":"string",
                 "images_url":"http://url/kw_api/integration/image/product.image/68/image_1920/",
                 "currency_id":0
              }
           ]
        }


    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я  партнера*
    :>json string ref: опис
    :>json string website: сайт
    :>json string phone: телефон партнера*
    :>json string email: електронна почта партнера*
    :>json string city: місто партнера
    :>json string street: адреса партнера
    :>json string street2: додаткова адреса партнера
    :query int partner_id: url параметр ідентифікатор партнера