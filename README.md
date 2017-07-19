hlsdl
==============

This program converts .m3u8 playlists to a .ts video. It supports decryption of both AES-128 and SAMPLE-AES encryption.

Requirements
------------

This program requirers FFmpeg installed in order to decrypt SAMPLE-AES content.

Build
-----

Use `make && make install && make clean` to install.

Usage and Options
-------
`./hlsdl url [options]`

---------------------------
```
--best    or -b  ... Automaticly choose the best quality.

--verbose or -v  ... Verbose more information.

--output  or -o  ... Choose name of output file.

--help    or -h  ... Print help.

--force   or -f  ... Force overwriting the output file.

--quiet   or -q  ... Print less to the console.

--dump-dec-cmd   ... Print the Key and IV of each media segment.

--dump-ts-urls   ... Print the links to the .ts files.
```
Todo
----

- Multithreading
- Remuxing to other formats
- Local .m3u8 files

使用需要安装ffmpeg
<pre>
1、brew install ffmpeg
2、git clone https://github.com/selsta/hlsdl
3、make && make install && make clean
4、hlsdl http://xxx.m3u8  -o  mp4file/a.mp4
</pre>

ffmpeg直接转
<pre>
ffmpeg -i https://video2.taptapdada.com/t/20170124/1080p_m3u8/aca2eb3e61fb3148be04207d377a1929.mp4/v.m3u8 -acodec copy -vcodec copy out.mp4
</pre>

