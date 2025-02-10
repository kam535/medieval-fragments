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
    <style>

.popup {
  position: relative;
  display: inline-block;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.popup .popuptext {
  visibility: hidden;
  width: 160px;
  background-color: #555;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 8px 0;
  position: absolute;
  z-index: 1;
  bottom: 125%;
  left: 50%;
  margin-left: -80px;
}

.popup .popuptext::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: #555 transparent transparent transparent;
}

.popup .show {
  visibility: visible;
  -webkit-animation: fadeIn 1s;
  animation: fadeIn 1s;
}

@-webkit-keyframes fadeIn {
  from {opacity: 0;} 
  to {opacity: 1;}
}

@keyframes fadeIn {
  from {opacity: 0;}
  to {opacity:1 ;}
}
</style>
  </head>
<body>
  
<div>
This is a sample sentence that illustrates the capacity for hypertext. Click on the highlighted text, like this <a href="#" data-audio-src="https://download.quranicaudio.com/quran/abdullaah_3awwaad_al-juhaynee/001.mp3">recitation of Surah al Faithah</a> to hear the audio. Click on the highlighted/bolded text to hear a <a href="#" data-audio-src="https://download.quranicaudio.com/quran/abdullaah_3awwaad_al-juhaynee/002.mp3">recitation of Surah al Bakarah</a>.
 <script>
    const player = new SoundPlayer();
    const elements = document.querySelectorAll('[data-audio-src]');
    for(let element of elements) {
      const audioSrc = element.getAttribute('data-audio-src');
      player.load(audioSrc);
      element.onclick = function () {
          player.get(audioSrc).play();
      }
    }
  </script>
</div>

<br>

<div>
<script>
function playSound(sound) {
  var song = document.querySelectorAll('[goog-data-audio-src]');
  song.volume = .25; // setting the volume to 25% because the sound is loud
  if (song.paused) {  // if song1 is paused
    song.play();
  } else {
    song.pause();
  }
}
</script>
This is a sample sentence that illustrates the capacity for hypertext. Click on the highlighted text, like this
<audio id="sound">
  <source src="https://download.quranicaudio.com/quran/abdullaah_3awwaad_al-juhaynee/001.mp3" type="audio/mp3">
</audio>
<text onclick="playSound('sound')">**recitation of Surah al Faithah**</text>
to hear the audio. Click on the highlighted/bolded text to hear a
<audio id="sound2">
  <source src="https://download.quranicaudio.com/quran/abdullaah_3awwaad_al-juhaynee/002.mp3" type="audio/mp3">
</audio>
<text onclick="playSound('sound2')">**recitation of Surah al Bakarah**</text>
</div>

<div style="text-align:center">
<h2>Popup</h2>
<div class="popup" onclick="myFunction()">Click me to toggle the popup!
  <span class="popuptext" id="myPopup">
  A Simple Popup!
  <img src="https://www.gravatar.com/avatar/995b3dfe123b57347bd3d6e29b986dea?s=64&d=identicon&r=PG&f=y&so-version=2">
  </span>
</div>
<script>
function myFunction() {
  var popup = document.getElementById("myPopup");
  popup.classList.toggle("show");
  }
</script>
</div>

</body>
</html>
