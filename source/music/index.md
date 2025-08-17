---
title: music
date: 2025-08-17 09:59:46
aplayer: true
---
测试文本

{% aplayer "Love Story" "Taylor Swift" "./LoveStory/lovestory.mp3" "https://upload.wikimedia.org/wikipedia/zh/6/60/Fearless_album.jpg" "lrc:./LoveStory/lovestory.txt" %}

{% aplayerlist %}
{
    "narrow": false,                          // （可选）播放器袖珍风格
    "autoplay": true,                         // （可选) 自动播放，移动端浏览器暂时不支持此功能
    "mode": "random",                         // （可选）曲目循环类型，有 'random'（随机播放）, 'single' (单曲播放), 'circulation' (循环播放), 'order' (列表播放)， 默认：'circulation' 
    "showlrc": 3,                             // （可选）歌词显示配置项，可选项有：1,2,3
    "mutex": true,                            // （可选）该选项开启时，如果同页面有其他 aplayer 播放，该播放器会暂停
    "theme": "#e6d0b2",	                      // （可选）播放器风格色彩设置，默认：#b7daff
    "preload": "auto",                    // （可选）音乐文件预载入模式，可选项： 'none' 'metadata' 'auto', 默认: 'auto'
    "listmaxheight": "513px",                 // (可选) 该播放列表的最大长度
    "music": [
        {
            "title": "Love Story",
            "author": "Taylor Swift",
            "url": "./LoveStory/lovestory.mp3",
            "pic": "https://upload.wikimedia.org/wikipedia/zh/6/60/Fearless_album.jpg",
            "lrc": "./LoveStory/lovestory.txt"
        }

    ]
}
{% endaplayerlist %}


<link rel="stylesheet" href="APlayer.min.css">
<div id="aplayer"></div>
<script src="APlayer.min.js"></script>

<script>
const ap = new APlayer({
    container: document.getElementById('player'),
    mini: false,
    autoplay: false,
    theme: '#FADFA3',
    loop: 'all',
    order: 'random',
    preload: 'auto',
    volume: 0.7,
    mutex: true,
    listFolded: false,
    listMaxHeight: 90,
    lrcType: 3,
    audio: [
        {
            name: 'Love Story',
            artist: 'Taylor Swift',
            url: './LoveStory/lovestory.mp3',
            cover: 'https://upload.wikimedia.org/wikipedia/zh/6/60/Fearless_album.jpg',
            lrc: './LoveStory/lovestory.txt',
            theme: '#ebd0c2'
        }
    ]
});
</script>