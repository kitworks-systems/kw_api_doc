Authentication
==============

Получение токена
------------------

.. http:get:: /kw_api/auth/token

Возвращает информацию об активном токене

**Example request**:



The content of body.json is like:

.. code-block:: json

    {
      "login": "login",
      "password": "password"
    }


200 - Successful Response

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

.. code-block:: console

    POST /kw_api/auth/token/refresh

метод запроса methods=['POST']

тип запроса type='json' (Нужно передать заголовок
Content-Type: application/json)

Обязательный параметр refreshToken, значение которого получается в ответе
/kw_api/auth/token в refresh_token

Стурктура корретного ответа (совпадает с /kw_api/auth/token)

.. code-block:: json

    {
      "jsonrpc": "2.0",
      "id": null,
      "result": [
        {
          "name": "access_token_1c807c04e173b64026",
          "user_id": 2,
          "expire_date": "2021-11-20 08:52:30",
          "is_expired": false,
          "refresh_token": "access_token_c670d49ccf",
          "refresh_expire_date": "2022-09-06 08:52:30",
          "is_refresh_token_expired": false
        }
      ]
    }


Удаление токена
---------------

.. code-block:: console

    DELETE /kw_api/auth/token

Удаляет токен и обновляемый токен, получить новый будет возможно только
через POST /kw_api/auth/token

метод запроса methods=['DELETE']

Обязательный параметр в заголовке Authorization, в котором нужно передать
токен, полученный через контроллер /kw_api/auth/token

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


Стурктура ответа с ошибкой, значение параметра message может быть переведено
на язык пользователя

.. code-block:: json

    {
      "jsonrpc": "2.0",
      "id": null,
      "result": {
        "code": "auth_error",
        "message": "No token were given or given wrong one"
      }
    }