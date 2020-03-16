# Mach3ToolFile
Mach3 tools file format class for python

## Mach3 tools file format
From:
https://www.cnczone.com/forums/mach-software-artsoft-software-/142166-mach3-tools3-dat-tool-table-binary-file.html

The file starts with 255 tool records (#0-254).
Each record is variable length. 
The end of the file is padded with 255 bytes of 0x01

Tool record file format:
- first byte is length of name (N)
- next N bytes is name
- 8 bytes ignored
- 8 bytes diameter double
- 26 bytes ignored
- 8 bytes diameter wear double
- 8 bytes height double
- 8 bytes height wear double

## Improvements
Read the fill as one bytearray, close the fill and process, same for write.

