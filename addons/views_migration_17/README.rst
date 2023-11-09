.. image:: https://img.shields.io/badge/licence-AGPL--3-blue.svg
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. image:: https://img.shields.io/badge/python-3.6-blue.svg
    :alt: Python support: 3.6
.. image:: https://app.travis-ci.com/OCA/odoo-module-migrator.svg?branch=master
    :target: https://app.travis-ci.com/OCA/odoo-module-migrator

====================
Views-migration-v17
====================

``views-migration-v17`` is a odoo server mode module that allows you to automatically migrate the views of a Odoo module versión <= v16 to v17 .

For example:

.. code-block:: xml

    <field name="test_field_1" attrs="{'invisible': [('active', '=', True)]}"/>
    <field name="test_field_2" attrs="{'invisible': [('zip', '!=', 123)]}"/>
    <field name="test_field_3" attrs="{'readonly': [('zip', '!=', False)]}"/>

To:

.. code-block:: xml

    <field name="test_field_1" invisible="active"/>
    <field name="test_field_2" invisible="zip != 123"/>
    <field name="test_field_3" readonly="zip"/>


Usage
=====

.. code-block:: shell

    odoo -d database -u module_to_migrate --load views_migration_17


Credits
=======

Authors
-------


Contributors
------------

