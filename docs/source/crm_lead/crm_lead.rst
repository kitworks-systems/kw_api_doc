Управління CRM
================

Отримання списку всіх CRM лідів
------------------
.. http:get:: /kw_api/integration/leads

    У результаті запиту отримуємо списку всіх CRM лідів.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash
        
            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/leads

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/leads'
            response = requests.get(URL, headers=headers)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "content":[
                 {
                    "id":1,
                    "name":"string",
                    "partner_id":0,
                    "active":true,
                    "date_action_last":"2000-01-01T00:00:00",
                    "email_from":"example@example.com",
                    "website":"http://www.example.com",
                    "team_id":0,
                    "kanban_state":"grey",
                    "description":"string",
                    "contact_name":"string",
                    "partner_name":"string",
                    "type":"opportunity",
                    "priority":"0",
                    "date_closed":"2000-01-01T00:00:00",
                    "stage_id":0,
                    "user_id":0,
                    "referred":"string",
                    "date_open":"2000-01-01T00:00:00",
                    "day_open":0.0,
                    "day_close":0.0,
                    "date_last_stage_update":"2000-01-01T00:00:00",
                    "date_conversion":"2000-01-01T00:00:00",
                    "probability":0.0,
                    "automated_probability":0.0,
                    "is_automated_probability":true,
                    "phone_state":"incorrect",
                    "email_state":"correct",
                    "prorated_revenue":0.0,
                    "expected_revenue":0.0,
                    "date_deadline":"2021-07-12",
                    "color":0,
                    "partner_is_blacklisted":false,
                    "company_currency":0,
                    "user_email":"example@example.com",
                    "user_login":"string",
                    "street":"string",
                    "street2":"string",
                    "zip":"string",
                    "city":"string",
                    "state_id":0,
                    "country_id":0,
                    "lang_id":0,
                    "phone":"(000)-000-0000",
                    "mobile":false,
                    "function":false,
                    "title":0,
                    "company_id":0,
                    "meeting_count":0
                 }
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


Отримання CRM ліда за id номером
------------------
.. http:get:: /kw_api/integration/leads/(int:lead_id)

    У результаті запиту отримуємо  CRM контакт за id.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash
        
            $ curl \
                -X GET \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/leads/(int:lead_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/leads/(int:lead_id)'
            response = requests.get(URL, headers=headers)
            print(response.json())


    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "id":1,
              "name":"string",
              "partner_id":0,
              "active":true,
              "date_action_last":"2000-01-01T00:00:00",
              "email_from":"example@example.com",
              "website":"http://www.example.com",
              "team_id":0,
              "kanban_state":"grey",
              "description":"string",
              "contact_name":"string",
              "partner_name":"string",
              "type":"opportunity",
              "priority":"0",
              "date_closed":"2000-01-01T00:00:00",
              "stage_id":0,
              "user_id":0,
              "referred":"string",
              "date_open":"2000-01-01T00:00:00",
              "day_open":0.0,
              "day_close":0.0,
              "date_last_stage_update":"2000-01-01T00:00:00",
              "date_conversion":"2000-01-01T00:00:00",
              "probability":0.0,
              "automated_probability":0.0,
              "is_automated_probability":true,
              "phone_state":"incorrect",
              "email_state":"correct",
              "prorated_revenue":0.0,
              "expected_revenue":0.0,
              "date_deadline":"2021-07-12",
              "color":0,
              "partner_address_name":"string",
              "partner_address_email":"example@example.com",
              "partner_address_phone":"(000)-000-0000",
              "partner_is_blacklisted":false,
              "company_currency":0,
              "user_email":"example@example.com",
              "user_login":"string",
              "street":"string",
              "street2":"string",
              "zip":"string",
              "city":"string",
              "state_id":0,
              "country_id":0,
              "lang_id":0,
              "phone":"(000)-000-0000",
              "mobile":"(000)-000-0000",
              "function":"string",
              "title":0,
              "company_id":0,
              "meeting_count":0
           }
        }


    :query int lead_id: ідентифікатор замовлення


