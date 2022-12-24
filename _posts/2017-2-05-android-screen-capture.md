---
layout: post
title:  Screen Capture and Output with Transformations
date:   2017-02-05 16:40:16
description: If you ever need to capture the content on your Android device and output it with some transformations... 
tags: 'Android_development'
categories: development_notes
---


<p><a href="https://www.linfengzhang.com">Linfeng Zhang</a></p>
<p>In a recent Android project I am working on, I try to implement a method that captures the content on screen and project it onto a medium with certain transformations.</p>
<p>There have been a lot of tutorials on the screen capturing part out there. The typical way is using <code>MediaProjectionManager</code> to create a screen capture intent, and then projecting the content onto a surface upon user’s approval using the <code>createVirtualDisplay</code> method. Google provides a nice demo about the usage of media projection, which can be found <a href="https://android.googlesource.com/platform/development/+/master/samples/ApiDemos/src/com/example/android/apis/media/projection/MediaProjectionDemo.java">here</a>. In this example, the surface for projection is created through a <code>SurfaceView</code>, but it can also be created from other instances like a <code>MediaRecorder</code> or a <code>ImageReader</code>, which can be used for video recording or taking screenshots.</p>
<p>In order to achieve the goal of live output with transformations, <code>TextureView</code> seems to be the best choice here, as it renders contents with <code>SurfaceTexture</code>, which can be used to construct a surface object, and unlike the <code>SurfaceView</code>, <code>TextureView</code> can be easily scaled and transformed using the <code>setTransform</code> method. This approach does the trick when you need to display only a part of the screen in a sized window. There might be other better ways to do it since <code>TextureView</code> is quite memory consuming and getting the proper transformation matrix can be tricky in some occasions.</p>