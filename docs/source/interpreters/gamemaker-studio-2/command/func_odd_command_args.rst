.. _i_gms2_func_odd_command_args:

odd_command_args
================

Syntax
------

.. code-block:: js

    odd_command_args(command)

Parameters
----------
+-------+------------------------------------------------------------+
|Name   |Description                                                 |
+=======+============================================================+
|command|The :ref:`Command<i_gms2_class_command>` to get the name of.|
+-------+------------------------------------------------------------+

Returns
-------

:code:`Array<Value>`: The arguments of the given command.

Description
-----------

This function gets the arguments of the given Command. This should be used instead of directly accessing it.

Example
-------

.. code-block:: js

    var args;
    args[0] = odd_create_value(odd_type_int32, 9);
    args[1] = odd_create_value(odd_type_int32, 10);

    var command = odd_create_command("add", args);

    var newArgs = odd_command_args(command);

    show_debug_message(string(array_length_1d(newArgs)));

    // ...

This would print "2" to the console.