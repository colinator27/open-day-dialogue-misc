.. _i_gms2_func_odd_instruction_op2:

odd_instruction_op2
===================

Syntax
------

.. code-block:: js

    odd_instruction_op2(instruction)

Parameters
----------
+-----------+------------------------------------------------------------------------------+
|Name       |Description                                                                   |
+===========+==============================================================================+
|instruction|The :ref:`Instruction<i_gms2_class_instruction>` to get the second operand of.|
+-----------+------------------------------------------------------------------------------+

Returns
-------

:code:`Number|Undefined`: The second operand of the given instruction.

Description
-----------

This function gets the second operand of the given Instruction, if any.

Example
-------

.. code-block:: js

    var inst = odd_create_instruction(odd_opcode.DebugLine, 20, undefined);

    show_debug_message(string(odd_instruction_op1(inst)));

    // ...

This would print "undefined" to the console.