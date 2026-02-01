# Enhanced LRC Lyrics Corrector

This is a small web-based tool that post-processes Enhanced LRC files so they display correctly in [Booming Music](https://github.com/mardous/BoomingMusic).

## Note: This is AI-generated code
This tool was created entirely with the help of AI assistants, specifically Claude and Perplexity, based on my prompts and requirements.
I reviewed and tested the generated code before publishing it.

## Usage
The tool is specifically intended for Enhanced LRC files created with the **Enhanced LRC Maker**:  
https://schindlershadow.com/tools/LRCmaker/

It rewrites each line so that:
- the main line timestamp at the beginning (`[mm:ss.xxx]`) is preserved,
- a matching inline timestamp (`<mm:ss.xxx>`) is added for the first word,
- extra spaces after `>` are removed so inline timestamps sit directly in front of each word.

Example:

```text
Input:
[00:01.000] Hello <00:01.300> world <00:02.600>
[00:10.500] This <00:10.900> is <00:11.200> good <00:12.200>

Output:
[00:01.000]<00:01.000>Hello <00:01.300>world <00:02.600>
[00:10.500]<00:10.500>This <00:10.900>is <00:11.200>good <00:12.200>
