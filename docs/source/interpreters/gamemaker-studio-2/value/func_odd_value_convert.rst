.. _i_gms2_func_odd_value_convert:

odd_value_convert
=================

Syntax
------

.. code-block:: c

    odd_value_convert(value, type)

Parameters
----------
+------+------------------------------------------+
|Name  |Description                               |
+======+==========================================+
|value |The :ref:`Value<i_gms2_class_value>`      |
|      |to convert.                               |
+------+------------------------------------------+
|type  |The :ref:`odd_type<i_gms2_macro_odd_type>`|
|      |to convert to.                            |
+------+------------------------------------------+

Returns
-------

A new :ref:`Value<i_gms2_class_value>`, that will be the value you pass in, but converted. See the possible conversions :ref:`here<i_spec_conversions>`.

Description
-----------

This function will convert any Value into another type, converting the GameMaker value it holds as well.

.. warning:: If the conversion is not listed on :ref:`the specification<i_spec_conversions>`,
             then it is likely the game will crash.

Example
-------

.. code-block:: js

    var value = odd_create_value(odd_type_int32, 21);

    var newValue = odd_value_convert(value, odd_type_string);

    show_debug_message(odd_value_val(newValue));

    // ...

This would print "21" to the console, without using :code:`string()`, because the value would already be converted.