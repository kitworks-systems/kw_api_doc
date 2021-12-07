Зображення товарів
================

Отримання списку всіх картинок за id продукта
------------------

.. http:get:: /kw_api/integration/product_images/(int:product_id)

    Отримання списку всіх картинок за id продукта

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl http://localhost/kw_api/integration/product_images/(int:product_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/product_images/(int:product_id)'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
           "result":{
              "Content":[
                 {
                    "id":0,
                    "name":"string",
                    "sequence":0,
                    "product_tmpl_id":4,
                    "video_url":"",
                    "update_date":"2021-11-16T11:38:33",
                    "images_url":"https://sportua.ct115.kitworks.systems/kw_api/integration/image/product.template/31/image_1920/"
                },
                 [
                    {
                       "id":1,
                       "name":"string",
                       "sequence":10,
                       "product_tmpl_id":1,
                       "Video_url":false,
                   "update_date":"2021-11-16T11:38:33",
                       "images_url":"http://example.com/kw_api/integration/image/product.image/1/image_1920/"
                    }
                 ]
              ],
              "totalElements":1,
              "totalPages":1,
              "numberOfElements":1,
              "number":0,
              "last":false
           }
        }


    :query int product_template_id: параметр ідентифікатор продукта


Створення картинок
--------------------------------------------------

.. http:post:: /kw_api/integration/product_images

    У результаті запиту створюємо картинки.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/product_images

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/product_images'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
           "product_images":[
              {
                   "id":1,
                   "name":"string",
                   "sequence":10,
                   "product_tmpl_id":1,
                   "video_url":"http://example.com/1920/",
                   "images_url":"http://example.com/1920/"
              }
           ]
        }


    **Example response**:

    .. sourcecode:: json

       {
            "jsonrpc": "2.0",
            "id": null,
            "result": [{
                   "id":1,
                   "name":"string",
                   "sequence":10,
                   "product_tmpl_id":1,
                   "video_url":false,
                      "images_url":"http://example.com/kw_api/integration/image/product.image/1/image_1920/"
                    }]
        }

     **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я розмірної сітки*
    :>json string sequence: порядковий номер
    :>json int product_tmpl_id: ідентифікатор шаблону продукта*
    :>json int video_url: посилання на відео
    :>json string image: бінарний файл картинки
    :>json string image_url: ссилка на картинку


Редагування картинки за id номером
--------------------------------------------------

.. http:post:: /kw_api/integration/product_images/(int:product_img_id)

    У результаті запиту створюємо картинки.

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl \
                -X POST \
                -H "Content-Type: application/json" \
                -d @body.json \
                http://localhost/kw_api/integration/product_images/(int:product_img_id)

        .. code-tab:: python

            import requests
            import json
            URL = 'http://localhost/kw_api/integration/product_images/(int:product_img_id)'
            data = json.load(open('body.json', 'rb'))
            response = requests.post(URL, json=data)
            print(response.json())

    The content of body.json is like:

    .. code-block:: json

        {
               "id":1,
               "name":"string",
               "sequence":10,
               "product_tmpl_id":1,
               "video_url":"http://example.com/1920/",
               "images_url":"http://example.com/1920/"
        }


    **Example response**:

    .. sourcecode:: json

       {
            "jsonrpc": "2.0",
            "id": null,
            "result": {
                   "id":1,
                   "name":"string",
                   "sequence":10,
                   "product_tmpl_id":1,
                   "video_url":false,
                      "images_url":"http://example.com/kw_api/integration/image/product.image/1/image_1920/"
            }
        }


     **Обов'язкові поля відмічені '*'**

    :>json string name: ім’я розмірної сітки*
    :>json string sequence: порядковий номер
    :>json int product_tmpl_id: ідентифікатор шаблону продукта*
    :>json int video_url: посилання на відео
    :>json string image: бінарний файл картинки
    :>json string image_url: ссилка на картинку
    :query int product_img_id: параметр ідентифікатор категорії розмірної сітки