.. VLinux theme documentation master file, created by
   sphinx-quickstart on Sun Jun 26 13:50:50 2011.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Solar theme's documentation!
========================================

About
-----
Solar is an attempt to create a theme for Python_ Sphinx_ based on the 
`Solarized <http://ethanschoonover.com/solarized>`_ color scheme.

Requirements
------------
* `Solarized dark pygments style <http://gthank.github.com/solarized-dark-pygments/>`_


Syntax Highlight
----------------

.. code-block:: python

    class Dlg(QDialog, Ui_Dialog):
        def __init__(self, parent=None):
            super(Dlg, self).__init__(parent)
            self.setupUi(self)
            self.dockWidget.hide()
            self.fileLineEdit.setDisabled(True)
            self.fileButton.setDisabled(True)
            
            self.closeButton.clicked.connect(self.close)
            self.buildButton.clicked.connect(self.build)
            self.fileButton.clicked.connect(self.getFile)
            self.fileRadioButton.toggled.connect(self.fileLineEdit.setEnabled)
            self.fileRadioButton.toggled.connect(self.fileButton.setEnabled)
            self.logButton.toggled.connect(self.dockWidget.setVisible)
            
            for button in (self.sourceButton, self.outputButton):
                button.clicked.connect(self.getDirectory)
                
            self.sourceDirectory = None
            self.outputDirectory = None
            
            self.process = QProcess()
            self.process.readyReadStandardOutput.connect(self.readOutput)
            self.process.readyReadStandardError.connect(self.readErrors)
            
            #restore settings
            settings = QSettings()
            size = settings.value('Dialog/Size', QVariant(QSize(600, 500))).toSize()
            self.resize(size)
            pos = settings.value('Dialog/Position', QVariant(QPoint(0, 0))).toPoint()
            self.move(pos)

            for widget, setting in ((self.sourceLineEdit, 'Data/SourceDirectory'),
                                  (self.outputLineEdit, 'Data/OutputDirectory')):
                widget.setText(settings.value(setting).toString())


Others
------

.. note::
    
    Here is a note!

.. warning::

    There can be warnings too!

Todo
----
* Fix the print preview


How to use
----------
#. Download `solar-theme-0.1.zip <http://www.github.com/vkvn/sphinx-themes/download/solar-theme-0.1.zip>`_ and uncompress the archive.
#. Modify the ``conf.py`` of an existing Sphinx project or create a new 
   Sphinx project using ``sphinx-quickstart``.
#. Change the ``html_theme`` parameter to ``solar``.
#. Change the ``html_theme_path`` to location of the downloaded theme.


.. links
.. _Python: http://www.python.org
.. _Sphinx: http://sphinx.pocoo.org/

