.. _i_gms2_func_odd_instruction_opcode:

odd_instruction_opcode
======================

Syntax
------

.. code-block:: js

    odd_instruction_opcode(instruction)

Parameters
----------
+-----------+----------------------------------------------------------------------+
|Name       |Description                                                           |
+===========+======================================================================+
|instruction|The :ref:`Instruction<i_gms2_class_instruction>` to get the opcode of.|
+-----------+----------------------------------------------------------------------+

Returns
-------

:code:`odd_opcode`: The opcode of the given Instruction.

Description
-----------

Gets the :ref:`odd_opcode<i_gms2_enum_odd_opcode>` of the given Instruction.

Example
-------

.. code-block:: js

    var inst = odd_create_instruction(odd_opcode.DebugLine, 20, undefined);

    show_debug_message(string(odd_instruction_opcode(inst)));

This would print "208" (the numerical value for the DebugLine opcode) to the console.