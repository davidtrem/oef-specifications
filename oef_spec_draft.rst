OEF file format specifications
==============================

Preambule
---------

- All computer strings (i.g. "text") specified in this document are case sensitive (i.e.
if string is lower case, an upper case version is not valid)

Definition
----------
An OEF file is designed to be an ESD data exchange format.
Practically it is an hdf5 file which follow conventions:

Specifications
--------------
- The file extension is "oef" (*.oef).

- Oef leaves :
  An oef leave is any hdf5 folder containing ESD data that must have
  - an attribute named "oef_data_type" which has is one the string in
    ("tlp", "hbm", "mm") list.
  -  an attribute named "oef_version" which
     is a string following standard strict python conventions for version numbering
   "A version number consists of two or three
    dot-separated numeric components, with an optional "pre-release" tag
    on the end.  The pre-release tag consists of the letter 'a' or 'b'
    followed by a number.  If the numeric components of two version
    numbers are equal, then one with a pre-release tag will always
    be deemed earlier (lesser) than one without."

- The root folder cannot be an oef leave

-...