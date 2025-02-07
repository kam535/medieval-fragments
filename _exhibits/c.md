---
layout: exhibit
title: 'Sample Exhibit Shell'
author: Cornell RMC
publish_date: 2024-11-15
permalink: /exhibits/c/
---
<html>
  <head>
    <title>Clover IIIF - Viewer - Web Component</title>
    <meta charset="UTF-8" />
  </head>
  <body>
  <script type="text/javascript">
  $("[data-audio-url]").each(
      function(){
          $(this).on('click', function() {
              var mp3Url = $(this).attr('data-audio-url');
              var a = new Audio(mp3Url);
              a.play();
          });
      }
  );
  
  </script>

  <span data-audio-url="mp3_file_1.mp3">Text1</span>
  <span data-audio-url="mp3_file_2.mp3">Text2</span>
  <span data-audio-url="mp3_file_3.mp3">Text3</span>

  </body>
</html>

An exhibit is just a page written in Markdown (or HTML, or both). You can put whatever you want on here.
