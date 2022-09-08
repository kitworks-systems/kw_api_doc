Module kw_api
==============

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
==========================================

All integration endpoints require valid :doc:`/kw_api/index:API Tokens` in header Authorization

.. http:get:: /kw_api/integration/partner

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
            "totalPages": 1,
            "numberOfElements": 36,
            "number": 0,
            "last": false
        }

Integration endpoints pagination
==========================================

List endpoint support pagination.

pageIndex pass required page number. By default is equal to first page.

pageSize pass required object quantity per page. By default is equal to 100

.. http:get:: /kw_api/integration/partner?pageIndex=2&pageSize=3

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