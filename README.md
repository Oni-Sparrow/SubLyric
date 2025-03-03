This library is used to convert SRT files to LRC files and vice versa.

Installation: 
`pip install sublyric`

How to import:
`from SubLyric import Converter`


Available Functions:

`Converter.srt_to_lrc(srt_file_path, lrc_file_path)`

This function converts srt files to lrc.
input file/path is srt_file. output path/file is lrc_file.
SRT files use 3 digits for milliseconds while LRC files use 2 digits.
Therefore, all the timings will be the off by 0.001 to 0.005 seconds. 
(Normally it'd be 0.001 to 0.009, But there's a rounding function that helped with making it more accurate.)
This timing inaccurance should not be significant nor cause problems in captions/subtitles.

`Converter.lrc_to_srt(lrc_file_path, srt_file_path)`

This function converts lrc files to srt.
input file/path is lrc_file. output path/file is srt_file.
LRC files use 2 digits for milliseconds while SRT files use 3 digits. 
Therefore, all the timings will be the off by 0.001 to 0.009 seconds.
This timing inaccurance should not be significant nor cause problems in captions/subtitles.
Also, LRC files use minutes, seconds, and milliseconds only. Unlike SRT files that use hours, minutes, seconds, and milliseconds.


Note: Both of the functions return True/False.
