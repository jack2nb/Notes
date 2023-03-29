---
date: 2022-10-24
 
title: "html混合makrdown"
authors: ["jack"]
categories:
  - 技术
  - 爱好
tags:
  - 技术
---

<div><img src="/img/tech/sprite.png"  ></div>
  <style>
      .ul li {
          float: left;
          width: 30px;
          height: 30px;
          list-style: none;
          margin: 5px;
          border: 1px solid #CCC;
          border-radius: 6px;
      }
      .ul li:nth-child(1){
          background: url(/img/tech/sprite.png) no-repeat 4px 1px;
      }
      .ul li:nth-child(2){
          background: url(/img/tech/sprite.png) no-repeat -38px 1px;
      }
      .ul li:nth-child(3){
          background: url(/img/tech/sprite.png) no-repeat -81px 3px;
      }
      .ul li:nth-child(4){
          background: url(/img/tech/sprite.png) no-repeat -123px 2px;
      }
      .ul li:nth-child(5){
          background: url(/img/tech/sprite.png) no-repeat -171px 0px;
      }
      .ul li:nth-child(6){
          background: url(/img/tech/sprite.png) no-repeat -214px 2px;
      }
      .ul li:nth-child(7){
          background: url(/img/tech/sprite.png) no-repeat -267px 1px;
      }
      .ul li:nth-child(8){
          background: url(/img/tech/sprite.png) no-repeat 2px -36px;
      }
  </style>

  <ul class="ul">
      <li></li><li></li>
      <li></li><li></li>
      <li></li><li></li>
      <li></li><li></li>
  </ul>

------------

<iframe id="iframe-one" name="iframe-one" src="/img/tech/sprite.png" width="100%" height="100%" scrolling="no" frameborder="0"></iframe>
<button id="goAmpl">全屏显示</button>

<script>
	/**
     * 进入全屏
     * @param element
     */
    function requestFullScreen(element) {
        var requestMethod = element.requestFullScreen || element.webkitRequestFullScreen || element.mozRequestFullScreen || element.msRequestFullScreen;
        if (requestMethod) {
            requestMethod.call(element);
        } else if (typeof window.ActiveXObject !== "undefined") {
            var wscript = new ActiveXObject("WScript.Shell");
            if (wscript !== null) {
                wscript.SendKeys("{F11}");
            }
        }
    }


    /**
     * 退出全屏
     */
    function exitFullscreen() {
        if (document.exitFullscreen) {
            document.exitFullscreen();
        } else if (document.msExitFullscreen) {
            document.msExitFullscreen();
        } else if (document.mozCancelFullScreen) {
            document.mozCancelFullScreen();
        } else if (document.webkitExitFullscreen) {
            document.webkitExitFullscreen();
        }
    }
    
    document.getElementById('goAmpl').onclick = function () {
        let iframe = document.getElementById("iframe-one");
        requestFullScreen(iframe);
    }
    document.getElementById('outAmpl').onclick = function () {
        let iframe = document.getElementById("iframe-one");
        exitFullscreen(iframe);
    }


</script>
-------------
 <iframe
          allow="fullscreen"
          id="iframeId"
          src="/img/tech/sprite.png"
          style="width: 100%; height: 100%"
          scrolling="no" 
          frameborder="0"
></iframe>
     

  

