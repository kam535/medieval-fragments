---
layout: exhibit
title: 'Sample Exhibit Shell'
author: Cornell RMC
publish_date: 2024-11-15
permalink: /exhibits/c/
---
<html>
  <head>
    <meta charset="UTF-8" />
    <script src="https://gustavgenberg.github.io/handy-front-end/SoundPlayer.js"></script>
  </head>
  <body>

  This is a sample sentence that illutsrates the capacity for hypertext. Click on the highlighted text, like this <a href="#" data-audio-src="https://download.quranicaudio.com/quran/abdullaah_3awwaad_al-juhaynee/001.mp3">recitation of Surah al Faithah</a> to hear the audio.
  Click on the highlighted/bolded text to hear a <a href="#" data-audio-src="https://download.quranicaudio.com/quran/abdullaah_3awwaad_al-juhaynee/002.mp3">recitation of Surah al Bakarah</a>.

  <script>
    const player = new SoundPlayer();
    const elements = document.querySelectorAll('[data-audio-src]');
    for(let element of elements) {
      const audioSrc = element.getAttribute('data-audio-src');
      player.load(audioSrc);
      element.onclick = function () {
        var audio_clip = get(audioSrc)
          if(audio_clip.paused);
          {
            audio_clip.play();
          }
          else
          {
            audio_clip.pause();
          }
      }
  </script>
  
  </body>
</html>
