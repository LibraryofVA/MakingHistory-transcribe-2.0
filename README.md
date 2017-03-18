Making History: Transcribe 2.0,
=====================

Transcribe is built upon the open-source generosity of George Mason University's [Center for History and New Media](http://chnm.gmu.edu/) and was an original creation by the amazing staff at [The University of Iowa Libraries](http://www.lib.uiowa.edu/). Their project, DIYHistory|transcribe, can be found at [http://diyhistory.lib.uiowa.edu/](http://diyhistory.lib.uiowa.edu/) with their github repository located at [github.com/ui-libraries](https://github.com/ui-libraries). A pervious version of this project can be found at [Making History: Transcribe](https://github.com/LibraryofVA/MakingHistory-transcribe).

Overview
--------
[Making History - Transcribe](http://www.virginiamemory.com/transcribe/) is a tool for engaging users in transcribing handwritten documents, making them more searchable and enhancing them for research. Transcribe is built on the [Omeka](http://omeka.org/) content management system and uses the [Scripto](http://scripto.org/) plugin to facilitate transcription. [Scripto](http://scripto.org/) uses [MediaWiki](http://www.mediawiki.org/wiki/MediaWiki), which allows users to continually improve upon work that has already been done. UI-Libraries made significant additions to the Scripto plugin, created a new Omeka theme, and customized other Omeka plugins to style and scale for a library production environment. In this project the Library of Virginia is completing further customizations and updating software to the versions listed below.

##Requirements
Transcribe was built on the following:

+ [Omeka](http://omeka.org/codex/Version_History) version 2.4.1
+ [Omeka Dublin Core Extended plugin](http://omeka.org/add-ons/plugins/dublin-core-extended/) version 2.0.1
+ [Daniel-KM/CsvImport](https://github.com/Daniel-KM/CsvImport), a fork of Omeka's CsvImport that allows bulk upload of item and file-level metadata
+ [LibraryofVA/plugin-Scripto-2.0](https://github.com/LibraryofVA/plugin-Scripto-2.0), a fork of [ui-libraries/plugin-Scripto](https://github.com/ui-libraries/plugin-Scripto), which was orginally forked from CHNM's Scripto tool for crowd sourced transcription of documents
+ [LibraryofVA/plugin-Export-2.0](https://github.com/LibraryofVA/plugin-Export-2.0), Export was designed specifically for use by the Library of Virginia to extract transcription data to then be imported into a digital asset management system adding full text search capability
+ [MediaWiki](http://www.mediawiki.org/wiki/MediaWiki) version 1.26.4
+ [LibraryofVA/Scribe-2.0](https://github.com/LibraryofVA/Scribe-2.0), a fork of [ui-libraries/Scribe](https://github.com/ui-libraries/Scribe) custom Omeka theme

Features
--------
[UI-Libraries](http://www.lib.uiowa.edu/) introduced the following features to plugin-Scripto:

- Track completion status of document pages (i.e., 'Not Started', 'Needs Review', 'Completed')
- Track completion progress of documents based on page statuses.
- Sort documents within their collection by most completed, floating least completed to the top.
- Initialize document page text entry box with pre-existing text, if available (helpful if using Scripto to correct OCR for typescript pages).
- On every page action, automatically import transcriptions from MediaWiki as file metadata.


The [Scribe](https://github.com/ui-libraries/Scribe) theme directs its focus on guiding users to easy transcription tasks rather than collection management features, offering a clean, thumbnail-oriented transcription view for any number of Omeka image collections.

By default, any member of the public is allowed to edit and save transcription data, but only users with an account can track their progress. Approved account holders can also be granted administrator (or deputy) status, allowing them to finalize documents as "complete".

[The Library of Virginia](http://www.lva.virginia.gov/) added the following features:

- Update to OpenLayers 3.0
- Horizontal/Vertical display toggle ability along with resize buttons for OpenLayers object.
- Removed Wiki anonymous editing ability and control anonymous edits through Scripto with a user account ultimately reducing spam.
- Autosave, results in more timely update of document status which reduces duplicate efforts of transcribers.
- Altered MediaWiki group structure reducing deputized public approvers from administrator to a more suitable role.
- Export capability to extract transcription information from Omeka.

Installation
------------
Follow the documentation at each source code repository to install 

For best results, install the LibraryofVA/plugin-Scripto-2.0 and create a collection before installing the LibraryofVA/Scribe-2.0 theme.
