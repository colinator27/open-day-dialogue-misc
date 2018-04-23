GameMaker Studio 2 Interpreter
==============================

This interpreter is for GameMaker Studio 2 projects. It is as close to the other interpreters as possible, however, as GameMaker has no lightweight objects or classes, everything is somewhat C-style.

This means to create, for instance, a Value, you would need to use a function which would return a handle to it. You would then have to use other functions to get information from it.

.. toctree::
    :maxdepth: 1
    :caption: Functions and classes
    
    func_odd_format_version
    
    binary/index
    instance/index
    value/index
    command/index
    instruction/index
    
.. toctree::
    :maxdepth: 1
    :caption: Enumerators and macros
    
    macro_odd_type
    enum_odd_opcode
    
