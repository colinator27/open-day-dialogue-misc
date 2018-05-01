.. _i_gms2_func_odd_create_instruction:

odd_create_instruction
======================

Syntax
------

.. code-block:: js

    odd_create_instruction(opcode, operand1, operand2)

Parameters
----------
+--------+-----------------------------------------------------------------------------+
|Name    |Description                                                                  |
+========+=============================================================================+
|opcode  |The :ref:`odd_opcode<i_gms2_enum_odd_opcode>` the Instruction is meant to do.|
+--------+-----------------------------------------------------------------------------+
|operand1|The first operand, if any, for the specified opcode.                         |
+--------+-----------------------------------------------------------------------------+
|operand2|The second operand, if any, for the specified opcode.                        |
+--------+-----------------------------------------------------------------------------+

Returns
-------

:code:`Instruction`: The reference to the new :ref:`Instruction<i_gms2_class_instruction>`. There is no need to free or delete it, because of how it is handled internally.

Description
-----------

Creates a new Instruction with the specified parameters, returning its reference

Example
-------

.. code-block:: js

    var inst = odd_create_instruction(odd_opcode.DebugLine, 20, undefined);

    // . . .

This would create a new Instruction with the DebugLine :ref:`opcode<i_gms2_enum_odd_opcode>`, with the first operand being 20.