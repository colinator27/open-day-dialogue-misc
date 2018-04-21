.. _i_gms2_func_odd_format_version:

odd_format_version
==================

Syntax
------

.. code-block:: c
   
   odd_format_version()
   
Returns
-------

The format version, as type **Real**.

Description
-----------

This function returns the binary file format version that the interpreter understands.

Example
-------

.. code-block:: c
   
   show_debug_message("Open Day Dialogue version: " + string(odd_format_version()));
   
This example would log the version of the binary format that this interpreter supports to the console.
It would be something like :code:`Open Day Dialogue version: 4`.