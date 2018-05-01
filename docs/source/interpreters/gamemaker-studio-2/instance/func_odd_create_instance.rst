.. _i_gms2_func_odd_create_instance:

odd_create_instance
===================

Syntax
------

.. code-block:: js
   
   odd_create_instance(binary, vs_setVariable, vs_getVariable, vs_cleanUp[, handleText, handleChoice, textMainProcessor, textChoiceProcessor, textDefProcessor])
   
Parameters
----------
+-------------------+----------------------+
|Name               |Description           |
+===================+======================+
|binary             |The reference to the  |
|                   |binary file instance  |
|                   |that the new instance |
|                   |will use.             |
+-------------------+----------------------+
|vs_setVariable     |The script that will  |
|                   |be called when ODD    |
|                   |code sets a variable. |
|                   |                      |
|                   |Script arguments:     |
|                   |                      |
|                   |**argument0**:        |
|                   |variable name         |
|                   |                      |
|                   |**argument1**: value  |
+-------------------+----------------------+
|vs_getVariable     |The script  that will |
|                   |be called when ODD    |
|                   |code gets a variable's|
|                   |value. Should return  |
|                   |a :code:`Value`.      |
|                   |                      |
|                   |Script arguments:     |
|                   |                      |
|                   |**argument0**:        |
|                   |variable name         |
+-------------------+----------------------+
|vs_cleanUp         |The script that will  |
|                   |be called when ODD    |
|                   |requests that         |
|                   |variables and their   |
|                   |values be cleared.    |
+-------------------+----------------------+
|handleText         |The script that will  |
|*(optional)*       |be called when ODD    |
|                   |code runs into a new  |
|                   |line of dialogue.     |
|                   |You would use this to,|
|                   |for instance, show    |
|                   |a new dialogue box.   |
|                   |                      |
|                   |Script arguments:     |
|                   |                      |
|                   |**argument0**: text,  |
|                   |as a string           |
+-------------------+----------------------+
|handleChoice       |The script that will  |
|*(optional)*       |be called when ODD    |
|                   |code runs into a new  |
|                   |dialogue choice.      |
|                   |You would use this to,|
|                   |for instance, show    |
|                   |a list of choices     |
|                   |to the game screen.   |
|                   |                      |
|                   |Script arguments:     |
|                   |                      |
|                   |**argument0**: array  |
|                   |of choices, as strings|
+-------------------+----------------------+
|textMainProcessor  |The script that will  |
|*(optional)*       |be called to process  |
|                   |lines of dialogue     |
|                   |before they are in    |
|                   |effect. The script    |
|                   |should return the     |
|                   |processed text as     |
|                   |a string.             |
|                   |                      |
|                   |Script arguments:     |
|                   |                      |
|                   |**argument0**:        |
|                   |non-processed text,   |
|                   |as a string           |
+-------------------+----------------------+
|textChoiceProcessor|The script that will  |
|*(optional)*       |be called to process  |
|                   |lines of dialogue     |
|                   |*inside of choices*   |
|                   |before they are in    |
|                   |effect. The script    |
|                   |should return the     |
|                   |processed text as     |
|                   |a string.             |
|                   |                      |
|                   |Script arguments:     |
|                   |                      |
|                   |**argument0**:        |
|                   |non-processed text,   |
|                   |of a singular choice, |
|                   |as a string           |
+-------------------+----------------------+
|textDefProcessor   |The script that will  |
|*(optional)*       |be called to process  |
|                   |strings in definitions|
|                   |before they are used. |
|                   |The script            |
|                   |should return the     |
|                   |processed text as     |
|                   |a string.             |
|                   |                      |
|                   |Script arguments:     |
|                   |                      |
|                   |**argument0**:        |
|                   |non-processed text,   |
|                   |of a singular         |
|                   |definition, as a      |
|                   |string                |
+-------------------+----------------------+
   
Returns
-------

:code:`Instance`: The reference to the instance, typically a **Real**. This should be stored in a variable, and cleaned up by :ref:`odd_destroy_instance<i_gms2_func_odd_destroy_instance>` later.

Description
-----------

This function creates a new instance, given a :ref:`binary file instance<i_gms2_class_binary>` and other parameters (such as the variable store scripts and callbacks).

.. attention:: The value of the function should be stored in a variable, 
               and cleaned up by :ref:`odd_destroy_instance<i_gms2_func_odd_destroy_instance>` 
               later. This will free the memory used, preventing possible
               memory leaks.

Example
-------

.. code-block:: js
   
   // Load the binary file
   var binary = odd_load_binary("english.opdac");
   
   // Create the instance
   var inst = odd_create_instance(binary, scr_varstore_set, scr_varstore_get, scr_varstore_clean, scr_handletext);
   
This example would create a new binary file instance from an ODD binary file named "english.opdac", and use it to create an instance. The instance uses several scripts as callbacks to the parameters (:code:`scr_varstore_set, scr_varstore_get, scr_varstore_clean, scr_handletext`).