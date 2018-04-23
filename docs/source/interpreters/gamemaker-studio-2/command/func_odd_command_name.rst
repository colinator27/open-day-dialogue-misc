.. _i_gms2_func_odd_command_name:

odd_command_name
================

Syntax
------

.. code-block:: js

    odd_command_name(command)

Parameters
----------
+-------+------------------------------------------------------------+
|Name   |Description                                                 |
+=======+============================================================+
|command|The :ref:`Command<i_gms2_class_command>` to get the name of.|
+-------+------------------------------------------------------------+

Returns
-------

:code:`string`: The name of the given command.

Description
-----------

This function gets the name of the given Command. This should be used instead of directly accessing it.

Example
-------

.. code-block:: js

    // ...
    
    var command = odd_create_command("add", args);

    show_debug_message(odd_command_name(command));

    // ...

This would print "add" to the console.