Кількість товарів
================

Отримання списку всіх кількостей продукта
------------------

.. http:get:: /kw_api/integration/product_quants

    У результаті запиту отримуємо списку всіх кількостей продукта.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/product_quants

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/product_quants'
            response = requests.get(URL, headers=headers)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "content":[
                 {
                    "id":1,
                    "product_id":1,
                    "product_tmpl_id":1,
                    "company_id":1,
                    "company_name":"string",
                    "location_id":1,
                    "location_name":"string",
                    "quantity":1.0,
                    "inventory_quantity":1.0,
                    "reserved_quantity":1.0,
                    "available_quantity":1.0,
                    "write_date":"2021-10-13T09:18:24.247770"
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


    :query string datetime: параметр дата час від якого відправляти зміни по кількості продуктів ``%Y-%m-%d %H:%M:%S``


Отримання списку всіх кількостей продукту за id
------------------

.. http:get:: /kw_api/integration/product_quants/(int:product_id)

    У результаті запиту отримуємо кількость продукту  за id.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/product_quants/(int:product_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/product_quants/(int:product_id)'
            response = requests.get(URL, headers=headers)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":
              {
                    "id":1,
                    "product_id":1,
                    "product_tmpl_id":1,
                    "company_id":1,
                    "company_name":"string",
                    "location_id":1,
                    "location_name":"string",
                    "quantity":1.0,
                    "inventory_quantity":1.0,
                    "reserved_quantity":1.0,
                    "available_quantity":1.0,
                    "write_date":"2021-10-13T09:18:24.247770"
               }

        }


    :query string datetime: параметр дата час від якого відправляти зміни по кількості продуктів ``%Y-%m-%d %H:%M:%S``
    :query int product_id: параметр ідентифікатор бренда
