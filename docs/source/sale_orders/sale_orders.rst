Продажі
================

Отримання списку всіх продажів
------------------
.. http:get:: /kw_api/integration/sales

    У результаті запиту отримуємо списку всіх продажів.
    
    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)
    
    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/sales 

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/sales'
            response = requests.get(URL, headers=headers)
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
              "source": {
                  "id": 0,
                  "name": "string",
              },
              "medium": {
                  "id": 0,
                  "name": "string",
              },
              "campaign": {
                  "id": 0,
                  "name": "string",
              },
              "carrier_id": 4,
              "kw_sale_order_number":"string",
              "kw_website":"string",
              "kw_website_id":1,
              "kw_is_same_billing_shipping":false,
              "kw_shipping_name":"string",
              "kw_shipping_phone":"string",
              "kw_shipping_city":"string",
              "kw_shipping_address":"string",
              "kw_shipping_house": "string",
              "kw_shipping_flat": "string",
              "kw_shipping_detail_date": "2021-12-16",
              "kw_discount_code":"string",
              "kw_payment_state":"string",
              "kw_payment_type":"string",
              "kw_shipping_type":"string",
              "kw_self_point":"string",
              "kw_stage_id":0
              "kw_car_service_id": "string",
              "kw_np_service_type": "string",
              "kw_np_payer_type": "string",
              "kw_np_cargo_type": "string",
              "kw_np_delivery_weight": 2,
              "kw_np_delivery_volume": 0,
              "kw_np_delivery_so_cost": 1000,
              "kw_time_slot_id":1
              }
           ]
        }


Отримання замовлення на продаж за id номером
------------------
.. http:get:: /kw_api/integration/sales/(int:sale_order_id)

    У результаті запиту отримуємо замовлення на продаж за id номером.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/sales/(int:sale_order_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/sales/(int:sale_order_id)'
            response = requests.get(URL, headers=headers)
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
              "carrier_id": 4,
              "kw_sale_order_number":"string",
              "kw_website":"string",
              "kw_website_id":1,
              "kw_is_same_billing_shipping":false,
              "kw_shipping_name":"string",
              "kw_shipping_phone":"string",
              "kw_shipping_city":"string",
              "kw_shipping_address":"string",
              "kw_shipping_house": "string",
              "kw_shipping_flat": "string",
              "kw_shipping_detail_date": "2021-12-16",
              "kw_discount_code":"string",
              "kw_payment_state":"string",
              "kw_payment_type":"string",
              "kw_shipping_type":"string",
              "kw_self_point":"string",
              "kw_stage_id":0
              "kw_car_service_id": "string",
              "kw_np_service_type": "string",
              "kw_np_payer_type": "string",
              "kw_np_cargo_type": "string",
              "kw_np_delivery_weight": 2,
              "kw_np_delivery_volume": 0,
              "kw_np_delivery_so_cost": 1000,
              "kw_time_slot_id":1
           }
        }

    :query int sale_order_id: ідентифікатор замовлення


Зміна продавця в замовлення на продаж за id номером
------------------
.. http:get::  /kw_api/integration/sales/(int:sale_order_id)/salesperson/(int:user_id)

    У результаті запиту отримуємо списку всіх продажів.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/sales/(int:sale_order_id)/salesperson/(int:user_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/sales/(int:sale_order_id)/salesperson/(int:user_id)'
            response = requests.get(URL, headers=headers)
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
              "carrier_id": 4,
              "kw_sale_order_number":"string",
              "kw_website":"string",
              "kw_website_id":1,
              "kw_is_same_billing_shipping":false,
              "kw_shipping_name":"string",
              "kw_shipping_phone":"string",
              "kw_shipping_city":"string",
              "kw_shipping_address":"string",
              "kw_shipping_house": "string",
              "kw_shipping_flat": "string",
              "kw_shipping_detail_date": "2021-12-16",
              "kw_discount_code":"string",
              "kw_payment_state":"string",
              "kw_payment_type":"string",
              "kw_shipping_type":"string",
              "kw_self_point":"string",
              "kw_stage_id":0
              "kw_car_service_id": "string",
              "kw_np_service_type": "string",
              "kw_np_payer_type": "string",
              "kw_np_cargo_type": "string",
              "kw_np_delivery_weight": 2,
              "kw_np_delivery_volume": 0,
              "kw_np_delivery_so_cost": 1000,
              "kw_time_slot_id":1
           }
        }


    :query int sale_order_id: ідентифікатор замовлення
    :query int user_id: ідентифікатор користувача


