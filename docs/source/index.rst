Kitworks API Specification
==========================

.. note::

    This project is under active development.

API creating framework
----------------------

kw_api is a framework for creating a deeply customized API that can be used to
integrate Odoo with other systems such as CMS, mobile application,
frontend sites etc.

Module kw_api provides

* all request logging functionality
* authorization based on user token (more applicable for mobile apps)
* authorization based on api key with IP address restriction (more applicable for CMS or other server systems)
* endpoints wrapper
* input data parsing and validation
* automatic response data preparation and pagination
* multi language response



.. toctree::
   :maxdepth: 3
   :hidden:
   :glob:
   :caption: kw_api (base functionality)

   kw_api/index
   kw_api/endpoint

.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Authentication

   auth/index
   currencies/index

.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Products

   products/products
   products/product_images
   products/product_brands
   products/product_quants

.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Sale Orders

   sale_orders/sale_orders_stages
   sale_orders/sale_orders

.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: CRM Lead

   crm_lead/crm_lead

.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Users

   users/users

.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Partners

   partners/partners


.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Delivery

   delivery/delivery


.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Website

   website/website


.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Sizes

   sizes/sizes
   sizes/size_charts
   sizes/size_chart_categories
