.. include:: ../Includes.txt
.. highlight:: rst

.. _general-conventions-dir-and-filenames:

=====================
Directories and Files
=====================

Directory and File Names
========================

* All documentation resides in a :file:`Documentation` subfolder
* This folder contains the files :file:`Settings.cfg`, :file:`Includes.txt` and :file:`Index.rst`
* Use **CamelCase** for file and directory names.
* reSt files have ending **.rst**
* Included files have ending **.rst.txt**


.. code-block:: none

  Documentation/
  |
   --> Settings.cfg
  |
   --> Includes.txt
  |
   --> Index.rst
  |
   --> Topic1/
         |
         -> Index.rst
         -> Subtopic1.rst
         -> Subtopic2.rst

If the documentation follows these conventions, the documentation rendering toolchain
automatically detects the documentation and renders it correctly on the documentation
server.

It is **strongly recommended** to do it the way it is described here.
For alternatives, please look at :ref:`supported-filenames-and-formats`.


Required  Files
===============

At least the files :file:`Settings.cfg`, :file:`Includes.txt` and
:file:`Index.rst` are required in the :file:`Documentation` folder (at least
if you are creating an entire sphinx project and not a single-file solution).

The rest of the files listed here are optional, but strongly recommended.

.. _settings-cfg:

Settings.cfg
------------

:file:`Documentation/Settings.cfg`

.. important::
   This file must be adapted for the manual.

It contains some meta information. It also
contains start urls for the intersphinx linking mechanism.

* Use  `Settings.cfg
  <https://github.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/blob/master/Documentation/Settings.cfg>`__
  in this project as an up-to-date example for an official manual!
* Use the file in `TYPO3CMS-Example-ExtensionManual
  <https://github.com/TYPO3-Documentation/TYPO3CMS-Example-ExtensionManual/blob/latest/Documentation/Settings.cfg>`__
  as an up-to-date example for an extension manual!

The file consists of sections, which start with a keyword in brackets, such as `[general]`.
Make sure that all directives exist in the correct section.

We are showing the contents of this manual's Settings.cfg by using the
`literalincludes` directive.

.. literalinclude:: ../Settings.cfg
   :linenos:



.. _includes-txt:

Includes.txt
------------

:file:`Documentation/Includes.txt`

This file can be the same for all Documentation projects!

Use `Includes.txt <https://github.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/blob/master/Documentation/Includes.txt>`__
from this project as an up-to-date example.

We are showing the contents of this manual's Includes.txt by using the
`literalincludes` directive.

.. literalinclude:: ../Includes.txt
   :linenos:




.. _index-rst:

Index.rst
---------

:file:`Documenation/Index.rst`

.. important::

   This file must be adapted for the manual.

It contains text that is displayed on the start page
as well as the toctree.

Use `Index.rst <https://github.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/blob/master/Documentation/Index.rst>`__
in this manual as an example.

Minimal Example
~~~~~~~~~~~~~~~

.. code-block:: rest
   :linenos:

      .. include:: Includes.txt

      =================
      T3DocTeam at Work
      =================

      some text


   .. toctree::
      :hidden:

      Introduction/Index
      Configuration/Index


* line 1 : every .rst file should include Includes.txt
* line 3-5: the header
* line 10-14: the toctree, which specifically includes the files
  :file:`Introduction/Index.rst`, :file:`Configuration/Index.rst`

Complete Example
~~~~~~~~~~~~~~~~

We are showing the contents of this manual's Includes.txt by using the
`literalincludes` directive.

.. literalinclude:: ../Index.rst
   :linenos:


.. _editorconfig-in-filenames:

.editorconfig
-------------

:file:`.editorconfig`

For more information, see :ref:`editorconfig`.

Use the file in `this manual: .editorconfig
<https://github.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/blob/master/.editorconfig>`__
as an example.

.. _gitignore-in-filenames:

.gitignore
----------

:file:`.gitignore`

All files listed in .gitignore will be ignored by Git. This is useful for generated files,
that should not be added to your repository or for temporary files (e.g. backup files of
your editor).

You can ignore additional files by adding them to your .git/info/exclude file.

.gitignore will apply to anyone using the repository, .git/info/exclude is for yourself
only and will not be included in the repository on GitHub when you push.

Use the file in `this manual: .gitignore
<https://github.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/blob/master/.gitignore>`__ as a template.

Minimal Example
~~~~~~~~~~~~~~~

.. code-block:: none

   # Git global ignore file
   # for local exclude patterns please edit .git/info/exclude
   # Example file see https://github.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/blob/master/.gitignore

   # ignore generated documentation
   *GENERATED*

.. _readme-rst:

README.rst
----------

This file will be displayed on GitHub when someone browses through the
repositories. Use `README.rst <https://github.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/blob/master/README.rst>`__
from this project as an example! (see `source <https://raw.githubusercontent.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/master/README.rst>`__).

The link "Read online" will help people to jump directly to the rendered version.

.. _contributing-rst:

CONTRIBUTING.rst
----------------

This file should contain some information about contributing to the documentation.

You can name it CONTRIBUTING.md or CONTRIBUTING.rst, but as we commonly use reST
here, it is best to stick to CONTRIBUTING.rst.

Again, use `CONTRIBUTING.rst <https://github.com/TYPO3-Documentation/TYPO3CMS-Guide-HowToDocument/blob/master/CONTRIBUTING.rst>`__
from this manual.

A link to the file will automatically displayed by GitHub when someone enters the
"Issues" area (and has not created an issue yet) or when someone creates an issue.
