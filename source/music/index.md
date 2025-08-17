---
title: music
date: 2025-08-17 09:59:46
aplayer: false
---

<!-- 引入APlayer资源 -->
<link rel="stylesheet" href="https://unpkg.com/aplayer@1.10.1/dist/APlayer.min.css">
<script src="https://unpkg.com/aplayer@1.10.1/dist/APlayer.min.js"></script>
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
        lrc: '/music/LoveStory/lovestory.lrc',
        theme: '#ebd0c2'
      },
      {
        name: '童话镇',
        artist: '陈一发儿',
        url: '/music/童话镇/童话镇.mp3',  // 确保文件在source/music目录下
        cover: 'https://i.kfs.io/album/global/84935848,3v2/fit/500x500.jpg',
        lrc: '/music/童话镇/童话镇.lrc',
        theme: '#252E47'
      },
      {
        name: '好想爱这个世界啊',
        artist: '华晨宇',
        url: '/music/好想爱这个世界啊/好想爱这个世界啊.mp3',  // 确保文件在source/music目录下
        cover: 'https://upload.wikimedia.org/wikipedia/zh-yue/d/d2/%E5%A5%BD%E6%83%B3%E6%84%9B%E9%80%99%E5%80%8B%E4%B8%96%E7%95%8C%E5%95%8A.jpg',
        lrc: '/music/好想爱这个世界啊/好想爱这个世界啊.lrc',
        theme: '#343030'
      }
    ]
  });
};
</script>