Створення замовлення на продаж
------------------
.. http:post:: /kw_api/integration/sales

    У результаті запиту створюємо замовлення на продаж.

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
                http://localhost/kw_api/integration/sales

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/sales'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "orders":[
              {
                 "state":"bearer",
                 "user_id":0,
                 "partner_id":0,
                 "partner_name":"string",
                 "partner_phone":"0000000000",
                 "partner_email":"example@example.com",
                 "validity_date":"2000-01-01",
                 "date_order":"2000-01-01 00:00:00",
                 "payment_term_id":1,
                 "commitment_date":"2000-01-01 00:00:00",
                 "client_order_ref":"string",
                 "order_line":[
                    {
                       "name":"string",
                       "product_id":0,
                       "price_unit":0,
                       "product_uom_qty":0.0
                    },
                    {
                       "name":"string",
                       "product_id":1,
                       "price_unit":0,
                       "product_uom_qty":0.0
                    }
                 ],
              "currency_id":1,
              "carrier_id": 4,
              "kw_sale_order_number":"string",
              "kw_website":"string",
              "kw_website_id":1,
              "kw_is_same_billing_shipping":false,
              "kw_shipping_name":"string",
              "kw_shipping_phone":"string",
              "kw_shipping_city":"string",
              "kw_shipping_address":"string",
              "kw_shipping_house": "string",
              "kw_shipping_flat": "string",
              "kw_shipping_detail_date": "2021-12-16",
              "kw_discount_code":"string",
              "kw_payment_state":"string",
              "kw_payment_type":"string",
              "kw_shipping_type":"string",
              "kw_self_point":"string",
              "kw_stage_id":0
              "kw_car_service_id": "string",
              "kw_np_service_type": "string",
              "kw_np_payer_type": "string",
              "kw_np_cargo_type": "string",
              "kw_np_delivery_weight": 2,
              "kw_np_delivery_volume": 0,
              "kw_np_delivery_so_cost": 1000,
              "kw_time_slot_id":1
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
                    "id": 0,
                    "name": "string",
                    "state":"bearer",
                    "user_id":1,
                    "partner_id": 1,
                    "partner_name": "string",
                    "partner_phone": "(000)-000-0000",
                    "partner_email": "example@example.com",
                    "partner_invoice_id": 1,
                    "partner_shipping_id": 1,
                    "sale_order_template_id": 1,
                    "validity_date": "2000-01-01",
                    "date_order": "2000-01-01 00:00:00",
                    "payment_term_id": 1,
                    "commitment_date": "2000-01-01 00:00:00",
                    "client_order_ref": "string",
                    "amount_untaxed": 0.0,
                    "amount_tax": null,
                    "amount_undiscounted": 0.0,
                    "amount_total": 0.0,
                    "order_line": [
                        {
                            "id": 0,
                            "product_id": 0,
                            "image": "http://url/kw_api/integration/image/product.image/0/image_1920/",
                            "name": "string",
                            "display_name": "string",
                            "default_code": null,
                           "price_unit":0,
                           "quantity":0
                        },
                        {
                            "id": 1,
                            "product_id": 1,
                            "image": "http://url/kw_api/integration/image/product.image/0/image_1920/",
                            "name": "string",
                            "display_name": "string",
                            "default_code": null,
                           "price_unit":0,
                           "quantity":0
                        }
                    ],
              "currency_id":1,
              "carrier_id": 4,
              "kw_sale_order_number":"string",
              "kw_website":"string",
              "kw_website_id":1,
              "kw_is_same_billing_shipping":false,
              "kw_shipping_name":"string",
              "kw_shipping_phone":"string",
              "kw_shipping_city":"string",
              "kw_shipping_address":"string",
              "kw_shipping_house": "string",
              "kw_shipping_flat": "string",
              "kw_shipping_detail_date": "2021-12-16",
              "kw_discount_code":"string",
              "kw_payment_state":"string",
              "kw_payment_type":"string",
              "kw_shipping_type":"string",
              "kw_self_point":"string",
              "kw_stage_id":0
              "kw_car_service_id": "string",
              "kw_np_service_type": "string",
              "kw_np_payer_type": "string",
              "kw_np_cargo_type": "string",
              "kw_np_delivery_weight": 2,
              "kw_np_delivery_volume": 0,
              "kw_np_delivery_so_cost": 1000,
              "kw_time_slot_id":1
                }
            ]
        }


    **Обов'язкові поля відмічені '*'**
    
    **Для створення доставки необхідно обов'язково переслати поле "carrier_id"**

    :>json string state: статус замовлення (``draft``, ``sale``, ``sent``, ``done``, ``cancel``)*
    :>json int user_id: порядковий номер
    :>json int partner_id: ідентифікатор партнера
    :>json string partner_name:  ім’я партнера *
    :>json sring partner_phone:  телефон партнера *
    :>json sring partner_email: почта партнера *
    :>json int partner_invoice_id: ідентифікатор партнера рахунок-фактури
    :>json int partner_shipping_id: ідентифікатор партнера доставки
    :>json int sale_order_template_id: ідентифікатор шаблону замовлення на продаж
    :>json string validity_date: дата валідації ( формат - ``%Y-%m-%d``)
    :>json string date_order: дата замолення ( формат - ``%Y-%m-%d %H:%M:%S``)
    :>json int payment_term_id: ідентифікатор терміну оплати
    :>json string commitment_date: дата підтвердження ( формат - ``%Y-%m-%d %H:%M:%S``)
    :>json string client_order_ref: коментар клієнта до замовлення
    :>json int product_id: ідентифікатор продукту *
    :>json string name: ім’я продукту
    :>json int product_uom_qty: кількість продукту
    :>json float price_unit: ціна продукту
    :>json int currency_id: ідентифікатор валюти оплати
    :>json string kw_sale_order_number: номер заказу з сайту
    :>json string kw_website: сайт заказу
    :>json int kw_website_id: індекс вебсайту
    :>json boolean kw_is_same_billing_shipping: флаг чи однаковий одержувач і замовник
    :>json string kw_shipping_name: ім’я одержувача
    :>json string kw_shipping_phone: телефон одержувача
    :>json string kw_shipping_city: місто одержувача
    :>json string kw_shipping_address: адреса одержувача
    :>json string kw_shipping_house: будинок одержувача
    :>json string kw_shipping_flat: квартира одержувача
    :>json string kw_shipping_detail_date: дата доставки
    :>json string kw_discount_code: код знижки
    :>json string kw_payment_state: статус оплати (``not_paid``, ``waiting_for_prepayment``, ``partially_paid``, ``paid``)
    :>json string kw_payment_type: тип оплати (``on_delivery``, ``card``)
    :>json string kw_delivery_price: сума доставки
    :>json string kw_shipping_type: тип доставки (``self``, ``courier``)
    :>json string kw_sefl_point: адреса самовивозу
    :>json int kw_stage_id: ідентифікатор веб статуса


