.. _i_gms2_func_odd_unload_binary:

odd_unload_binary
=================

Syntax
------

.. code-block:: c
   
   odd_unload_binary(filename)
   
Parameters
----------
+-----------+----------------------+
|Name       |Description           |
+===========+======================+
|binary     |The reference to the  |
|           |binary file instance. |
+-----------+----------------------+
   
Returns
-------

N/A

Description
-----------

This function unloads/frees a binary file instance that was loaded by either :ref:`odd_load_binary<i_gms2_func_odd_load_binary>` or :ref:`odd_load_binary_from_buffer<i_gms2_func_odd_load_binary_from_buffer>`.

The binary can no longer be used, and any instances that are using it will no longer work, and can crash the game. It is recommended you free those instances as well, through :ref:`odd_destroy_instance<i_gms2_func_odd_destroy_instance>`.

.. note:: If you need to dynamically change a binary, for instance,
          swapping languages, you must free the previous binary using
          this function beforehand. Otherwise, a memory leak can occur,
          or the game will simply be wasting memory in general.

Example
-------

.. code-block:: c
   
   // When the game loads:
   
   var binary = odd_load_binary("english.opdac");
   
   // Later on, when the game closes, or the binary has to change (or is no longer in use):
   
   odd_unload_binary(binary);
   
This example would load a binary file when the game starts, and later on, unload it due to it no longer being needed.