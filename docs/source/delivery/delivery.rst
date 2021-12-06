Доставки
================

Отримання списку всіх методів доставки
------------------
.. http:get:: /kw_api/integration/deliveries

    У результаті запиту отримуємо список всіх методів доставки.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/deliveries

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/deliveries'
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
                    "sequence":1,
                    "delivery_type":"string",
                    "integration_level":"string",
                    "prod_environment":false,
                    "product_id":1,
                    "invoice_policy":"string",
                    "margin":0.0,
                    "free_over":true,
                    "amount":0.0,
                    "can_generate_return":false,
                    "return_label_on_delivery":false,
                    "get_return_label_from_portal":false
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


Отримання методу доставки за id номером
------------------
.. http:get::  /kw_api/integration/deliveries/(int:carrier_id)

    У результаті запиту отримуємо метод доставки за id номером.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/deliveries/(int:carrier_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/deliveries/(int:carrier_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

       {
           "result":{
                 "id":1,
                 "name":"string",
                 "sequence":1,
                 "delivery_type":"string",
                 "integration_level":"string",
                 "prod_environment":false,
                 "product_id":1,
                 "invoice_policy":"string",
                 "margin":0.0,
                 "free_over":true,
                 "amount":0.0,
                 "can_generate_return":false,
                 "return_label_on_delivery":false,
                 "get_return_label_from_portal":false
             }
        }


:query int carrier_id: url параметр ідентифікатор метода доставки
