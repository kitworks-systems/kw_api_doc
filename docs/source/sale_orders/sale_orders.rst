Продажі
================

Отримання списку всіх продажів
------------------
.. http:get:: /kw_api/integration/sales

    У результаті запиту отримуємо списку всіх продажів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/sales

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/sales'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":[
              {
                 "id":1,
                 "name":"string",
                 "state":"bearer",
                 "user_id":0,
                 "partner_id":0,
                 "partner_name":"string",
                 "partner_phone":"(000)-000-0000",
                 "partner_email":"example@example.com",
                 "partner_invoice_id":0,
                 "partner_shipping_id":0,
                 "sale_order_template_id":0,
                 "validity_date":"2000-00-01",
                 "date_order":"2000-00-01T00:00:00",
                 "payment_term_id":0,
                 "commitment_date":"2000-00-01T00:00:00",
                 "client_order_ref":"string",
                 "amount_untaxed":0.0,
                 "amount_tax":0.0,
                 "amount_undiscounted":0.0,
                 "amount_total":0.0,
                 "order_line":[
                    {
                       "id":0,
                       "product_id":0,
                       "image":"http://url/kw_api/integration/image/product.image/0/image_1920/",
                       "name":"string",
                       "display_name":"string",
                       "default_code":"string",
                       "price_unit":0,
                       "quantity":0
                    },
                    {
                       "id":1,
                       "product_id":1,
                       "image":"http://url/kw_api/integration/image/product.image/0/image_1920/",
                       "name":"string",
                       "display_name":"string",
                       "default_code":"string",
                       "price_unit":0,
                       "quantity":0
                    }
                 ],
              "currency_id":1,
              "kw_sale_order_number":"string",
              "kw_website":"string",
              "kw_website_id":1,
              "kw_is_same_billing_shipping":false,
              "kw_shipping_name":"string",
              "kw_shipping_phone":"string",
              "kw_shipping_city":"string",
              "kw_shipping_address":"string",
              "kw_shipping_detail_date":"2021-01-01",
              "kw_discount_code":"string",
              "kw_payment_state":"string",
              "kw_payment_type":"bearer",
              "kw_shipping_type":"bearer",
              "kw_self_point":"string",
              "kw_stage_id":0
              }
           ]
        }


Отримання замовлення на продаж за id номером
------------------
.. http:get:: /kw_api/integration/sales/(int:sale_order_id)

    У результаті запиту отримуємо замовлення на продаж за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/sales/(int:sale_order_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/sales/(int:sale_order_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "id":1,
              "name":"string",
              "state":"bearer",
              "user_id":0,
              "partner_id":0,
              "partner_name":"string",
              "partner_phone":"(000)-000-0000",
              "partner_email":"example@example.com",
              "partner_invoice_id":0,
              "partner_shipping_id":0,
              "sale_order_template_id":0,
              "validity_date":"2000-00-01",
              "date_order":"2000-00-01T00:00:00",
              "payment_term_id":0,
              "commitment_date":"2000-00-01T00:00:00",
              "client_order_ref":"string",
              "amount_untaxed":0.0,
              "amount_tax":0.0,
              "amount_undiscounted":0.0,
              "amount_total":0.0,
              "order_line":[
                 {
                    "id":0,
                    "product_id":0,
                    "image":"http://url/kw_api/integration/image/product.image/0/image_1920/",
                    "name":"string",
                    "display_name":"string",
                    "default_code":"string",
                    "price_unit":0,
                    "quantity":0
                 },
                 {
                    "id":1,
                    "product_id":1,
                    "image":"http://url/kw_api/integration/image/product.image/0/image_1920/",
                    "name":"string",
                    "display_name":"string",
                    "default_code":"string",
                    "price_unit":0,
                    "quantity":0
                 }
              ],
              "currency_id":1,
              "kw_sale_order_number":"string",
              "kw_website":"string",
              "kw_website_id":1,
              "kw_is_same_billing_shipping":false,
              "kw_shipping_name":"string",
              "kw_shipping_phone":"string",
              "kw_shipping_city":"string",
              "kw_shipping_address":"string",
              "kw_shipping_detail_date":"2021-01-01",
              "kw_discount_code":"string",
              "kw_payment_state":"string",
              "kw_payment_type":"bearer",
              "kw_shipping_type":"bearer",
              "kw_self_point":"string",
              "kw_stage_id":0
           }
        }

    :query int sale_order_id: ідентифікатор замовлення

