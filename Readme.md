# JNBT: The Java NBT Library

## NBT

NBT, or Named Binary Tag, is a file format created by Markus Persson for use with Minecraft levels. Although originally designed for Minecraft levels, it is appropriate for many use cases.

## JNBT

JNBT is a Java library to read and write NBT files, written by Graham Edgecombe and available open-source under the BSD license.

This fork of JNBT has added support for Tag_Int_Array, and added classes that allow reading without loading an entire NBT structure to memory.

Thanks to:
Ancient (a.k.a. grahamedgecombe) - JNBT 1.0 and 1.1
osici - for the TAG_Lists bug
Jocopa3 - Initial Int-Array support
Morlok8k - Maintaining the project
MarkJeronimus - Maintaining the project

## Building

This version uses Maven. To build JAR and Javadocs, type
> mvn clean install site

For more information about the license, see LICENSE.TXT.

For more information about the project, see http://jnbt.sf.net/.

## Version History

JNBT 1.8 (Dan Greening)
- Build apidocs with Maven

1.7 (Marius Lindvall)
 ** WORK IN PROGRESS **
 - NBT reader and writer classes which do not require loading the entire NBT structure to memory
    > Similar interface to GSON
    > Especially useful for huge NBT files

1.6 (Mark Jeronimus)
 - Getters/setters for List and Array type tags (access like a data structure)
    > CompoundTag.getTag(String) is especially useful
 - Constructors for List and Array type tags (without value parameter)
 - Constructors for primitive type tags with int parameter

1.5 (Mark Jeronimus)
 - Constructors for streams with manual compression type (using Enum)
 - Getters for primitive type tags with primitive return value
 Under te hood:
 - Refactored multiple scattered utility functions into a single enum NBTTagType

1.4
- (pruby) InputStream gzip/not-gziped support
- (ensirius) Raw DataInputStream support

1.3 (Morlok8k)
- Changed encoding of .java files to UTF-8
- added "[JNBT]" to error output
- added .equals and .hashcode to tags
- cleaned source and formatting, etc...

1.2 (Morlok8k)
- Tag_Int_Array Support

1.1 (grahamedgecombe)
- fix for writing TAG_Lists
- toString() methods on each tag type

1.0 (grahamedgecombe)
- Initial Release



