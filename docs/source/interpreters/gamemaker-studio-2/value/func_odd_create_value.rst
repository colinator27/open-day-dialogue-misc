.. _i_gms2_func_odd_create_value:

odd_create_value
================

Syntax
------

.. code-block:: js

    odd_create_value(type, value)

Parameters
----------
+-----------+------------------------------------------+
|Name       |Description                               |
+===========+==========================================+
|type       |The :ref:`odd_type<i_gms2_macro_odd_type>`| 
|           |the Value represents.                     |
+-----------+------------------------------------------+
|value      |The GameMaker value the Value holds.      |
|           |                                          |
+-----------+------------------------------------------+

Returns
-------

The reference to the new :ref:`Value<i_gms2_class_value>`. There is no need to free or delete it, because of how it is handled internally.

Description
-----------

This function creates a new Value, initializing it with the given parameters.

.. attention:: Do not attempt to access the data of a Value directly, instead use :ref:`odd_value_type<i_gms2_func_odd_value_type>` and :ref:`odd_value_val<i_gms2_func_odd_value_val>`.

Example
-------

.. code-block:: js

    var value = odd_create_value(odd_type_int32, 21);

    // . . .

This would create a new Value with the type of odd_type_int32 and the value of 21.