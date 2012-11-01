.. Template for sphinx-themes documentation master file, created by
   sphinx-quickstart2 on Thu Nov  1 19:54:49 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

sphinx-themes
=============

These are some themes for Python `Sphinx <http://sphinx.pocoo.org/>`_
documentation projects.

Preview
-------
To see how these themes look, visit http://vimalkumar.in/sphinx-themes

Download
--------
Released versions are available from https://github.com/vkvn/sphinx-themes/downloads

You can also download this repository as a `zip archive <https://github.com/vkvn/sphinx-themes/zipball/master>`_

Support
-------
If there are problems with any of these themes, you can file a bug report at
https://github.com/vkvn/sphinx-themes/issues

Themes are licensed under the
`GNU General Public License <http://www.gnu.org/licenses/gpl.html>`_.


.. raw:: html

   <iframe style="border: 0; margin: 0; padding: 0;"
           src="https://www.gittip.com/vkvn/widget.html"
           width="48pt" height="22pt"></iframe>

   <a href="http://coderwall.com/vkvn"><img alt="Endorse vkvn on Coderwall" src="http://api.coderwall.com/vkvn/endorsecount.png" /></a>

Styles
------

* List element 1
* List element 2

Code snippet::

	from fabric.api import local

	def run_rcc():
		"""Generate resources file"""
		local("pyrcc4 -o resources_rc.py ui/resources.qrc")

	def run_uic():
		"""Process ui file"""
		local("pyuic4 -o ui_window.py ui/window.ui")
	

Admonition levels
-----------------

Note
....

.. note::
    
    This is a note!

Hint, Tip
.........

.. hint::

   This can be a hint.
  
Warning, Important
.................. 

.. warning::

    There can be warnings too!
   
Caution, Attention, Danger and Error
....................................
    
.. attention::

   Requires your attention.

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

