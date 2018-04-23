.. _i_gms2_class_insturction:

Class: Instruction
==================

The Instruction class is a storage class meant to hold data that tells the Interpreter what to do.

.. warning:: You should not, **by any means**, need to use this class in a game. However if you do use this class, do not access the data directly, instead use the :ref:`odd_instruction_opcode<i_gms2_func_odd_instruction_opcode>`, :ref:`odd_instruction_op1<i_gms2_func_odd_instruction_op1>`, and :ref:`odd_instruction_op2<i_gms2_func_odd_instruction_op2>` functions.

Instructions can be created with:

.. toctree::
    :maxdepth: 1

    func_odd_create_instruction

And it's data can be accessed with:

.. toctree::
    :maxdepth: 1

    func_odd_instruction_opcode
    func_odd_instruction_op1
    func_odd_instruction_op2
