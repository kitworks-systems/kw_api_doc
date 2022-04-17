Користувачі
================

Отримання списку всіх користувачів
------------------
.. http:get:: /kw_api/integration/users

    У результаті запиту отримуємо списку всіх користувачів.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)
        
    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/users

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/users'
            response = requests.get(URL, headers=headers)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":[
              {
                 "id":2,
                 "name":"string",
                 "login":"string",
                 "email":"string@example.com",
                 "partner_id":1
              }
           ]
        }


Отримання користувача за id номером
------------------
.. http:get:: /kw_api/integration/users/(int:user_id)

    У результаті запиту отримуємо  CRM контактаки за id.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)
        
    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/users/(int:user_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/users/(int:user_id)'
            response = requests.get(URL, headers=headers)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
                 “id":2,
                 "name":"string",
                 "login":"string",
                 "email":"string@example.com",
                 "partner_id":1
             }
        }



    :query int user_id: url параметр ідентифікатор користувача

