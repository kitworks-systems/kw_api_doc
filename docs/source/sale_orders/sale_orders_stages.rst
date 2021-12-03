Этапи Продажу
================

Отримання списку всіх стадій замовлення
------------------
.. http:get:: /kw_api/integration/stages

    У результаті запиту отримуємо списку всіх стадій.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/stages

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/stages'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":[
              {
                 "id":1,
                 "name":"string",
                 "sequence":1,
                 "fold":true
              }
           ]
        }


Отримання стадії за id номером
------------------
.. http:get:: /kw_api/integration/stages/(int:stage_id)

    У результаті запиту отримуємо стадію замовлення за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/stages/(int:stage_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/stages/(int:stage_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "id":1,
              "name":"string",
              "sequence":1,
              "fold":true
           }
        }

    :query int stage_id: ідентифікатор стадії


Створення списку стадій
------------------
.. http:post:: /kw_api/integration/stages

    У результаті запиту створюємо стадії замовлення.

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
                "sequence":1,
                "fold":true
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
                    "id": 2,
                    "name": "string",
                    "sequence": 1,
                    "fold": true
                }
            ]
        }

    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я стадії*
    :>json int sequence: порядковий номер
    :>json boolean fold: флаг включення статусу в список відображаючих


Редагування стадії за id номером
------------------
.. http:post:: /kw_api/integration/stages/(int:stage_id)

    У результаті запиту створюємо стадії замовлення.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/stages/(int:stage_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/stages/(int:stage_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
            "name":"string",
            "sequence":1,
            "fold":true
        }


    **Example response**:

    .. sourcecode:: json

        {
            "jsonrpc": "2.0",
            "id": null,
            "result": {
                "id": 1,
                "name": "string",
                "sequence": 1,
                "fold": true
            }
        }



    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я стадії*
    :>json int sequence: порядковий номер
    :>json boolean fold: флаг включення статусу в список відображаючих



