.. _i_gms2_class_instance

Class: Instance
===============

.. warning:: This page is currently incomplete. It is
             missing most of the important functions.

Instances, not to be confused with binary file instances, are the actual virtual machines that perform the "magic" that run dialogue and get definitions.

Instances be created with the following function:

.. toctree::
   :maxdepth: 1
   
   func_odd_create_instance

Instances can be unloaded/destroyed with this function:

.. toctree::
   :maxdepth: 1
   
   func_odd_destroy_instance
   
These are the main instance functions:

.. toctree::
   :maxdepth: 1
   
   func_odd_instance_run_scene
   func_odd_instance_stop_scene
   func_odd_instance_resume
   func_odd_instance_pause
   func_odd_instance_select_choice
   func_odd_instance_command_add
   func_odd_instance_function_add
   func_odd_instance_get_definition
   func_odd_instance_get_definition_string

These are some more advanced instance functions, that are only sometimes necessary:

.. toctree::
   :maxdepth: 1
   
   func_odd_instance_update
   func_odd_instance_run_instruction

You can get variables from instances through these functions:

.. toctree::
   :maxdepth: 1
   
   func_odd_instance_get_current_scene
   func_odd_instance_get_current_text
   func_odd_instance_get_paused
   func_odd_instance_get_in_choice
   func_odd_instance_get_binary
   func_odd_instance_get_store_setter
   func_odd_instance_get_store_getter
   func_odd_instance_get_store_cleanup
   func_odd_instance_get_handler_text
   func_odd_instance_get_handler_choice
   func_odd_instance_get_processor_text
   func_odd_instance_get_processor_choice
   func_odd_instance_get_processor_definition

You can set some variables in instances through these functions:

.. toctree::
   :maxdepth: 1
   
   func_odd_instance_set_store_setter
   func_odd_instance_set_store_getter
   func_odd_instance_set_store_cleanup
   func_odd_instance_set_handler_text
   func_odd_instance_set_handler_choice
   func_odd_instance_set_processor_text
   func_odd_instance_set_processor_choice
   func_odd_instance_set_processor_definition
   
.. attention:: It is recommended that you destroy an Instance once it is no longer in use.