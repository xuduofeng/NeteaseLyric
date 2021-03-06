NeteaseLyric [![star this repo](http://github-svg-buttons.herokuapp.com/star.svg?user=Urinx&repo=NeteaseLyric&style=flat&background=1081C1)](https://github.com/Urinx/NeteaseLyric) [![fork this repo](http://github-svg-buttons.herokuapp.com/fork.svg?user=Urinx&repo=NeteaseLyric&style=flat&background=1081C1)](https://github.com/Urinx/NeteaseLyric/fork) ![python](https://img.shields.io/badge/python-2.7%20&%203.6-ff69b4.svg)
----------------------

网易云音乐歌曲的歌词分享图片生成脚本。

一开始，[@lijiarui](https://github.com/lijiarui) 找了个生成网易云音乐歌词图片的脚本 [songzhi/Lrc2Img](https://github.com/songzhi/Lrc2Img) ，然而生成的歌词图片太丑，所以做了一些修改，加了一些其他的功能，使其贴近原版客户端的歌词分享图片，效果如下：

<div align=center>
<img src="res/lyric_0.png" width="280" height="443"/> <img src="res/lyric_1.png" width="280" height="213"/> <img src="res/lyric_2.png" width="280" height="443"/>
</div>

## 使用说明

请先安装 `PIL` 等第三方包依赖，并提供字体文件放在 `res` 目录下，在代码中修改使用的字体。代码中默认使用的是 `STHeiti Light` 字体。

```
Usage: [--sid <song id> | --pid <playlist id>] -t <pic style> -r <random_line>
	-i <your image> -w <some text> -n <name> -l -p <line_range>

Options:
  -h, --help      show this help message and exit
  --sid=SID       song id
  --pid=PID       playlist id
  -t PIC_STYLE    1: has album image, 2: lyric only, 3: combine 1 & 2
  -r RANDOM_LINE  number of random lyric lines
  -p LINE_RANGE   range of lyric lines
  -i IMG_FILE     your own image
  -w TEXT         some text
  -n NAME         name
  -l              only show the lyrics with line number to stdout
```

例1. 根据歌曲`id`生成该歌的歌词，图片样式为`1`，随机选取`2`行歌词：
```
python netease_lyric.py --sid 35476049 -t 1 -r 2
```

例2. 根据歌单`id`生成歌单下所有歌曲的歌词图片，图片样式为`3`：
```
python netease_lyric.py --gid 138688333 -t 3
```

例3. 根据歌曲`id`生成该歌的歌词，选取`1,3,6-9`行歌词：
```
python netease_lyric.py --sid 28695603 -p 1,3,6-9
```

例4. 选取自己的图片和文字生成分享图片：
```
python netease_lyric.py -i 'path/to/img' -w '一回头 青春都喂了狗' -n 'Urinx'
```
<div align=center>
<img src='res/lyric_4.png' width='320' height='464'>
</div>

## 茫然退立，若有所思

> 自幼身处江城，长年跨江往返两地，奔波汉口武昌。不时于车上驻窗而望，看物是人非，观人群熙攘。常叹人生在世，苦乐自知，时而茫然退立，若有所思。遂以图配字，刻记于此。望君翻阅之后，也能分享故事。

<div align=center>
<img src='res/lyric_8.png' width='320' height='562'>
</div>

> 这首歌在网易云音乐上听了208遍。

<div align=center>
<img src='res/lyric_6.png' width='320' height='562'>
</div>

> 还没有留下回忆，就到了这个年纪。

<div align=center>
<img src='res/lyric_3.png' width='320' height='506'>
</div>

> 是我太傻。—— 2017.5.21

<div align=center>
<img src='res/lyric_7.png' width='320' height='562'>
</div>
