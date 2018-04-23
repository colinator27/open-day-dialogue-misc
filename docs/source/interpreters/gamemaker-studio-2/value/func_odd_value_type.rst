.. _i_gms2_func_odd_value_type:

odd_value_type
==============

Syntax
------

.. code-block:: js

    odd_value_type(value)

Parameters
----------
+-----+-------------------------------------+
|Name |Description                          |
+=====+=====================================+
|value|The :ref:`Value<i_gms2_class_value>` |
|     |to get the                           |
|     |type                                 |
|     |of.                                  |
+-----+-------------------------------------+

Returns
-------

The :ref:`odd_type<i_gms2_macro_odd_type>` that the given :ref:`Value<i_gms2_class_value>` holds.

Description
-----------

This function pulls the :ref:`odd_type<i_gms2_macro_odd_type>` out of the given Value. This should be used instead of directly accessing it.

Example
-------

.. code-block:: js

    var value = odd_create_value(odd_type_int32, 21);

    var type = odd_value_type(value);

    // ...

This would get the type :code:`odd_type_int32` from the value, and put it into the variable :code:`type`.