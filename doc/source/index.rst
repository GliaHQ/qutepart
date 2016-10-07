.. automodule:: qutepart

.. autoclass:: qutepart.Qutepart
    :members:

Helper functions
^^^^^^^^^^^^^^^^
.. autofunction:: qutepart.iterateBlocksFrom
.. autofunction:: qutepart.iterateBlocksBackFrom

Logging
^^^^^^^
Package logs it's debug information to ``qutepart`` logger.
By default logger prints messages to stderr with ``qutepart:`` prefix.
For performance reasons, parser in C:

    * checks, if DEBUG logs are enabled only when created
    * always prints logs to stderr
    * always prints ERROR logs
    * always uses ``qutepart:`` prefix

Logging handler is available as ``consoleHandler`` attribute of the package

API Version
^^^^^^^^^^^
API version is available as ``qutepart.VERSION``. It is a tuple ``(major, minor, patch)``

* Major versions might be incompatible.
* Minor versions add new API, but remain backward compatilbe
* Patch versions does not change API

Binary parser
^^^^^^^^^^^^^
Qutepart has 2 text parsers - slower in Python, and quicker in C. If C parser has been successfully loaded, ``qutepart.binaryParserAvailable`` is True


Margins
^^^^^^^
Qutepart supports margins on the left hand side of the editor pane.
Please see the `Margins Support <CustomMargins.html# Margins Support>`__ section
for more details.

