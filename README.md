# FieldtypeOdfFile
Fieldtype/Inputfield for the ProcessWire CMS allowing editing of ODT (Open Document Text) in the backend

## Description
This Fieldtype/Inputfield/Process module adds a field type for a (single) ODT document as created by OpenOffice/LibreOffice and lets you edit that directly in the ProcessWire backend.

The module uses the free [Wodo Texteditor](https://github.com/kogmbh/Wodo.TextEditor_release) based on [WebODF](http://webodf.org/).

## Status
This is an early alpha release. Use at your own risk.

I'll be happy about all feedback and reported issues though.

## Compatibility
ProcessWire Versions 2.7, 2.8 and 3.0.

## Installation
Download a zip package here through the green button and extract it into your PW installation's site/modules folder. In the backend, click on "Modules" -> "Refresh", then click "Install" for FieldtypeOdfFile. The other two modules (InputfieldOdfFile and ProcessOdfEdit) will be installed alongside.

## Usage

Create a file named e.g. "odffile" and select type "OdfFile". Change any settings you need. Compared to a regular InputfieldFile, maxFiles and extensions are removed (we currently only allow one file of type odt) and a new setting for editor height (in pixels) has been added on the details tab.

Add the field to your template, then edit a page with this template and add an odt file. Save the page, then click on the "Edit this document" link. The editor will open in an overlay.

Save any changes you made with the "save" button (second from left) in the editor toolbar.

## Known issues

- Text flow around images is garbled
- Inserting images works but the can't be resized and make documents huge
- Changes in a document's size aren't reflected in the page editor after closing the overlay
- There's no check for unsaved changes (yet)

## Technical stuff
The module extends InputfieldFile and does some stuff to force configuration values like maxFiles etc.

Somewhere in the future, it's probably going to be able to deal with multiple files as well.

## License
This module is licensed under AGPL v3 or any comparable license as outlined in the LICENSE file. Look there for further details.
