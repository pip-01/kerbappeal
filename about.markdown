---
layout: page
title: About
permalink: 
---

<html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <title></title>
        <script type="text/javascript">
            var picPaths = ['../img sm/0-1-edited.jpg','../img sm/0-5.jpg','../img sm/0-10.jpg','../img sm/unnamed-3.jpg','../img sm/0-12-edited.jpg'];
            var curPic = -1;
            //preload the images for smooth animation
            var imgO = new Array();
            for(i=0; i < picPaths.length; i++) {
                imgO[i] = new Image();
                imgO[i].src = picPaths[i];
            }

            function swapImage() {
                curPic = (++curPic > picPaths.length-1)? 0 : curPic;
                imgCont.src = imgO[curPic].src;
                setTimeout(swapImage,4000);
            }

            window.onload=function() {
                imgCont = document.getElementById('imgBanner');
                swapImage();
            }
        </script>

    </head>
    <body>

        <div>
            <img id="imgBanner" src="" alt="" />
        </div>

    </body>

</html>
