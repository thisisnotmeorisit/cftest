aiocf package
=============

Subpackages
-----------

.. toctree::
   :maxdepth: 4

   aiocf.lydia

Submodules
----------

aiocf.api module
----------------

.. automodule:: aiocf.api
   :members:
   :undoc-members:
   :show-inheritance:

.. warning::
   You needn't instantiate this class directly.
   Doing so would create a ClientSession object.
   Another ClientSession would be created when you instantiate a subclass like LydiaAI.
   You'd have to manually close **both** sessions in this case.

   You're always better off instantiating subclasses like LydiaAI directly.


aiocf.exception module
----------------------

.. automodule:: aiocf.exception
   :members:
   :undoc-members:
   :show-inheritance:


Module contents
---------------

.. automodule:: aiocf
   :members:
   :undoc-members:
   :show-inheritance:
