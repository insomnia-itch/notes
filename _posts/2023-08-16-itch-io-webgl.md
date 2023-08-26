---
layout: post
title:  "Publish WebGL Unity game to itch.io"
categories: unity itch.io
author: Jelani
---

In your Unity project, open `File`, then click on `Build Settings`. Once that is open under "Platform", select `WebGL`, then click on `Switch Platform`.

![](/assets/unity-build-settings-switch-platform.png)


### Build Settings

Open `Player Settings`, then `Publishing Settings`, and under `Compression Format` select `Disabled`


![Unity WebGL Settings for itchi.io](/assets/unity-webgl-settings-for-itch-io.png)

### Build the Game

Back in `Build Settings`, click on `Build`, which should create a folder with your game in it.

Once it's finished, compress the folder as ZIP.

### Uploading to itch.io

![](/assets/itch-io-game-type.png)
