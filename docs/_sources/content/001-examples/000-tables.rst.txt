******
Tables
******

Simple tables
=============

- First column cells cannot be multiple lines
- Must contain more than 1 row

=======  =====
name     age
=======  =====
Alice    42
Bob      99
=======  =====


.. code-block:: rst

    =======  =====
    name     age
    =======  =====
    Alice    42
    Bob      99
    =======  =====




Grid Table Syntax
=================

.. code-block:: rst

    +-------+-----+
    | name  | age |
    +=======+=====+
    | Alice | 42  |
    +-------+-----+
    | Bob   | 99  |
    +-------+-----+

Result:

+-------+-----+
| name  | age |
+=======+=====+
| Alice | 42  |
+-------+-----+
| Bob   | 99  |
+-------+-----+



Sublime shortcuts for OSX
=========================

Using the `Sublime Text rst-completion plugin <https://github.com/mgaitan/sublime-rst-completion#magic-tables>`_:


Grid table rst-completion
-------------------------

:kbd:`Command-Shift-t`, :kbd:`Enter`

https://github.com/mgaitan/sublime-rst-completion#grid-table


hello    world
foo      use 2+ spaces as a delimiter
bar      then do cmd-shift-t, enter

+-------+------------------------------+
| hello | world                        |
+=======+==============================+
| foo   | use 2+ spaces as a delimiter |
+-------+------------------------------+
| bar   | then do cmd-shift-t, enter   |
+-------+------------------------------+


Simple table rst-completion
---------------------------

:kbd:`Command-Shift-t`, :kbd:`s`

https://github.com/mgaitan/sublime-rst-completion#simple-table





References
==========

`Tables: Miscellaneous Markup, Sphinx Documentation <http://www.sphinx-doc.org/en/stable/markup/misc.html#tables>`_

`Tables: Restructured Text Primer, Sphinx Documentation <http://www.sphinx-doc.org/en/stable/rest.html#rst-tables>`_

`Tables, RestructuredText Docs <http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#tables>`_

`RST Cheatsheet: Tables <http://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html#tables>`_

`Magic Tables from RST Completion Sublime plugin <https://github.com/mgaitan/sublime-rst-completion#magic-tables>`_
