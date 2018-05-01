.. _i_gms2_func_odd_instruction_op1:

odd_instruction_op1
===================

Syntax
------

.. code-block:: js

    odd_instruction_op1(instruction)

Parameters
----------
+-----------+-----------------------------------------------------------------------------+
|Name       |Description                                                                  |
+===========+=============================================================================+
|instruction|The :ref:`Instruction<i_gms2_class_instruction>` to get the first operand of.|
+-----------+-----------------------------------------------------------------------------+

Returns
-------

:code:`Number|Undefined`: The first operand of the given instruction.

Description
-----------

This function gets the first operand of the given Instruction, if any.

Example
-------

.. code-block:: js

    var inst = odd_create_instruction(odd_opcode.DebugLine, 20, undefined);

    show_debug_message(string(odd_instruction_op1(inst)));

    // ...

This would print "20" to the console.