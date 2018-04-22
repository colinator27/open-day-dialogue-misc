.. _i_gms2_func_odd_create_value:

odd_create_value
================

Syntax
------

.. code-block:: c

    odd_create_value(type, value)

Parameters
----------
+-----------+-----------------------------------------+
|Name       |Description                              |
+===========+=========================================+
|type       |The :ref:`odd_type<i_gms2_enum_odd_type>`| 
|           |the Value represents.                    |
+-----------+-----------------------------------------+
|value      |The GameMaker value the Value holds.     |
|           |                                         |
+-----------+-----------------------------------------+

Returns
-------

The new :ref:`Value<i_gms2_class_value>`.

Description
-----------

This function creates a new Value, initializing it with the passed arguments.

.. attention:: Do not access the data of the Value directly, instead use :ref:`odd_value_type<i_gms2_func_odd_value_type>` and :ref:`odd_value_val<i_gms2_func_odd_value_val>`.

Example
-------

.. code-block:: js

    var value = odd_create_value(odd_type_int32, 21);

    // . . .

This would create a new Value with the type of odd_type_int32 and the value of 21.