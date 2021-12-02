Authentication
==============

Получение токена
------------------

.. http:post:: /kw_api/auth/token

    Авторизует пользователя по логину и паролю и возвращает активный токен

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/auth/token/refresh

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/auth/token'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
          "login": "login",
          "password": "password"
        }

    **Example response**:

    .. code-block:: json

        {
          "jsonrpc": "2.0",
          "id": null,
          "result": [
            {
              "name": "access_token_604d657a64ef24d",
              "user_id": 2,
              "expire_date": "2021-11-20 08:45:03",
              "is_expired": false,
              "refresh_token": "access_token_08938c77",
              "refresh_expire_date": "2022-09-06 08:45:03",
              "is_refresh_token_expired": false
            }
          ]
        }

    :>json string name: Token value
    :>json integer user_id: ID of user who was authorised
    :>json string expire_date: Date of token expiration
    :>json boolean is_expired: Is token expired
    :>json string refresh_token: Refresh token value
    :>json string refresh_expire_date: Date of refresh token expiration
    :>json boolean is_refresh_token_expired: Is refresh token expired
    :query string login: User login
    :query string password: User password


Обновление токена
--------------------------

.. http:post:: /kw_api/auth/token/refresh

    Обновляет токен на основании специального рефрештокена

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/auth/token/refresh

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/auth/token'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
          "refresh_token": "refresh_token"
        }

    **Example response**:

    .. code-block:: json

        {
          "jsonrpc": "2.0",
          "id": null,
          "result": [
            {
              "name": "access_token_604d657a64ef24d",
              "user_id": 2,
              "expire_date": "2021-11-20 08:45:03",
              "is_expired": false,
              "refresh_token": "access_token_08938c77",
              "refresh_expire_date": "2022-09-06 08:45:03",
              "is_refresh_token_expired": false
            }
          ]
        }

    :>json string name: Token value
    :>json integer user_id: ID of user who was authorised
    :>json string expire_date: Date of token expiration
    :>json boolean is_expired: Is token expired
    :>json string refresh_token: Refresh token value
    :>json string refresh_expire_date: Date of refresh token expiration
    :>json boolean is_refresh_token_expired: Is refresh token expired
    :query string refresh_token: User refresh_token


Удаление токена
---------------


.. http:delete:: /kw_api/auth/token

    Удаляет токен и обновляемый токен, получить новый будет возможно только
    через POST /kw_api/auth/token

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -H "Authorization: Token <token>" \
                http://localhost/kw_api/auth/token

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/auth/token'
            TOKEN = '<token>'
            HEADERS = {'Authorization': f'token {TOKEN}'}
            response = requests.delete(URL, headers=HEADERS)
            print(response.json())

    **Example response**:

    .. code-block:: json

        {
          "jsonrpc": "2.0",
          "id": null,
          "result": {
            "code": {
              "message": "Token has been successfully deleted"
            },
            "message": ""
          }
        }

