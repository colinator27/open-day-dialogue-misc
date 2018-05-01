.. _i_gms2_func_odd_value_val:

odd_value_val
=============

Syntax
------

.. code-block:: js

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

:code:`any`: The GameMaker value that the given :ref:`Value<i_gms2_class_value>` holds.

Description
-----------

This function pulls the GameMaker value out of the Value. This should be used instead of directly accessing it.

Example
-------

.. code-block:: js

    var value = odd_create_value(odd_type_int32, 21);
    
    show_debug_message(string(odd_value_val(value)));

    // ...

This would print "21" to the console. Take careful note that :code:`value` is not used directly, but gets passed through this function first.