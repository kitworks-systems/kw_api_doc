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
            "list_price": 0,
            "standard_price": 8,
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

GET /kw_api/integration/product_templates

У результаті запиту отримуємо списку всіх продуктів.

Parameters

Request body

Responses

200 - Successful Response

.. code-block:: json

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