Створення CRM контактів
------------------
.. http:post:: /kw_api/integration/leads

    У результаті запиту створюємо CRM лід.

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
                http://localhost/kw_api/integration/leads

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/leads'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "leads":[
              {
                 "name":"string",
                 "partner_id":1,
                 "active":true,
                 "date_action_last":"2000-01-01 00:00:00",
                 "email_from":"example@example.com",
                 "website":"http://www.example.com",
                 "team_id":1,
                 "kanban_state":"grey",
                 "description":"string",
                 "contact_name":"string",
                 "partner_name":"string",
                 "type":"opportunity",
                 "priority":"0",
                 "date_closed":"2000-01-01 00:00:00",
                 "stage_id":1,
                 "user_id":1,
                 "referred":"string",
                 "date_open":"2000-01-01 00:00:00",
                 "day_open":0.0,
                 "day_close":0.0,
                 "date_last_stage_update":"2000-01-01 00:00:00",
                 "date_conversion":"2000-01-01 00:00:00",
                 "probability":0.0,
                 "automated_probability":0.0,
                 "is_automated_probability":true,
                 "phone_state":"incorrect",
                 "email_state":"correct",
                 "prorated_revenue":0.0,
                 "expected_revenue":0.0,
                 "date_deadline":"2021-07-12",
                 "color":1,
                 "partner_is_blacklisted":false,
                 "company_currency":1,
                 "user_email":"example@example.com",
                 "user_login":"string",
                 "street":"string",
                 "street2":"string",
                 "zip":"string",
                 "city":"string",
                 "state_id":1,
                 "country_id":1,
                 "lang_id":1,
                 "phone":"(000)-000-0000",
                 "mobile":"(000)-000-0000",
                 "function":"string",
                 "title":1,
                 "company_id":0,
                 "meeting_count":0
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
                    "partner_id": 1,
                    "active": true,
                    "date_action_last": "2000-01-01 00:00:00",
                    "email_from": "example@example.com",
                    "website": "http://www.example.com",
                    "team_id": 1,
                    "kanban_state": "grey",
                    "description": "string",
                    "contact_name": "string",
                    "partner_name": "string",
                    "type": "opportunity",
                    "priority": "0",
                    "date_closed": "2000-01-01 00:00:00",
                    "stage_id": 1,
                    "user_id": 1,
                    "referred": "string",
                    "date_open": "2000-01-01 00:00:00",
                    "day_open": 0.0,
                    "day_close": 0.0,
                    "date_last_stage_update": "2000-01-01 00:00:00",
                    "date_conversion": "2000-01-01 00:00:00",
                    "probability": 0.0,
                    "automated_probability": 0.0,
                    "is_automated_probability": true,
                    "phone_state": "incorrect",
                    "email_state": "correct",
                    "prorated_revenue": 0.0,
                    "expected_revenue": 0.0,
                    "date_deadline": "2021-01-01",
                    "color": 1,
                    "partner_address_name": "string",
                    "partner_address_email": "example@example.com",
                    "partner_address_phone": "+1 (650) 555-0111 ",
                    "partner_is_blacklisted": false,
                    "company_currency": 1,
                    "user_email": "example@example.com",
                    "user_login": "string",
                    "street": "string",
                    "street2": "string",
                    "zip": "string",
                    "city": "string",
                    "State_id": 1,
                    "country_id": 1,
                    "lang_id": 1,
                    "phone": "(000)-000-0000",
                    "mobile": "(000)-000-0000",
                    "function": "string",
                    "title": 1,
                    "company_id": 1,
                    "meeting_count": 0
                }
            ]
        }



    **Обов'язкові поля відмічені '*'**

    :>json string name: назва ліда CRM *
    :>json int partner_id: ідентифікатор партнера
    :>json string date_action_last: дата останньої активності (формат - ``%Y-%m-%d %H:%M:%S``)
    :>json string email_from:  почта з якого прийшлов лід
    :>json sring website:  вебсайт
    :>json int team_id: ідентифікатор команди
    :>json string kanban_stage: етап дошки (``grey``, ``red``, ``green``)
    :>json string description: опис ліда CRM
    :>json string contact_name:  ім’я контакта CRM
    :>json string partner_name: ім’я партнера CRM
    :>json string type: тип ліда в CRM - лід або нагода (``lead``, ``opportunity``) *
    :>json string priority: пріорітет ліда CRM (``1`` - Low, ``2`` - Medium ,``3`` - High ,``4`` - Very High )
    :>json string date_closed: дата закриття ( формат - ``%Y-%m-%d %H:%M:%S``)
    :>json int stage_id: ідентифікатор етапу
    :>json int user_id: ідентифікатор користувача
    :>json string referred: посилання
    :>json string date_open: дата відкриття (формат - ``%Y-%m-%d %H:%M:%S``)
    :>json float day_open: скільки днів відкрито
    :>json float day_close: скільки днів закрито
    :>json string date_last_stage_update: дата відкриття (формат - ``%Y-%m-%d %H:%M:%S``)
    :>json string date_conversion: дата перетворення (формат - ``%Y-%m-%d %H:%M:%S``)
    :>json float probability: вірогідність ліда CRM
    :>json float automated_probability: автоматична вірогідність ліда CRM
    :>json boolean is_automated_probability: флаг автоматична вірогідність ліда CRM
    :>json string phone_state: статус телефона (``correct``, ``incorrect``)
    :>json string email_state: статус почти (``correct``, ``incorrect``)
    :>json float prorated_revenue: запланований дохід
    :>json float expected_revenue: очікуваний дохід
    :>json string date_deadline: дата бажаного завершення (формат - ``%Y-%m-%d %H:%M:%S``)
    :>json int color: номер коліру
    :>json boolean partner_is_blacklisted: чи є  партнер в чорному списку
    :>json int company_currency: ідентифікатор валюти компанії
    :>json string user_email: почта користувача
    :>json string user_login: ім’я користувача
    :>json string street: вулиця
    :>json string street2: вулиця 2
    :>json string zip: zip код регіону
    :>json string city: місто
    :>json int state_id: ідентифікатор штату
    :>json int country_id: ідентифікатор країни
    :>json int lang_id: ідентифікатор мови
    :>json string phone: телефон
    :>json string mobile: мобільний телефон
    :>json string function: функція
    :>json int title: ідентифікатор заголовку партнера
    :>json int company_id: ідентифікатор компанії
    :>json int meeting_count: кількість зустрічей


