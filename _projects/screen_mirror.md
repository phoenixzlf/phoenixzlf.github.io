---
layout: page
title: 'Screen Mirror'
description: This is a small Android tool that splits your phone screen and mirrors the content. 
img: assets/img/screen_mirror.png
importance: 0
category: fun
---

This is a small Android tool that I created for fun. It splits your phone screen and mirrors the content, so you and your partner sitting on the other side of the table can view the same content on your phone at the same time. 

It does something like this. 

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/screen_mirror_demo/screener_1.png" title="Screenshot 1" class="img-fluid rounded z-depth-1" %}
        {% include figure.html path="assets/img/screen_mirror_demo/screener_2.png" title="Screenshot 2" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/screen_mirror_demo/screener_3.png" title="Screenshot 3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

This application was originally developed for Android 7 devices, and I have no intention to update it further. Recently (12/24/2022) I tested it on my Android 10 device, and it still worked. Depending on the device and the version of Android, one issue that might be observed is that the mirrored screen is not perfectly positioned at where it should be, thus possibly causing extra margins and some part of the mirrored screen to be cut off. The positioning is off by just a bit, so this issue does not hurt the functionality much, but you are more than welcome to fix it. 

Here is the source code of this project: <a href="https://github.com/phoenixzlf/screen_mirror.git">Open GitHub Link</a>; and here is an article that discusses some technical details of this project: <a href="/blog/2017/android-screen-capture/">Open Blog Article</a>.


