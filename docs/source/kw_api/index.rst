Framework features (module kw_api)
==================================

kw_api modile is a core of API framework. Most settings, features and common code works in it.

Settings
------------------

Settings allow you to customize how the API works according to your needs

.. figure:: /_static/images/kw_api/1.png
   :width: 800
   :align: center
   :alt: Settings


Token settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Response settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Language settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Logging
------------------

kw_api logs all request successful and error

.. figure:: /_static/images/kw_api/2.png
   :width: 800
   :align: center
   :alt: Log list

.. figure:: /_static/images/kw_api/3.png
   :width: 800
   :align: center
   :alt: Log json


Request logs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Error logs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


API Tokens
------------------


API Keys
------------------


Integration endpoints protection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

All integration endpoints require valid :doc:`API token </kw_api/index:api-tokens>` in header Authorization

.. http:get:: /kw_api/integration/partner

    ``Authorization``  pass valid API key.

    ``Content-Type``  pass "application/json"

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
            headers = {
                'Authorization': 'Your_Api_Key',
                'Content-Type': 'application/json',
            }
            URL = 'http://localhost/kw_api/integration/partner'
            response = requests.get(URL, headers=headers)
            print(response.json())


Integration endpoints pagination
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

List endpoint endpoints supports pagination with requested pages size

.. http:get:: /kw_api/integration/partner?pageIndex=2&pageSize=3

    List endpoint support pagination.

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
            headers = {
                'Authorization': 'Your_Api_Key',
                'Content-Type': 'application/json',
            }
            URL = 'http://localhost/kw_api/integration/partner'
            response = requests.get(URL, headers=headers)
            print(response.json())

    :query int pageIndex: pass required page number. By default is equal to first page.
    :query int pageSize: pass required object quantity per page. By default is equal to 100

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
                    "email": "azure.Interior24@example.com",
                    "city": "Fremont",
                    "street": "4557 De Silva St",
                    "street2": false
                }
            ],
            "totalElements": 36,
            "totalPages": 12,
            "numberOfElements": 3,
            "number": 2,
            "last": false
        }

    :>json string totalElements: Quantity of elements in response
    :>json string totalPages: Quantity of pages in response
    :>json string numberOfElements: Quantity of elements in page (is equals to pageSize)
    :>json string number: Current page number (is equals to pageIndex)
    :>json string last: Is page last (number == totalPages)


Integration endpoints updated only elements
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Most of list endpoints supports filtration by last update date.

.. http:get:: /kw_api/integration/partner?update_date=2022-10-10 10:10:10

    List endpoint support last update date filtration.

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
            headers = {
                'Authorization': 'Your_Api_Key',
                'Content-Type': 'application/json',
            }
            URL = 'http://localhost/kw_api/integration/partner'
            response = requests.get(URL, headers=headers)
            print(response.json())

    :query datetime update_date: Datetime from which changed objects will be selected


