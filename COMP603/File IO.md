`I\/O = Input/Output
- Input
	 Keyboards
	 Files
	 
- Output
	 Screen
	 Files

Advantages of file I/O
- Permanent copy
- Output from one program can be input to another
- Input can be automated

**Binary Files**
- The bits represent other types of encoded information, such as executable instruction of numeric data
**Text Files**
- The bits represent printable characters
	  Examples are Java Source Code and any file created with a "text editor"

**Buffering**
Not buffered
- Each byte is read/written from/to disk as soon as possible
- Small delay for each byte
- A disk operation per byte

Buffered
- Reading/writing in "chunks"
- Reading : access the first 4 bytes, need to wait for all 16 bytes before proceeding
- Writing : save the first 4 bytes, need to wait for all 16 bytes before proceeding