.. _i_gms2_class_command:

Class: Command
==============

The Command class (which the Function class extends) is a storage class meant to hold data for Commands or Functions, mainly their Name and their Arguments

You can create a Command with:

.. toctree::
    :maxdepth: 1

    func_odd_create_command

You can get the Command's name with:

.. toctree::
    :maxdepth: 1

    func_odd_command_name

You can get the Command's arguments with:

.. toctree::
    :maxdepth: 1

    func_odd_command_args

.. warning:: You shouldn't **need or want** to use this class, as it's mainly used internally, however if you do, do not access the data directly, instead use the aforementioned :ref:`odd_command_name<i_gms2_func_odd_command_name>` and :ref:`odd_command_args<i_gms2_func_odd_command_args>`.