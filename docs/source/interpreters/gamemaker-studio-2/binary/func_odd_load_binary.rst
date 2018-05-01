.. _i_gms2_func_odd_load_binary:

odd_load_binary
===============

Syntax
------

.. code-block:: c
   
   odd_load_binary(filename)
   
Parameters
----------
+-----------+----------------------+
|Name       |Description           |
+===========+======================+
|filename   |The name of the       |
|           |file to load.         |
+-----------+----------------------+
   
Returns
-------

:code:`Binary`: The reference to the binary file instance, typically a **Real**. This should be stored in a variable, and cleaned up by :ref:`odd_unload_binary<i_gms2_func_odd_unload_binary>` later.

Description
-----------

This function creates a new binary file instance, given a file name. The file must be visible to GameMaker's sandboxed filesystem.

.. attention:: The value of the function should be stored in a variable, 
               and cleaned up by :ref:`odd_unload_binary<i_gms2_func_odd_unload_binary>` 
               later. This will free the memory used, preventing possible
               memory leaks.

Example
-------

.. code-block:: c
   
   var binary = odd_load_binary("english.opdac");
   
   // ...
   
This example would create a new binary file instance from an ODD binary file named "english.opdac". The variable :code:`binary` would contain the reference to the binary file instance, which can be used by other functions.