Редагування CRM ліда за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/leads/(int:lead_id)

    У результаті запиту створюємо замовлення CRM лід за id.

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
                http://localhost/kw_api/integration/leads/(int:lead_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/leads/(int:lead_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "name":"string",
           "partner_id":1,
           "active":true,
           "date_action_last":"2000-01-01 00:00:00",
           "email_from":"example@example.com",
           "website":"http://www.example.com",
           "team_id":1,
           "kanban_state":"grey",
           "description":"string",
           "contact_name":"string",
           "partner_name":"string",
           "type":"opportunity",
           "priority":"0",
           "date_closed":"2000-01-01 00:00:00",
           "stage_id":1,
           "user_id":1,
           "referred":"string",
           "date_open":"2000-01-01 00:00:00",
           "day_open":0.0,
           "day_close":0.0,
           "date_last_stage_update":"2000-01-01 00:00:00",
           "date_conversion":"2000-01-01 00:00:00",
           "probability":0.0,
           "automated_probability":0.0,
           "is_automated_probability":true,
           "phone_state":"incorrect",
           "email_state":"correct",
           "prorated_revenue":0.0,
           "expected_revenue":0.0,
           "date_deadline":"2021-07-12",
           "color":1,
           "partner_is_blacklisted":false,
           "company_currency":1,
           "user_email":"example@example.com",
           "user_login":"string",
           "street":"string",
           "street2":"string",
           "zip":"string",
           "city":"string",
           "state_id":1,
           "country_id":1,
           "lang_id":1,
           "phone":"(000)-000-0000",
           "mobile":"(000)-000-0000",
           "function":"string",
           "title":1,
           "company_id":0,
           "meeting_count":0
        }



    **Example response**:

    .. sourcecode:: json

        {
           "jsonrpc":"2.0",
           "id":null,
           "result":{
              "id":0,
              "name":"string",
              "partner_id":1,
              "active":true,
              "date_action_last":"2000-01-01 00:00:00",
              "email_from":"example@example.com",
              "website":"http://www.example.com",
              "team_id":1,
              "kanban_state":"grey",
              "description":"string",
              "contact_name":"string",
              "partner_name":"string",
              "type":"opportunity",
              "priority":"0",
              "date_closed":"2000-01-01 00:00:00",
              "stage_id":1,
              "user_id":1,
              "referred":"string",
              "date_open":"2000-01-01 00:00:00",
              "day_open":0.0,
              "day_close":0.0,
              "date_last_stage_update":"2000-01-01 00:00:00",
              "date_conversion":"2000-01-01 00:00:00",
              "probability":0.0,
              "automated_probability":0.0,
              "is_automated_probability":true,
              "phone_state":"incorrect",
              "email_state":"correct",
              "prorated_revenue":0.0,
              "expected_revenue":0.0,
              "date_deadline":"2021-01-01",
              "color":1,
              "partner_address_name":"string",
              "partner_address_email":"example@example.com",
              "partner_address_phone":"+1 (650) 555-0111 ",
              "partner_is_blacklisted":false,
              "company_currency":"res.currency()",
              "user_email":"example@example.com",
              "user_login":"string",
              "street":"string",
              "street2":"string",
              "zip":"string",
              "city":"string",
              "state_id":1,
              "country_id":1,
              "lang_id":1,
              "phone":"(000)-000-0000",
              "mobile":"(000)-000-0000",
              "function":"string",
              "title":1,
              "company_id":1,
              "meeting_count":0
           }
        }


    :query int sale_order_id: параметр ідентифікатор замовлення


Видалення  ліда CRM за id номером
--------------------------------------------------

.. http:delete:: /kw_api/integration/leads/(int:lead_id)

    У результаті запиту архівуємо  лід CRM за id номером.

    .. attention::

        Api Key - ключ для особистого доступу до API (required in header)

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X DELETE \
                -H "Content-Type: application/json" \
                -H "Authorization: Bearer_ + Your Api Key" \
                http://localhost/kw_api/integration/leads/(int:lead_id)

        .. code-tab:: python

            import requests
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/leads/(int:lead_id)'
            response = requests.delete(URLб headers=headers)
            print(response.json())


    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "200":"Success"
           }
        }


    :statuscode 404: Lead not found
    :query int product_id: url параметр ідентифікатор продукту

