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


<!-- 引入APlayer资源 -->
<link rel="stylesheet" href="https://unpkg.com/aplayer@1.10.1/dist/APlayer.min.css">
<script src="https://unpkg.com/aplayer@1.10.1/dist/APlayer.min.js"></script>

<!-- 播放器容器 -->
<div id="aplayer" style="width: 100%; max-width: 800px; margin: 2rem auto;"></div>

<!-- 初始化脚本 -->
<script>
// 确保页面完全加载后再执行
window.onload = function() {
  // 检查APlayer是否加载成功
  if (typeof APlayer === 'undefined') {
    console.error('APlayer未加载成功，请检查CDN链接');
    return;
  }
  
  // 检查容器是否存在
  const container = document.getElementById('aplayer');
  if (!container) {
    console.error('未找到播放器容器');
    return;
  }
  
  // 初始化播放器
  const ap = new APlayer({
    container: container,
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
        url: '/music/LoveStory/lovestory.mp3',  // 确保文件在source/music目录下
        cover: 'https://upload.wikimedia.org/wikipedia/zh/6/60/Fearless_album.jpg',
        lrc: '/music/LoveStory/lovestory.txt',
        theme: '#ebd0c2'
      }
    ]
  });
};
</script>