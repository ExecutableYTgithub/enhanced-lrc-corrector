# Enhanced LRC Lyrics Corrector

This is a small web-based tool that post-processes Enhanced LRC files so they display correctly in [Booming Music](https://github.com/mardous/BoomingMusic).

The tool is specifically intended for Enhanced LRC files created with the **Enhanced LRC Maker**:  
https://schindlershadow.com/tools/LRCmaker/

It rewrites each line so that:
- the main line timestamp at the beginning (`[mm:ss.xxx]`) is preserved,
- a matching inline timestamp (`<mm:ss.xxx>`) is added for the first word,
- extra spaces after `>` are removed so inline timestamps sit directly in front of each word.

Example:

```text
Input:
[00:01.000] Hallo <00:01.300> Welt
[00:10.500] Das <00:10.900> ist <00:11.200> gut

Output:
[00:01.000]<00:01.000>Hallo <00:01.300>Welt
[00:10.500]<00:10.500>Das <00:10.900>ist <00:11.200>gut
