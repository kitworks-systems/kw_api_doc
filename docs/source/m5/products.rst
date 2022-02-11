Товари
================

Отримання списку всіх продуктів
------------------

.. http:get:: /kw_api/m5/integration/products

    У результаті запиту отримуємо список всіх продуктів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/m5/integration/products

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/products'
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
                "public_categ_ids": [
                    {
                        "id":1,
                        "name": "string",
                    }
                    {
                        "id":2,
                        "name": "string",
                    }
                ],
                "list_price": 0,
                "standard_price": 0,
                "kw_age_id": 0,
                "kw_complexity_id": "string",
                "kw_item_amount_id": 0,
                "kw_packing_size": "string",
                "kw_manufacture_country_id": "Ukraine",
                "kw_target_id": "boy",
                "kw_seo_title": "string",
                "kw_seo_description": "string",
                "kw_seo_keywords": "string",
                "kw_magic_type_ids": [
                    {
                        "id":1,
                        "name": "string",
                    }
                    {
                        "id":2,
                        "name": "string",
                    }
                ],
                "kw_material_type_ids": [
                    {
                        "id":1,
                        "name": "string",
                    }
                    {
                        "id":2,
                        "name": "string",
                    }
                ],
                "kw_progress_ids": [
                    {
                        "id":1,
                        "name": "string",
                    }
                    {
                        "id":2,
                        "name": "string",
                    }
                ],
                "kw_education_ids": [
                    {
                        "id":1,
                        "name": "string",
                    }
                    {
                        "id":2,
                        "name": "string",
                    }
                ],
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


Отримання продукту за id номером
--------------------------------------------------

.. http:get:: /kw_api/m5/integration/products/(int:product_id)/

    У результаті запиту отримуємо продукт за id номером.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/m5/integration/products/(int:product_id)/

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/products/(int:product_id)/'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
          "result": {
            "id": 0,
            "name": "string",
            "sale_ok": true,
            "description": "string",
            "description_purchase": "string",
            "description_sale": "string",
            "type": "string",
            "rental": false,
            "categ_id": 0,
            "public_categ_ids": [
                {
                    "id":1,
                    "name": "string",
                }
                {
                    "id":2,
                    "name": "string",
                }
            ],
            "list_price": 0,
            "standard_price": 8,
            "kw_age_id": 0,
            "kw_complexity_id": "string",
            "kw_item_amount_id": 0,
            "kw_packing_size": "string",
            "kw_manufacture_country_id": "Ukraine",
            "kw_target_id": "boy",
            "kw_seo_title": "string",
            "kw_seo_description": "string",
            "kw_seo_keywords": "string",
            "kw_magic_type_ids": [
                {
                    "id":1,
                    "name": "string",
                }
                {
                    "id":2,
                    "name": "string",
                }
            ],
            "kw_material_type_ids": [
                {
                    "id":1,
                    "name": "string",
                }
                {
                    "id":2,
                    "name": "string",
                }
            ],
            "kw_progress_ids": [
                {
                    "id":1,
                    "name": "string",
                }
                {
                    "id":2,
                    "name": "string",
                }
            ],
            "kw_education_ids": [
                {
                    "id":1,
                    "name": "string",
                }
                {
                    "id":2,
                    "name": "string",
                }
            ],
            "price_extra": 0,
            "taxes_id": 0,
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
        }


    :query int product_id: ідентифікатор продукту


Отримання списку всіх шаблонів продукту
--------------------------------------------------

