.. _i_gms2_func_odd_load_binary_from_buffer:

odd_load_binary_from_buffer
===========================

Syntax
------

.. code-block:: c
   
   odd_load_binary_from_buffer(buffer)
   
Parameters
----------
+-----------+----------------------+
|Name       |Description           |
+===========+======================+
|buffer     |The buffer to read    |
|           |from, containing a    |
|           |valid ODD binary.     |
+-----------+----------------------+
   
Returns
-------

The reference to the binary file instance, typically a **Real**. This should be stored in a variable, and cleaned up by :ref:`odd_unload_binary<i_gms2_func_odd_unload_binary>` later.

Description
-----------

This function creates a new binary file instance, given a pre-existing buffer. The buffer *must* be the contents of a valid ODD binary, and must be 1-byte aligned.

.. note:: The buffer you input will not be automatically deleted;
          you must delete/free it yourself.

.. attention:: The value of the function should be stored in a variable, 
               and cleaned up by :ref:`odd_unload_binary<i_gms2_func_odd_unload_binary>` 
               later. This will free the memory used, preventing possible
               memory leaks.

Example
-------

.. code-block:: c
   
   var buff = buffer_load("english.opdac");
   var binary = odd_load_binary_from_buffer(buff);
   buffer_delete(buff);
   
   // ...
   
This example would create a new binary file instance from an ODD binary file named "english.opdac". It loads the file into the buffer manually, instead of letting ODD handle it (see :ref:`odd_load_binary<i_gms2_func_odd_load_binary>` if you do not wish for this). The variable :code:`binary` would contain the reference to the binary file instance, which can be used by other functions.