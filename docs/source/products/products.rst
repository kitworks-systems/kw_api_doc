Товари
================

Отримання списку всіх продуктів
------------------

.. http:get:: /kw_api/integration/products

    У результаті запиту отримуємо список всіх продуктів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/products

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/products'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
          "result": {
            "content": [
              {
                "id": 0,
                "name": "string",
                "sale_ok": true,
                "description": "string",
                "description_purchase": "string",
                "description_sale": "string",
                "type": "bearer",
                "rental": false,
                "categ_id": 0,
                "list_price": 0,
                "standard_price": 0,
                "price_extra": 0,
                "taxes_id": null,
                "purchase_ok": true,
                "active": true,
                "color": 0,
                "is_product_variant": true,
                "default_code": "string",
                "barcode": "string",
                "images_url": "http://url/kw_api/integration/image/product.product/0/image_1920/",
                "currency_id": 0,
                "kw_product_size_chart_id": 1,
                "kw_product_size_id": 1,
                "kw_primary_product_size_id": 1,
                "kw_product_size_dimension_1": 1.1,
                "kw_product_size_dimension_2": 1.1,
                "kw_product_size_dimension_3": 1.1,
                "kw_pp_size_ids": [
                  {
                    "id": 1,
                    "product_id": 1,
                    "Product_size_chart_id": 1,
                    "kw_product_size_id": 1
                  }
                ],
                "kw_size_chart_category_id": 1
              }
            ],
            "totalElements": 1,
            "totalPages": 1,
            "numberOfElements": 1,
            "number": 0,
            "Last": false
          }
        }


Отримання списку всіх відредактованих продуктів за останню годину
------------------

.. http:get:: /kw_api/integration/product_price_update

    У результаті запиту отримуємо список всіх відредактованих за останню годину продуктів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/product_price_update

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/product_price_update'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
            "result": [
                {
                    "id": 15,
                    "name": "qq11aa22",
                    "list_price": 1.0,
                    "price": 1.0,
                    "promo_price": 1.0,
                    "currency": "UAH",
                    "currency_prices": [
                        {
                            "list_price": 1.0,
                            "price": 1.0,
                            "promo_price": 1.0,
                            "currency": "EUR"
                        },
                        {
                            "list_price": 1.0,
                            "price": 1.0,
                            "promo_price": 1.0,
                            "currency": "USD"
                        }
                    ]
                }
            ]
        }

    :query string update_date: час з якого показати редактовані продукти, формат - ``YYYY-MM-DDThh:mm:ss``


Отримання продукту за id номером
--------------------------------------------------

.. http:get:: /kw_api/integration/products/(int:product_id)/

    У результаті запиту отримуємо продукт за id номером.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/products/(int:product_id)/

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/products/(int:product_id)/'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "id":0,
              "name":"string",
              "sale_ok":true,
              "description":"string",
              "description_purchase":"string",
              "description_sale":"string",
              "type":"string",
              "rental":false,
              "categ_id":0,
              "list_price":0.0,
              "standard_price":8.0,
              "price_extra":0.0,
              "taxes_id":0,
              "purchase_ok":true,
              "active":true,
              "color":0,
              "is_product_variant":true,
              "default_code":"string",
              "barcode":"string",
              "images_url":"http://url/kw_api/integration/image/product.image/0/image_1920/",
              "currency_id":0,
           }
        }


    :query int product_id: ідентифікатор продукту


Отримання списку всіх шаблонів продукту
--------------------------------------------------

.. http:get:: /kw_api/integration/product_templates

    У результаті запиту отримуємо список всіх продуктів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/product_templates

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/product_templates'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "content":[
                 {
                    "id":0,
                    "name":"string",
                    "can_be_sold":true,
                    "description":"string",
                    "description_purchase":"string",
                    "description_sale":"string",
                    "type":"consu",
                    "rental":false,
                    "categ_id":0,
                    "list_price":0.0,
                    "standard_price":0.0,
                    "taxes_id":0,
                    "sale_ok":true,
                    "purchase_ok":true,
                    "active":true,
                    "color":0,
                    "is_product_variant":false,
                    "default_code":"string",
                    "barcode":"string",
                    "images_url":"http://url/kw_api/integration/image/product.image/42/image_1920/",
                    "product_variant_ids":[
                       {
                          "id":0,
                          "name":"0",
                          "price":0.0,
                          "price_extra":0.0,
                          "url":"http://url/kw_api/integration/image/product.image/50/image_1920/"
                       }
                    ],
                    "currency_id":0,
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":42,
              "number":0,
              "last":false
           }
        }


