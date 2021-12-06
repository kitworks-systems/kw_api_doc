Автосервіси
================

Отримання списку всіх СТО
------------------

.. http:get:: /kw_api/integration/car_services

    У результаті запиту отримуємо список всіх продуктів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/car_services

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/car_services'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":[
              {
                 "id":1,
                 "name":"string",
                 "message":"string"
              }
           ]
        }


Отримання СТО за id номером
------------------

.. http:get:: /kw_api/integration/stages/(int:car_service_id)

    У результаті запиту отримуємо СТО за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/stages/(int:car_service_id)/

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/stages/(int:car_service_id)/'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "id":1,
              "name":"string",
              "message":"string"
           }
        }



    :query int car_service_id: параметр ідентифікатор СТО


Створення списку СТО
--------------------------------------------------

.. http:post:: /kw_api/integration/stages

    У результаті запиту створюємо СТО.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/stages

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/stages'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "stages":[
              {
                "name":"string",
            "message":"string"
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
                    "id":1,
                    "name":"string",
                    "message":"string"
                }
            ]
        }

    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я стадії*
    :>json string message: повідомлення


Редагування СТО за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/stages/(int:car_service_id)

    У результаті запиту редагуємо СТО.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/stages/(int:car_service_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/stages/(int:car_service_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
            "name":"string",
            "message":"string"
        }


    **Example response**:

    .. sourcecode:: json

       {
            "jsonrpc": "2.0",
            "id": null,
            "result": {
                 "id":1,
                 "name":"string",
                 "message":"string"
            }
        }


    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я стадії*
    :>json string message: повідомлення
    :query int car_service_id: параметр ідентифікатор СТО