.. http:get:: /kw_api/m5/integration/product_templates

    У результаті запиту отримуємо список всіх продуктів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/m5/integration/product_templates

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/product_templates'
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
                    "public_categ_ids": [
                        {
                            "id":1,
                            "name": "string",
                        }
                        {
                            "id":2,
                            "name": "string",
                        }
                    ],
                    "list_price":0.0,
                    "standard_price":0.0,
                    "kw_age_id": 0,
                    "kw_complexity_id": "string",
                    "kw_item_amount_id": 0,
                    "kw_packing_size": "string",
                    "kw_manufacture_country_id": "Ukraine",
                    "kw_target_id": "boy",
                    "kw_seo_title": "string",
                    "kw_seo_description": "string",
                    "kw_seo_keywords": "string",
                    "kw_magic_type_ids": [
                        {
                            "id":1,
                            "name": "string",
                        }
                        {
                            "id":2,
                            "name": "string",
                        }
                    ],
                    "kw_material_type_ids": [
                        {
                            "id":1,
                            "name": "string",
                        }
                        {
                            "id":2,
                            "name": "string",
                        }
                    ],
                    "kw_progress_ids": [
                        {
                            "id":1,
                            "name": "string",
                        }
                        {
                            "id":2,
                            "name": "string",
                        }
                    ],
                    "kw_education_ids": [
                        {
                            "id":1,
                            "name": "string",
                        }
                        {
                            "id":2,
                            "name": "string",
                        }
                    ],
                    "price_extra": 0,
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

