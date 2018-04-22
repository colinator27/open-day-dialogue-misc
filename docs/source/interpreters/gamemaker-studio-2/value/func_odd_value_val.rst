.. _i_gms2_func_odd_value_val:

odd_value_val
=============

Syntax
------

.. code-block:: c

    odd_value_val(value)

Parameters
----------
+-----------+------------------------------------+
|Name       |Description                         |
+===========+====================================+
|value      |The :ref:`Value<i_gms2_class_value>`|
|           |to get the GameMaker value of.      |
+-----------+------------------------------------+

Returns
-------

The GameMaker value that the :ref:`given Value<i_gms2_class_value>` holds.

Description
-----------

This function pulls the GameMaker value out of the given Value, and should be used instead of directly accessing it.

Example
-------

.. code-block:: js

    var value = odd_create_value(odd_type_int32, 21);
    
    show_debug_message(string(odd_value_val(value)));

    // ...

This would print "21" to the console.