Отримання шаблону продукту за id номером
--------------------------------------------------

.. http:get:: /kw_api/integration/product_templates/(int:product_template_id)

    У результаті запиту отримуємо список всіх продуктів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/product_templates/(int:product_template_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/product_templates/(int:product_template_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "id":0,
              "name":"string",
              "can_be_sold":true,
              "description":"string",
              "description_purchase":"string",
              "description_sale":"string",
              "type":"bearer",
              "rental":false,
              "categ_id":null,
              "list_price":0.0,
              "standard_price":0.0,
              "taxes_id":0,
              "sale_ok":true,
              "purchase_ok":true,
              "active":true,
              "color":0,
              "is_product_variant":false,
              "default_code":"string",
              "barcode":"string",
              "images_url":"http://url/kw_api/integration/image/product.image/0/image_1920/",
              "product_variant_ids":[
                 {
                    "id":0,
                    "name":"string",
                    "price":0.0,
                    "price_extra":0.0,
                    "url":"http://url/kw_api/integration/image/product.image/1/image_1920/"
                 }
              ],
              "currency_id":0,
           }
        }


    :query int product_template_id: ідентифікатор шаблона продукту


Отримання списку всіх категорій
--------------------------------------------------

.. http:get:: /kw_api/integration/categories

    У результаті запиту отримуємо списку всіх категорій продукту.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/categories

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/categories'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "content":[
                 {
                    "id":0,
                    "name":"string"
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


Створення списку категорій
--------------------------------------------------

.. http:post:: /kw_api/integration/categories

    У результаті запиту отримуємо списку всіх категорій продукту.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/categories

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/categories'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "categories":[
              {
                 "name":"string"
              }
           ]
        }


    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "content":[
                 {
                    "id":0,
                    "name":"string"
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


    :>json string name: назва категорії


Редагування категорії товару за id
--------------------------------------------------

.. http:post:: /kw_api/integration/categories/(int:product_category_id)

    У результаті запиту редагуємо категорію за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/categories/(int:product_category_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/categories/(int:product_category_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
          {
             "name":"string"
          }
        }


    **Example response**:

    .. sourcecode:: json

        {
           "result":{
             {
                "id":0,
                "name":"string"
             }
           }
        }

    :>json string name: назва категорії
    :query int product_category_id: ідентифікатор категоріï продукту


Створення продуктів
--------------------------------------------------

.. http:post:: /kw_api/integration/products

    У результаті запиту створюємо продукти.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/products

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/products'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "products":[
              {
                 "name":"string",
                 "sale_ok":false,
                 "description":"string",
                 "description_purchase":"string",
                 "description_sale":"string",
                 "type":"product",
                 "rental":false,
                 "categ_id":1,
                 "list_price":0.0,
                 "standard_price":0.0,
                 "price_extra":0.0,
                 "taxes_id":1,
                 "purchase_ok":false,
                 "active":true,
                 "color":0,
                 "is_product_variant":true,
                 "default_code":"string",
                 "barcode":"string",
                 "image_url":"https://examples-url.jpg",
                 "currency_id":0
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

    :>json string name: назва продукту*
    :>json boolean sale_ok: флаг товару що продається/не продається
    :>json string description: опис товару
    :>json string description_purchase: опис товару покупки
    :>json string description_sale: опис товару продажу
    :>json string type: тип товару, ``consu`` - витратний матеріал, ``service`` - сервіс, ``product`` - продукт*
    :>json boolean rental: флаг товару можливо здати в оренду
    :>json int categ_id: категорія продукту (GET /kw_api/integration/categories)*
    :>json float list_price: основна ціна товару
    :>json float standard_price: стандартна ціна товару
    :>json float price_extra: націнка конкретного варіанта товару
    :>json int taxes_id:  ідентифікатор податку
    :>json boolean purchase_ok: флаг товару що купується/не купується
    :>json boolean active:  флаг активного товару/товару в архіві*
    :>json boolean is_product_variant: флаг товару що є варіантом/не є варіантом шаблона товару
    :>json string default_code: код товару
    :>json string barcode: унікальний код товару
    :>json string image_url: url картинки товару
    :>json int currency_id: ідентифікатор валюти оплати


Редагування продукту за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/products/(int:product_id)

    У результаті запиту редагуємо продукт.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/products/(int:product_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/products/(int:product_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
             "name":"string",
             "sale_ok":false,
             "description":"string",
             "description_purchase":"string",
             "description_sale":"string",
             "type":"product",
             "rental":false,
             "categ_id":1,
             "list_price":0.0,
             "standard_price":0.0,
             "price_extra":0.0,
             "taxes_id":1,
             "purchase_ok":false,
             "active":true,
             "color":0,
             "is_product_variant":true,
             "default_code":"string",
             "barcode":"string",
             "image_url":"https://examples-url.jpg",
             "currency_id":0
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


Створення варіанта продукту до певного шаблона за id номером шаблона
--------------------------------------------------

.. http:post:: /kw_api/integration/product_templates/(int:product_template_id)

    У результаті запиту створюємо продукти який є варіантом  шаблона за id номером шаблона.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/product_templates/(int:product_template_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/product_templates/(int:product_template_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
             "name":"string",
             "sale_ok":false,
             "description":"string",
             "description_purchase":"string",
             "description_sale":"string",
             "type":"product",
             "rental":false,
             "categ_id":1,
             "list_price":0.0,
             "standard_price":0.0,
             "price_extra":0.0,
             "taxes_id":1,
             "purchase_ok":false,
             "active":true,
             "color":0,
             "is_product_variant":true,
             "default_code":"string",
             "barcode":"string",
             "image_url":"https://examples-url.jpg",
             "currency_id":0
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
                 "images_url":"http://url/kw_api/integration/image/product.image/0/image_1920/",
                 "currency_id":0
              }
           ]
        }

    **Обов'язкові поля відмічені '*'**

    :>json string name: назва продукту'*'
    :>json boolean sale_ok: флаг товару що продається/не продається
    :>json string description: опис товару
    :>json string description_purchase: опис товару покупки
    :>json string description_sale: опис товару продажу
    :>json string type: тип товару, ``consu`` - витратний матеріал, ``service`` - сервіс, ``product`` - продукт*
    :>json boolean rental: флаг товару можливо здати в оренду
    :>json int categ_id: категорія продукту (GET /kw_api/integration/categories)'*'
    :>json float list_price: основна ціна товару
    :>json float standard_price: стандартна ціна товару
    :>json float price_extra: націнка конкретного варіанта товару
    :>json int taxes_id:  ідентифікатор податку
    :>json boolean purchase_ok: флаг товару що купується/не купується
    :>json boolean active:  флаг активного товару/товару в архіві'*'
    :>json boolean is_product_variant: флаг товару що є варіантом/не є варіантом шаблона товару
    :>json string default_code: код товару
    :>json string barcode: унікальний код товару
    :>json string image_url: url картинки товару
    :>json int currency_id: ідентифікатор валюти оплати
    :query int product_template_id: ідентифікатор категоріï продукту


Видалення продукту за id номером
--------------------------------------------------

.. http:delete:: /kw_api/integration/products/(int:product_id)

    У результаті запиту продукту за id номером буде заархівовано.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X DELETE \
                -H "Content-Type: application/json" \
                http://localhost/kw_api/integration/products/(int:product_id)

        .. code-tab:: python

            import requests
            URL = 'http://localhost/kw_api/integration/product_templates/(int:product_template_id)'
            response = requests.delete(URL)
            print(response.json())


    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "200":"Success"
           }
        }


    :statuscode 404: Product not found
    :query int product_id: url параметр ідентифікатор продукту