.. http:get:: /kw_api/m5/integration/product_templates/(int:product_template_id)

    У результаті запиту отримуємо список всіх продуктів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/m5/integration/product_templates/(int:product_template_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/product_templates/(int:product_template_id)'
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
              "categ_id":0,
              "public_categ_ids": [
                    {
                        "id":1,
                        "name": "string",
                    }
                    {
                        "id":2,
                        "name": "string",
                    }
              ],
              "list_price":0.0,
              "standard_price":0.0,
              "kw_age_id": 0,
              "kw_complexity_id": "string",
              "kw_item_amount_id": 0,
              "kw_packing_size": "string",
              "kw_manufacture_country_id": "Ukraine",
              "kw_target_id": "boy",
              "kw_seo_title": "string",
              "kw_seo_description": "string",
              "kw_seo_keywords": "string",
              "kw_magic_type_ids": [
                  {
                      "id":1,
                      "name": "string",
                  }
                  {
                      "id":2,
                      "name": "string",
                  }
              ],
              "kw_material_type_ids": [
                  {
                      "id":1,
                      "name": "string",
                  }
                  {
                      "id":2,
                      "name": "string",
                  }
              ],
              "kw_progress_ids": [
                  {
                      "id":1,
                      "name": "string",
                  }
                  {
                      "id":2,
                      "name": "string",
                  }
              ],
              "kw_education_ids": [
                {
                    "id":1,
                    "name": "string",
                }
                {
                    "id":2,
                    "name": "string",
                }
              ],
              "price_extra": 0,
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


Створення продуктів
--------------------------------------------------

.. http:post:: /kw_api/m5/integration/products

    У результаті запиту створюємо продукти.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/m5/integration/products

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/products'
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
                 "public_categ_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "list_price":0.0,
                 "standard_price":0.0,
                 "kw_age_id": 0,
                 "kw_complexity_id": "string",
                 "kw_item_amount_id": 0,
                 "kw_packing_size": "string",
                 "kw_manufacture_country_id": "Ukraine",
                 "kw_target_id": "boy",
                 "kw_seo_title": "string",
                 "kw_seo_description": "string",
                 "kw_seo_keywords": "string",
                 "kw_magic_type_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_material_type_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_progress_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_education_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
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
                 "categ_id":0,
                 "public_categ_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "list_price":0.0,
                 "standard_price":0.0,
                 "kw_age_id": 0,
                 "kw_complexity_id": "string",
                 "kw_item_amount_id": 0,
                 "kw_packing_size": "string",
                 "kw_manufacture_country_id": "Ukraine",
                 "kw_target_id": "boy",
                 "kw_seo_title": "string",
                 "kw_seo_description": "string",
                 "kw_seo_keywords": "string",
                 "kw_magic_type_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_material_type_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_progress_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_education_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
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
    :>json int public_categ_ids: категорії продукту (GET /kw_api/m5/integration/categories)
    :>json float list_price: основна ціна товару
    :>json float standard_price: стандартна ціна товару
    :>json int kw_age_id: вiк
    :>json string kw_complexity_id: складність
    :>json int kw_item_amount_id: кiлькiсть
    :>json string kw_packing_size: розмiр товару
    :>json string kw_manufacture_country_id: країна виробник
    :>json string kw_target_id: цiльова аудиторiя
    :>json string kw_magic_type_ids: тип магiї
    :>json string kw_material_type_ids: тип матерiалу
    :>json string kw_progress_ids: розвиток
    :>json string kw_education_ids: рiвень освiти
    :>json string kw_seo_title: найменування SEO
    :>json string kw_seo_description: опис SEO
    :>json string kw_seo_keywords: ключовi слова
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

.. http:post:: /kw_api/m5/integration/products/(int:product_id)

    У результаті запиту редагуємо продукт.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/m5/integration/products/(int:product_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/products/(int:product_id)'
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
             "public_categ_ids": [
                {
                    "id":1,
                    "name": "string",
                }
                {
                    "id":2,
                    "name": "string",
                }
             ],
             "list_price":0.0,
             "standard_price":0.0,
             "kw_age_id": 0,
             "kw_complexity_id": "string",
             "kw_item_amount_id": 0,
             "kw_packing_size": "string",
             "kw_manufacture_country_id": "Ukraine",
             "kw_target_id": "boy",
             "kw_seo_title": "string",
             "kw_seo_description": "string",
             "kw_seo_keywords": "string",
             "kw_magic_type_ids": [
                 {
                     "id":1,
                     "name": "string",
                 }
                 {
                     "id":2,
                     "name": "string",
                 }
             ],
             "kw_material_type_ids": [
                 {
                     "id":1,
                     "name": "string",
                 }
                 {
                     "id":2,
                     "name": "string",
                 }
             ],
             "kw_progress_ids": [
                 {
                     "id":1,
                     "name": "string",
                 }
                 {
                     "id":2,
                     "name": "string",
                 }
             ],
             "kw_education_ids": [
                 {
                     "id":1,
                     "name": "string",
                 }
                 {
                     "id":2,
                     "name": "string",
                 }
             ],
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
                 "categ_id":0,
                 "public_categ_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "list_price":0.0,
                 "standard_price":0.0,
                 "kw_age_id": 0,
                 "kw_complexity_id": "string",
                 "kw_item_amount_id": 0,
                 "kw_packing_size": "string",
                 "kw_manufacture_country_id": "Ukraine",
                 "kw_target_id": "boy",
                 "kw_seo_title": "string",
                 "kw_seo_description": "string",
                 "kw_seo_keywords": "string",
                 "kw_magic_type_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_material_type_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_progress_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_education_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
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

.. http:post:: /kw_api/m5/integration/product_templates/(int:product_template_id)

    У результаті запиту створюємо продукти який є варіантом  шаблона за id номером шаблона.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/m5/integration/product_templates/(int:product_template_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/product_templates/(int:product_template_id)'
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
             "public_categ_ids": [
                {
                    "id":1,
                    "name": "string",
                }
                {
                    "id":2,
                    "name": "string",
                }
             ],
             "list_price":0.0,
             "standard_price":0.0,
             "kw_age_id": 0,
             "kw_complexity_id": "string",
             "kw_item_amount_id": 0,
             "kw_packing_size": "string",
             "kw_manufacture_country_id": "Ukraine",
             "kw_target_id": "boy",
             "kw_seo_title": "string",
             "kw_seo_description": "string",
             "kw_seo_keywords": "string",
             "kw_magic_type_ids": [
                 {
                     "id":1,
                     "name": "string",
                 }
                 {
                     "id":2,
                     "name": "string",
                 }
             ],
             "kw_material_type_ids": [
                 {
                     "id":1,
                     "name": "string",
                 }
                 {
                     "id":2,
                     "name": "string",
                 }
             ],
             "kw_progress_ids": [
                 {
                     "id":1,
                     "name": "string",
                 }
                 {
                     "id":2,
                     "name": "string",
                 }
             ],
             "kw_education_ids": [
                 {
                     "id":1,
                     "name": "string",
                 }
                 {
                     "id":2,
                     "name": "string",
                 }
             ],
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
                 "categ_id":0,
                 "public_categ_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "list_price":0.0,
                 "standard_price":0.0,
                 "kw_age_id": 0,
                 "kw_complexity_id": "string",
                 "kw_item_amount_id": 0,
                 "kw_packing_size": "string",
                 "kw_manufacture_country_id": "Ukraine",
                 "kw_target_id": "boy",
                 "kw_seo_title": "string",
                 "kw_seo_description": "string",
                 "kw_seo_keywords": "string",
                 "kw_magic_type_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_material_type_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_progress_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
                 "kw_education_ids": [
                     {
                         "id":1,
                         "name": "string",
                     }
                     {
                         "id":2,
                         "name": "string",
                     }
                 ],
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
    :>json int public_categ_ids: категорії продукту (GET /kw_api/m5/integration/categories)
    :>json float list_price: основна ціна товару
    :>json float standard_price: стандартна ціна товару
    :>json int kw_age_id: вiк
    :>json string kw_complexity_id: складність
    :>json int kw_item_amount_id: кiлькiсть
    :>json string kw_packing_size: розмiр товару
    :>json string kw_manufacture_country_id: країна виробник
    :>json string kw_target_id: цiльова аудиторiя
    :>json string kw_magic_type_ids: тип магiї
    :>json string kw_material_type_ids: тип матерiалу
    :>json string kw_progress_ids: розвиток
    :>json string kw_education_ids: рiвень освiти
    :>json string kw_seo_title: найменування SEO
    :>json string kw_seo_description: опис SEO
    :>json string kw_seo_keywords: ключовi слова
    :>json float price_extra: націнка конкретного варіанта товару
    :>json int taxes_id:  ідентифікатор податку
    :>json boolean purchase_ok: флаг товару що купується/не купується
    :>json boolean active:  флаг активного товару/товару в архіві'*'
    :>json boolean is_product_variant: флаг товару що є варіантом/не є варіантом шаблона товару
    :>json string default_code: код товару
    :>json string barcode: унікальний код товару
    :>json string image_url: url картинки товару
    :>json int currency_id: ідентифікатор валюти оплати
    :query int product_template_id: ідентифікатор продукту


Видалення продукту за id номером
--------------------------------------------------

.. http:delete:: /kw_api/m5/integration/products/(int:product_id)

    У результаті запиту продукту за id номером буде заархівовано.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X DELETE \
                -H "Content-Type: application/json" \
                http://localhost/kw_api/m5/integration/products/(int:product_id)

        .. code-tab:: python

            import requests
            URL = 'http://localhost/kw_api/m5/integration/product_templates/(int:product_template_id)'
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


Отримання списку всіх категорій
--------------------------------------------------

.. http:get:: /kw_api/m5/integration/categories

    У результаті запиту отримуємо списку всіх категорій продукту.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/m5/integration/categories

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/categories'
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
                    "parent_id":0,
                    "sequence":10000,
                    "images_url":"http://url/kw_api/integration/image/product.image/0/image_1920/"
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

.. http:post:: /kw_api/m5/integration/categories

    У результаті запиту отримуємо список всіх категорій продукту.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/m5/integration/categories

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/categories'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "categories":[
              {
                 "name":"string",
                 "parent_id":0,
                 "sequence":10000,
                 "images_url":"https://examples-url.jpg"
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
                    "name":"string",
                    "parent_id":0,
                    "sequence":10000,
                    "images_url":"https://examples-url.jpg"
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
    :>json int parent_id: батьківський ідентифікатор категорії
    :>json int sequence: послідовність
    :>json string images_url: url картинки категорiї

Редагування категорії товару за id
--------------------------------------------------

.. http:post:: /kw_api/m5/integration/categories/(int:product_category_id)

    У результаті запиту редагуємо категорію за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/m5/integration/categories/(int:product_category_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/m5/integration/categories/(int:product_category_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
          {
              "name":"string",
              "parent_id":0,
              "sequence":10000,
              "images_url":"https://examples-url.jpg"
          }
        }


    **Example response**:

    .. sourcecode:: json

        {
           "result":{
             {
                "id":0,
                "name":"string",
                "parent_id":0,
                "sequence":10000,
                "images_url":"https://examples-url.jpg"
             }
           }
        }

    **Обов'язкові поля відмічені '*'**

    :>json string name: назва категорії'*'
    :>json int parent_id: батьківський ідентифікатор категорії
    :>json int sequence: послідовність
    :>json string images_url: url картинки категорiї
    :query int product_template_id: ідентифікатор категоріï продукту