# Python VLC 媒体列表–为其设置单个媒体对象

> 原文:[https://www . geesforgeks . org/python-VLC-medialist-setting-single-media-object-to-it/](https://www.geeksforgeeks.org/python-vlc-medialist-setting-single-media-object-to-it/)

在本文中，我们将看到如何在 python vlc 模块中将单个媒体对象设置为 MediaList 对象。VLC 媒体播放器是 VideoLAN 项目开发的一款免费开源的便携式跨平台媒体播放器软件和流媒体服务器。MediaList 对象包含多个媒体，换句话说，它有一个媒体列表，可以与 MediaListPlayer 对象一起使用来播放这些多个媒体对象。我们可以借助`add_media`方法将多个视频添加到媒体列表中。

> 为此，我们将对 MediaList 对象使用`set_media`方法
> 
> **语法:** media_list.set_media(媒体)
> 
> **自变量:**以 Media 对象为自变量
> 
> **返回:**返回无

下面是实现

```
# importing vlc module
import vlc

# importing time module
import time

# creating a media player object
media_player = vlc.MediaListPlayer()

# creating Instance class object
player = vlc.Instance()

# creating a media list object
media_list = vlc.MediaList()

# creating a new media
media = player.media_new("death_note.mkv")

# setting media object to the media list
media_list.set_media(media)

# setting media list to the media player
media_player.set_media_list(media_list)

# start playing video
media_player.play()

# wait so the video can be played for 5 seconds
# irrespective for length of video
time.sleep(5)
```

**输出:**
![](img/57ccffa8c486070958f67ed1dd7ef62e.png)

另一个例子

```
# importing vlc module
import vlc

# importing time module
import time

# creating a media player object
media_player = vlc.MediaListPlayer()

# creating Instance class object
player = vlc.Instance()

# creating a media list object
media_list = vlc.MediaList()

# creating a new media
media = player.media_new("1.mp4")

# setting media object to the media list
media_list.set_media(media)

# setting media list to the media player
media_player.set_media_list(media_list)

# start playing video
media_player.play()

# wait so the video can be played for 5 seconds
# irrespective for length of video
time.sleep(5)
```

**输出:**
![](img/1182bf29ec1fe0d0a2c3ce2234f329d4.png)