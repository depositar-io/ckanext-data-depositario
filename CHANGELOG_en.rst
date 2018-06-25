.. This tocdepth stops Sphinx from putting every subsection title in this file
   into the master table of contents.

:tocdepth: 1

---------
Changelog
---------

v6.1.2 2018-05-10
=================

 * Update: CKAN core version 2.6.6.

v6.1.1 2018-04-23
=================

 * Add: Documentation in footer (Chinese only at present).

v6.1.0 2018-03-23
=================

 * Add: Site status in footer.
 * Improvement: Fix the wrong positive_float_validator validator.
 * Improvement: Apply the suitable validators to schema fields.
 * Improvement: Add LineString support to map for filling spatial extent.
 * Improvement: Add edit and delete tools to map for filling spatial extent.
 * Update: Leaflet.draw 0.4.1.
 * Update: CKAN core version 2.6.5.
 * Move the Wikidata-powered keyword function to an extension: https://github.com/depositar-io/ckanext-wikidatakeyword.
 * Other improvements and UI adjustments.

v6.0 2017-11-03
===============

 * Add: A Keywords field, which integrates wikidata entries, replaces the old theme and spatial keywords.
 * Add: System will generate a hash if the new dataset's title can not be slugfied.
 * Update: CKAN core version 2.6.4.
 * Other improvements and UI adjustments.

v5.0.x 2017-09-05
=================

 * Improvement: Simplified metadata with three categories – basic information, descriptive Information, and management information. Add Remarks to replace Reference and Sub Project. Move Encoding to resource level. Remove some fields which are not often used.
 * Improvement: After a user fills in Spatial field using a map, system will generate geojson value and parcel corner and lock those fields.
 * Improvement: Maintainer and Maintainer Email can be filled in with logged-in account information.
 * Improvement: Add a checkbox to open a dataset for organization members only.
 * Improvement: Separate translations for our custom extension from CKAN core thanks to CKAN 2.5's translation capabilities for extensions.
 * Update: ckanext-pages verison with zh_TW language.
 * Update: CKAN core version 2.6.3.
 * Other improvements and UI adjustments.