.. _i_gms2_func_odd_create_command:

odd_create_command
==================

Syntax
------

.. code-block:: js

    odd_create_command(name, arg_array)

Parameters
----------
+---------+-------------------------------------------------------------------------------------+
|Name     |Description                                                                          |
+=========+=====================================================================================+
|name     |The name of the command or function to create.                                       |
+---------+-------------------------------------------------------------------------------------+
|arg_array|An array of :ref:`Values<i_gms2_class_value>` acting as the arguments to the command.|
+---------+-------------------------------------------------------------------------------------+

Returns
-------

:code:`Command`: The reference to the new :ref:`Command<i_gms2_class_command>`. There is no need to free or delete it, because of how it is handled internally.

Description
-----------

This function creates a new Command, initializing it with the given parameters.

.. note:: If you're looking to make a command or function to use in-game, instead use :ref:`odd_instance_function_add<i_gms2_func_odd_instance_function_add>` or :ref:`odd_instance_command_add<i_gms2_func_odd_instance_command_add>`.

Example
-------

.. code-block:: js

    var args;
    args[0] = odd_create_value(odd_type_int32, 9);
    args[1] = odd_create_value(odd_type_int32, 10);

    var command = odd_create_command("add", args);

    // ...

This would create a new Command with the name "add", that has 2 int32 arguments, 9 and 10.