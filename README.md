# StreamMediaMemand
一个基于live555系统做了增强，在些基础上加入了更多的视频格式
#关于live555 http://www.live555.com/

#下面是更新日志

#2014/10/31
	1.对live555的开源项目进行vs2010的移植
#2014/11/03
	1.加入的去mp4文件的支持
		原理：mediaServer只支持".m4e"格式的Elementary Stream fie，但并不支持串流mp4封装格式的文件，要串流mp4格式的文件一般都是结合FFmpeg进行，但是代码量稍大，这里使用一种较为简单的方法实现对mp4封装格式文件的串流。即我们预先对mp4文件进行处理，解析出各个流，并单独存储它们（解析工具用'mp4creator -extract='），然后将解析出来的H.264文件再进行串流处理（最新版的live555支持H.264的串流），客户端可用VLC或者FFmpeg的ffplay进行串流播放