Створення замовлення на продаж з доставкою НП
------------------
.. http:post:: /kw_api/integration/sales

    У результаті запиту створюємо замовлення на продаж з доставкою Новою Поштою. Це розширення дійсне при  встановленому модулі kw_np_api_sale.

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
                http://localhost/kw_api/integration/sales

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/sales'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    Тіло запиту має містити: The content of body.json is like:

    .. code-block:: json

        {
            "orders": [
                {
                    "date_order": "2000-01-01 00:00:00",
                    "partner_name": <string>,
                    "partner_phone": <string>,
                    "order_line": [
                        {
                            "product_id": <int>
                        }
                        ],
                    "carrier_id": <int>,
                    "kw_shipping_name": <string>,
                    "kw_shipping_phone": <string>,
                    "kw_shipping_city": <string>,
                    "kw_shipping_address": <string>,
                    "kw_np_service_type": <string>,
                    "kw_np_payer_type": <string>
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
                    "id": <int>,
                    "name": <string>,
                    "state":<tring>,
                    "user_id":<int>,
                    "partner_id": <int>,
                    "partner_name": <string>,
                    "partner_phone": <string>,
                    "partner_email": <string>,
                    "partner_invoice_id": <int>,
                    "partner_shipping_id": <int>,
                    "validity_date": "2000-01-01",
                    "date_order": "2000-01-01 00:00:00",
                    "payment_term_id": <int>,
                    "commitment_date": "2000-01-01 00:00:00",
                    "client_order_ref": "string",
                    "amount_untaxed": <float>,
                    "amount_tax": null,
                    "amount_undiscounted": <float>,
                    "amount_total": <float>,
                    "order_line": [
                        {
                            "id": <int>,
                            "product_id": <int>,
                            "image": "http://url/kw_api/integration/image/product.image/0/image_1920/",
                            "name": <string>,
                            "display_name": <string>,
                            "default_code": null,
                            "price_unit":0,
                            "product_uom_qty": <int>
                        },
                        ],
                    "currency_id": <int>,
                    "carrier_id": <int>,
                    "kw_sale_order_number": <string>,
                    "kw_website": <string>,
                    "kw_website_id": <int>,
                    "kw_is_same_billing_shipping": <bool>,
                    "kw_shipping_name": <string>,
                    "kw_shipping_phone": <string>,
                    "kw_shipping_city": <string>,
                    "kw_shipping_address": <string>,
                    "kw_shipping_house": <string>,
                    "kw_shipping_flat": <string>,
                    "kw_shipping_detail_date": "2000-01-01",
                    "kw_discount_code": <string>,
                    "kw_payment_type": <string>,
                    "kw_delivery_price": <float>,
                    "kw_payment_state": <string>,
                    "kw_shipping_type": <string>,
                    "kw_self_point": <string>,
                    "kw_np_recipient_type": <string>,
                    "kw_np_service_type": <string>,
                    "kw_np_payer_type": <string>,
                    "kw_np_payment_form": <string>,
                    "kw_np_cargo_type": <string>,
                    "kw_np_delivery_weight": <float>,
                    "kw_np_delivery_volume": <float>,
                    "kw_np_delivery_so_cost": <int>
                }
            ]
        }


    **Обов'язкові поля відмічені '*'**

    :>json string state: статус замовлення (``draft``, ``sale``, ``sent``, ``done``, ``cancel``)
    :>json int user_id: продавець
    :>json int partner_id: ідентифікатор партнера (або partner_name та partner_phone)
    :>json string partner_name:  ім’я партнера *
    :>json sring partner_phone:  телефон партнера *
    :>json sring partner_email: пошта партнера
    :>json string validity_date: дійсний до ( формат - ``%Y-%m-%d``)
    :>json string date_order: дата замовлення ( формат - ``%Y-%m-%d %H:%M:%S``) *
    :>json int payment_term_id: ідентифікатор терміну оплати
    :>json string commitment_date: дата підтвердження ( формат - ``%Y-%m-%d %H:%M:%S``)
    :>json string client_order_ref: коментар клієнта до замовлення
    :>json int product_id: ідентифікатор продукту *
    :>json string name: ім’я продукту
    :>json int product_uom_qty: кількість продукту
    :>json float price_unit: ціна продукту
    :>json int currency_id: ідентифікатор валюти оплати
    :>json string kw_sale_order_number: номер заказу з сайту
    :>json string kw_website: сайт заказу
    :>json int kw_website_id: індекс вебсайту
    :>json boolean kw_is_same_billing_shipping: флаг чи однаковий одержувач і замовник
    :>json boolean carrier_id: спосіб доставки *
    :>json string kw_shipping_name: ім’я одержувача (має містити Ім'я та прізвище українською мовою) *
    :>json string kw_shipping_phone: телефон одержувача (формат - ``38000000000``) *
    :>json string kw_shipping_city: місто одержувача *
    :>json string kw_shipping_address: адреса одержувача, для НП - відділення в форматі name або ref (Бізнес-відділення №373: вул. Каунаська, 27 / 50daf85a-0ac5-11e5-8a92-005056887b8d) *
    :>json string kw_shipping_house: будинок одержувача, для НП теж
    :>json string kw_shipping_flat: квартира одержувача, для НП теж
    :>json string kw_discount_code: код знижки
    :>json string kw_payment_type: тип оплати (``on_delivery``, ``card``)
    :>json int kw_np_payment_form_id: метод оплати для НП. ``1`` (Безготівковий), ``2``(Готівка)
    :>json int kw_stage_id: ідентифікатор веб статуса
    :>json int kw_np_service_type: тип доставки НП, в форматі name або ref (Адреса-Відділення/DoorsWarehouse) (``Адреса-Адреса``, ``Адреса-Відділення``, ``Відділення-Відділення``, ``Відділення-Адреса``, ``Адреса-Поштомат``, ``Відділення-Поштомат``) *
    :>json int kw_np_payer_type: тип платника доставки НП, в форматі name/ref ( Одержувач/Recipient) (``Відправник``, ``Одержувач``, ``Третя особа``) -*
    :>json string kw_np_cargo_type: тип вантажу (``Посилка``, ``Вантаж``, ``Документи``, ``Шини-диски``, ``Палети``)
    :>json string kw_np_additional_info:
    :>json string kw_np_preferred_delivery_date: бажана дата доставки (формат - ``%Y-%m-%d %H:%M:%S``)

Створення замовлення на продаж
------------------
.. http:post:: /kw_api/integration/sales/(int:sale_order_id)

    У результаті запиту створюємо замовлення на продаж.

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
                http://localhost/kw_api/integration/sales/(int:sale_order_id)/salesperson/(int:user_id)

        .. code-tab:: python
            
            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/sales/(int:sale_order_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "state":"bearer",
           "user_id":0,
           "partner_id":0,
           "partner_name":"string",
           "partner_phone":"0000000000",
           "partner_email":"example@example.com",
           "validity_date":"2000-01-01",
           "date_order":"2000-01-01 00:00:00",
           "payment_term_id":1,
           "commitment_date":"2000-01-01 00:00:00",
           "client_order_ref":"string",
           "order_line":[
              {
                 "name":"string",
                 "product_id":0,
                 "price_unit":0,
                 "product_uom_qty":0.0
              },
              {
                 "name":"string",
                 "product_id":1,
                 "price_unit":0,
                 "product_uom_qty":0.0
              }
           ],
           "currency_id":1,
           "carrier_id": 4,
           "kw_sale_order_number":"string",
           "kw_website":"string",
           "kw_website_id":1,
           "kw_is_same_billing_shipping":false,
           "kw_shipping_name":"string",
           "kw_shipping_phone":"string",
           "kw_shipping_city":"string",
           "kw_shipping_address":"string",
           "kw_shipping_house": "string",
           "kw_shipping_flat": "string",
           "kw_shipping_detail_date": "2021-12-16",
           "kw_discount_code":"string",
           "kw_payment_state":"string",
           "kw_payment_type":"string",
           "kw_shipping_type":"string",
           "kw_self_point":"string",
           "kw_stage_id":0
           "kw_car_service_id": 1,
           "kw_np_service_type": "string",
           "kw_np_payer_type": "string",
           "kw_np_cargo_type": "string",
           "kw_np_delivery_weight": 2,
           "kw_np_delivery_volume": 0,
           "kw_np_delivery_so_cost": 1000,
           "kw_time_slot_id":1
        }




    **Example response**:

    .. sourcecode:: json

        {
           "jsonrpc":"2.0",
           "id":null,
           "result":{
              "id":0,
              "name":"string",
              "state":"bearer",
              "user_id":1,
              "partner_id":1,
              "partner_name":"string",
              "partner_phone":"(000)-000-0000",
              "partner_email":"example@example.com",
              "partner_invoice_id":1,
              "partner_shipping_id":1,
              "sale_order_template_id":1,
              "validity_date":"2000-01-01",
              "date_order":"2000-01-01 00:00:00",
              "payment_term_id":1,
              "commitment_date":"2000-01-01 00:00:00",
              "client_order_ref":"string",
              "amount_untaxed":0.0,
              "amount_tax":null,
              "amount_undiscounted":0.0,
              "amount_total":0.0,
              "order_line":[
                 {
                    "id":0,
                    "product_id":0,
                    "image":"http://url/kw_api/integration/image/product.image/0/image_1920/",
                    "name":"string",
                    "display_name":"string",
                    "default_code":null,
                    "price_unit":0,
                    "quantity":0
                 },
                 {
                    "id":1,
                    "product_id":1,
                    "image":"http://url/kw_api/integration/image/product.image/0/image_1920/",
                    "name":"string",
                    "display_name":"string",
                    "default_code":null,
                    "price_unit":0,
                    "quantity":0
                 }
              }
           ],
           "currency_id":1,
           "carrier_id": 4,
           "kw_sale_order_number":"string",
           "kw_website":"string",
           "kw_website_id":1,
           "kw_is_same_billing_shipping":false,
           "kw_shipping_name":"string",
           "kw_shipping_phone":"string",
           "kw_shipping_city":"string",
           "kw_shipping_address":"string",
           "kw_shipping_house": "string",
           "kw_shipping_flat": "string",
           "kw_shipping_detail_date": "2021-12-16",
           "kw_discount_code":"string",
           "kw_payment_state":"string",
           "kw_payment_type":"string",
           "kw_shipping_type":"string",
           "kw_self_point":"string",
           "kw_stage_id":0
           "kw_car_service_id": 1,
           "kw_np_service_type": "string",
           "kw_np_payer_type": "string",
           "kw_np_cargo_type": "string",
           "kw_np_delivery_weight": 2,
           "kw_np_delivery_volume": 0,
           "kw_np_delivery_so_cost": 1000,
           "kw_time_slot_id":1
        }



    **Обов'язкові поля відмічені '*'**
    
    **Для оновлення доставки необхідно обов'язково переслати поле "carrier_id"**

    :>json string state: статус замовлення (``draft``, ``sale``, ``sent``, ``done``, ``cancel``)*
    :>json int user_id: порядковий номер
    :>json int partner_id: ідентифікатор партнера
    :>json string partner_name:  ім’я партнера *
    :>json sring partner_phone:  телефон партнера *
    :>json sring partner_email: почта партнера *
    :>json int partner_invoice_id: ідентифікатор партнера рахунок-фактури
    :>json int partner_shipping_id: ідентифікатор партнера доставки
    :>json int sale_order_template_id: ідентифікатор шаблону замовлення на продаж
    :>json string validity_date: дата валідації ( формат - ``%Y-%m-%d``)
    :>json string date_order: дата замолення ( формат - ``%Y-%m-%d %H:%M:%S``)
    :>json int payment_term_id: ідентифікатор терміну оплати
    :>json string commitment_date: дата підтвердження ( формат - ``%Y-%m-%d %H:%M:%S``)
    :>json string client_order_ref: коментар клієнта до замовлення
    :>json int product_id: ідентифікатор продукту *
    :>json string name: ім’я продукту
    :>json int product_uom_qty: кількість продукту
    :>json float price_unit: ціна продукту
    :>json int currency_id: ідентифікатор валюти оплати
    :>json string kw_sale_order_number: номер заказу з сайту
    :>json string kw_website: сайт заказу
    :>json int kw_website_id: індекс вебсайту
    :>json boolean kw_is_same_billing_shipping: флаг чи однаковий одержувач і замовник
    :>json string kw_shipping_name: ім’я одержувача
    :>json string kw_shipping_phone: телефон одержувача
    :>json string kw_shipping_city: місто одержувача, для НП - місто в форматі name/ref (Київ/8d5a980d-391c-11dd-90d9-001a92567626)
    :>json string kw_shipping_address: адреса одержувача, для НП - відділення в форматі name/ref (Пункт приймання-видачі (до 30 кг): вул. Білоуська, 17/e6627e75-de7e-11e9-b48a-005056b24375)
    :>json string kw_shipping_house: будинок одержувача, для НП теж
    :>json string kw_shipping_flat: квартира одержувача, для НП теж
    :>json string kw_shipping_detail_date: дата доставки
    :>json string kw_discount_code: код знижки
    :>json string kw_payment_state: статус оплати (``not_paid``, ``waiting_for_prepayment``, ``partially_paid``, ``paid``)
    :>json string kw_payment_type: тип оплати (``on_delivery``, ``card``)
    :>json string kw_delivery_price: сума доставки
    :>json string kw_shipping_type: тип доставки (``self``, ``courier``)
    :>json string kw_sefl_point: адреса самовивозу
    :>json int kw_stage_id: ідентифікатор веб статуса
    :>json int kw_np_service_type: тип доставки НП, в форматі name/ref (Адреса-Відділення/DoorsWarehouse)
    :>json int kw_np_payer_type: тип платника доставки НП, в форматі name/ref ( Одержувач/Recipient)
    :>json int kw_np_delivery_weight: вага товару НП
    :>json int kw_np_delivery_volume: об’єм вантажа НП
    :>json int kw_np_delivery_so_cost: вартість НП


Видалення замовлення на продаж за id номером
--------------------------------------------------

.. http:delete:: /kw_api/integration/sales/(int:sale_order_id)

    У результаті запиту архівуємо замовлення на продаж за id номером.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X DELETE \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/sales/(int:sale_order_id)

        .. code-tab:: python

            import requests
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/sales/(int:sale_order_id)'
            response = requests.delete(URL, headers=headers)
            print(response.json())


    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "200":"Success"
           }
        }


    :statuscode 404: Order not found

    :query int sale_order_id: url параметр ідентифікатор продукту
