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

Integration modules provides

* protection :doc:`Integration endpoints protections </kw_api/index:Integration endpoints protections>`
* pagination :doc:`Integration endpoints protections </kw_api/index:Integration endpoints pagination>`


.. toctree::
   :maxdepth: 2
   :hidden:
   :glob:
   :caption: Framework features

   kw_api/index
   kw_api/endpoint
   kw_api/auth
