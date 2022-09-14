Partner (Odoo Contacts)
========================

This endpoints provide access to Odoo Contacts (model res.partner)

Partner list
-----------------------------------

.. http:get:: /kw_api/integration/partner

    У результаті запиту отримуємо списку всіх контактів.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl -X GET \
                -H "Authorization: Your_Api_Key" \
                -H "Content-Type: application/json" \
                http://localhost/kw_api/integration/partner

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Your_Api_Key',
                       'Content-Type': 'application/json', }
            URL = 'http://localhost/kw_api/integration/partner'
            response = requests.get(URL, headers=headers)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
            "content": [
                {
                    "id": 14,
                    "name": "Azure Interior",
                    "ref": false,
                    "lang": "en_US",
                    "website": "http://www.azure-interior.com",
                    "phone": "(870)-931-0505",
                    "mobile": false,
                    "email": "azure.Interior24@example.com",
                    "country_id": {
                        "id": 233,
                        "name": "United States",
                        "name_en": "United States",
                        "name_ru": "Соединённые Штаты Америки",
                        "name_uk": "США"
                    },
                    "state_id": {
                        "id": 13,
                        "name": "California"
                    },
                    "city": "Fremont",
                    "street": "4557 De Silva St",
                    "street2": false
                }
            ],
            "totalElements": 36,
            "totalPages": 1,
            "numberOfElements": 36,
            "number": 0,
            "last": false
        }

    :>json int id: record database ID
    :>json string name: contact name
    :>json string ref: contact reference
    :>json string lang: contact locale (language ISO code)
    :>json string website: contact website
    :>json string phone: contact phone
    :>json string mobile: contact mobile
    :>json string email: contact email
    :>json dict country_id: contact country
    :>json dict state_id: contact state
    :>json string city: contact city
    :>json string street: contact building address
    :>json string street2: contact building address inside building


Partner get
------------------

.. http:get:: /kw_api/integration/partners/(int:partner_id)

    У результаті запиту отримуємо користувача за id номером.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl -X GET \
                -H "Authorization: Your_Api_Key" \
                -H "Content-Type: application/json" \
                http://localhost/kw_api/integration/partner/1

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Your_Api_Key',
                       'Content-Type': 'application/json', }
            URL = '/kw_api/integration/partners/1'
            response = requests.get(URL, headers=headers)
            print(response.json())

    :query int partner_id: record database ID

    **Example response**:

    .. sourcecode:: json

        {
            "id": 1,
            "name": "YourCompany",
            "ref": false,
            "lang": "en_US",
            "website": "http://www.example.com",
            "phone": "+1 (650) 555-0111 ",
            "mobile": false,
            "email": "info@yourcompany.com",
            "country_id": {
                "id": 233,
                "name": "United States",
                "name_en": "United States",
                "name_ru": "Соединённые Штаты Америки",
                "name_uk": "США"
            },
            "state_id": {
                "id": 13,
                "name": "California"
            },
            "city": "San Francisco",
            "street": "250 Executive Park Blvd, Suite 3400",
            "street2": false
        }



Створення контакту
--------------------------------------------------

.. http:post:: /kw_api/integration/partners

    У результаті запиту створюємо контакт.

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
                http://localhost/kw_api/integration/partners

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/partners'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "partners":[
              {
                 "name":"string",
                 "ref":"string",
                 "website":"http://www.example.com",
                 "phone":"(000)-000-0000",
                 "email":"example@example.com",
                 "city":"string",
                 "street":"string",
                 "street2":"string"
              }
           ]
        }

    **Example response**:

    .. sourcecode:: json

        {
           "jsonrpc":"2.0",
           "id":null,
           "result":[
              {
                 "id":0,
                 "name":"string",
                 "sale_ok":false,
                 "description":"string",
                 "description_purchase":"string",
                 "description_sale":"string",
                 "type":"product",
                 "rental":false,
                 "categ_id":"product.category()",
                 "list_price":0.0,
                 "standard_price":0.0,
                 "price_extra":0.0,
                 "taxes_id":"account.tax()",
                 "purchase_ok":false,
                 "active":true,
                 "color":0,
                 "is_product_variant":true,
                 "default_code":"string",
                 "barcode":"string",
                 "images_url":"http://url/kw_api/integration/image/product.image/68/image_1920/",
                 "currency_id":0
              }
           ]
        }


    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я  контакту*
    :>json string ref: опис
    :>json string website: сайт
    :>json string phone: телефон контакту*
    :>json string email: електронна почта контакту*
    :>json string city: місто контакту
    :>json string street: адреса контакту
    :>json string street2: додаткова адреса контакту


Редагування контакту за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/partners/(int:partner_id)

    У результаті запиту отримуємо контакту за id.

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
                http://localhost/kw_api/integration/partners/(int:partner_id)

        .. code-tab:: python

            import requests
            import json
            headers = {'Authorization': 'Bearer_ + Your Api Key'}
            URL = 'http://localhost/kw_api/integration/partners/(int:partner_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data, headers=headers)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "partners":[
              {
                 "name":"string",
                 "ref":"string",
                 "website":"http://www.example.com",
                 "phone":"(000)-000-0000",
                 "email":"example@example.com",
                 "city":"string",
                 "street":"string",
                 "street2":"string"
              }
           ]
        }

    **Example response**:

    .. sourcecode:: json

        {
           "jsonrpc":"2.0",
           "id":null,
           "result":[
              {
                 "id":0,
                 "name":"string",
                 "sale_ok":false,
                 "description":"string",
                 "description_purchase":"string",
                 "description_sale":"string",
                 "type":"product",
                 "rental":false,
                 "categ_id":"product.category()",
                 "list_price":0.0,
                 "standard_price":0.0,
                 "price_extra":0.0,
                 "taxes_id":"account.tax()",
                 "purchase_ok":false,
                 "active":true,
                 "color":0,
                 "is_product_variant":true,
                 "default_code":"string",
                 "barcode":"string",
                 "images_url":"http://url/kw_api/integration/image/product.image/68/image_1920/",
                 "currency_id":0
              }
           ]
        }


    **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я  контакту*
    :>json string ref: опис
    :>json string website: сайт
    :>json string phone: телефон контакту*
    :>json string email: електронна почта контакту*
    :>json string city: місто контакту
    :>json string street: адреса контакту
    :>json string street2: додаткова адреса контакту
    :query int partner_id: url параметр ідентифікатор контакту
