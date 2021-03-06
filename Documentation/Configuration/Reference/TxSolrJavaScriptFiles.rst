.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


.. raw:: latex

    \newpage

.. raw:: pdf

   PageBreak

.. _conf-tx-solr-javascriptFiles:

tx_solr.javascriptFiles
=======================

.. contents::
   :local:

Here you can configure what Javascript files you want to use for different areas
of the extension. The section is a definition of key-value pairs where the key
is the name of a part of the extension and the value points to the Javascript
file to be used for styling it.

In general we use jQuery as the default Javascript framework, but through this
configuration you are free to use any other framework you like.

To prevent loading of a file just set it empty like this:

|

.. code-block:: typoscript

   plugin.tx_solr.javascriptFiles.library =

|

or clear the setting like this:

|

.. code-block:: typoscript

   plugin.tx_solr.javascriptFiles.library >

|

To prevent the extension from loading any default Javascript files simple clear
the whole javascriptFiles settings:

|

.. code-block:: typoscript

   plugin.tx_solr.javascriptFiles >

|

loadIn
------

:Type: String
:TS Path: plugin.tx_solr.javascriptFiles.loadIn
:Default: footer
:Options: header, footer, none
:Since: 2.2

Controls where to load the Javascript files, load Javascript in the header, the
footer or not at all if you want to take care of it manually.

library
-------

:Type: String
:TS Path: plugin.tx_solr.javascriptFiles.library
:Default: EXT:solr/Resources/JavaScript/JQuery/jquery.min.js
:Since: 2.0

Defines the general Javascript library to use. By default this is jQuery.

ui
--

:Type: String
:TS Path: plugin.tx_solr.javascriptFiles.ui
:Default: EXT:solr/Resources/JavaScript/JQuery/jquery-ui.min.js
:Since: 6.1

Defines the user interface components library to use. By default this is jQuery UI.
This is minified and concatenated jQuery UI, which includes following components:

   widget
   position
   keycode
   unique-id
   widgets/autocomplete
   widgets/datepicker
   widgets/menu
   widgets/mouse
   widgets/slider

ui.datepicker
-------------

The date picker in jQuery UI is localizable, the localization labels are defined
in separate files which are loaded depending on the current page's language.
The localization label files are defined as followed:

|

.. code-block:: typoscript

   plugin.tx_solr.javascriptFiles.ui.datepicker {
     de = EXT:solr/Resources/JavaScript/JQuery/ui-i18n/jquery.ui.datepicker-de.js
     fr = EXT:solr/Resources/JavaScript/JQuery/ui-i18n/jquery.ui.datepicker-fr.js
     nl = EXT:solr/Resources/JavaScript/JQuery/ui-i18n/jquery.ui.datepicker-nl.js
   }

suggest
-------

:Type: String
:TS Path: plugin.tx_solr.javascriptFiles.suggest
:Default: EXT:solr/Resources/JavaScript/EidSuggest/suggest.js
:Since: 2.0

Defines the suggest Javascript file used in autocomplete / suggest to make the
actual request from the website through the TYPO3 eID script to Solr and back.

faceting.limitExpansion
-----------------------

:Type: String
:TS Path: plugin.tx_solr.javascriptFiles.faceting.limitExpansion
:Default: EXT:solr/Resources/JavaScript/PiResults/results.js
:Since: 2.0

A small script used for the collapse/expand feature of facet option lists.

faceting.dateRangeHelper
------------------------

:Type: String
:TS Path: plugin.tx_solr.javascriptFiles.faceting.dateRangeHelper
:Default: EXT:solr/Resources/JavaScript/PiResults/date_range_facet.js
:Since: 2.0

A small glue script used with date range facets and the date picker.

faceting.numericRangeHelper
---------------------------

:Type: String
:TS Path: plugin.tx_solr.javascriptFiles.faceting.numericRangeHelper
:Default: EXT:solr/Resources/JavaScript/PiResults/numeric_range_facet.js
:Since: 2.0

A small glue script used with numeric range facets and the slider.
