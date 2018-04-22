.. _i_gms2_func_odd_value_type:

odd_value_type
==============

Syntax
------

.. code-block:: c

    odd_value_type(value)

Parameters
----------
+-----+-------------------------------------+
|Name |Description                          |
+=====+=====================================+
|value|The :ref:`Value<i_gms2_class_value>` |
|     |to get the                           |
|     |:ref:`odd_type<i_gms2_enum_odd_type>`|
|     |of.                                  |
+-----+-------------------------------------+

Returns
-------

The :ref:`odd_type<i_gms2_enum_odd_type>` that the
:ref:`given Value<i_gms2_class_value>` holds.

Description
-----------

This function pulls the :ref:`odd_type<i_gms2_enum_odd_type>` out of the given Value, and should be used instead of directly accessing it.

Example
-------

.. code-block:: js

    var value = odd_create_value(odd_type_int32, 21);

    var type = odd_value_type(value);

    // ...

This would add the type **odd_type_int32** to the variable **type**.