Веб-Сайт
================

Отримання списку всіх вебсайтів
------------------
.. http:get:: /kw_api/integration/websites

    У результаті запиту отримуємо списку всіх вебсайтів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/websites

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/websites'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

       {
           "result":[
              {
                 "id":1,
                 "name":"string",
                 "domaine":"string",
                 "google_analytics_key":"string",
                 "auto_redirect_lang":false,
                 "cookies_bar":false,
                 "kw_counter_index":"string",
                 "kw_client_index":"string"
              }
           ]
        }


Отримання вебсайта за id номером
------------------
.. http:get:: /kw_api/integration/websites/(int:website_id)

    У результаті запиту отримуємо вебсайт за id.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/websites

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/websites'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

       {
           "result":
              {
                 "id":1,
                 "name":"string",
                 "domaine":"string",
                 "google_analytics_key":"string",
                 "auto_redirect_lang":false,
                 "cookies_bar":false,
                 "kw_counter_index":"string",
                 "kw_client_index":"string"
              }
        }


    :query int website_id: параметр ідентифікатор вебсайту


Створення списку вебсайтів
--------------------------------------------------

.. http:post::  /kw_api/integration/websites

    У результаті запиту створюємо партнерів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/websites

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/websites'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "websites":[
              {
                 "name":"string",
                 "domaine":"string",
                 "google_analytics_key":"string",
                 "auto_redirect_lang":false,
                 "cookies_bar":false,
                 "kw_counter_index":"string",
                 "kw_client_index":"string"
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
                    "name":"string",
                    "domaine":"string",
                    "google_analytics_key":"string",
                    "auto_redirect_lang":false,
                    "cookies_bar":false,
                    "kw_counter_index":"string",
                    "kw_client_index":"string"
                }
            ]
        }


    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я вебсайту*
    :>json string domaine: домен сайту
    :>json string google_analytics_key: ключ гугл аналітики



Редагування вебсайту за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/websites/(int:website_id)

    У результаті запиту редагуємо вебсайт.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/websites/(int:website_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/websites/(int:website_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
            “name":"string",
            "domaine":"string",
            "google_analytics_key":"string",
            "auto_redirect_lang":false,
            "cookies_bar":false,
            "kw_counter_index":"string",
            "kw_client_index":"string"
        }



    **Example response**:

    .. sourcecode:: json

        {
            "jsonrpc": "2.0",
            "id": null,
            "result": [
                {
                    "id": 2,
                    "name":"string",
                    "domaine":"string",
                    "google_analytics_key":"string",
                    "auto_redirect_lang":false,
                    "cookies_bar":false,
                    "kw_counter_index":"string",
                    "kw_client_index":"string"
                }
            ]
        }


    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я вебсайту*
    :>json string domaine: домен сайту
    :>json string google_analytics_key: ключ гугл аналітики
    :>json boolean auto_redirect_lang: флаг автоматичного визначення мови браузера
    :>json boolean cookies_bar: флаг відображення настроюваної панелі cookie на веб -сайті
    :>json string kw_counter_index: ідентифікатор лічильника
    :>json string kw_client_index: ідентифікатор клієнта
    :query int website_id: параметр ідентифікатор вебсайту