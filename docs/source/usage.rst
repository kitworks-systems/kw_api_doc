Usage
=====

.. _installation:

Installation
------------

To use kwapidoc, first install it using pip:

.. code-block:: console

   (.venv) $ pip install kwapidoc

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``kwapidoc.get_random_ingredients()`` function:

.. autofunction:: kwapidoc.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`kwapidoc.get_random_ingredients`
will raise an exception.

.. autoexception:: kwapidoc.InvalidKindError

For example:

>>> import kwapidoc
>>> kwapidoc.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

