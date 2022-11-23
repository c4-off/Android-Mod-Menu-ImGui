 # ImGui Mod Menu for Android
 > 24.11.2022: Read Recomendations.


 This is a mod menu with ImGui for Android Unity Games
 Preview (built in Standoff 2):
 [<img src="image/menu.png" alt="menu"/>](image/menu.png)
 # Why i'm copypasta this project?
 the open code of this menu was initially merged, I fixed it and made it under Android Studio
 The original open source source belongs to [OzMod](https://github.com/ozmod)
 # How it works?
   By hooking eglSwapBuffers and Register Natives and then nativeInjectEvent. Yes, i know that it's very old way. 
   I know there is a much better way to hook these 2 functions, (but it not recomended yet).
   It easily crashing. Because this is old project, i decided to open to public it now.
   Just know, The shit-code you see is not my level in 2022. Many things changed from first creation time.
   
   I even realized that CMake is not good for building at all,
   but i won't update all of these things on GitHub.
   So it's FULLY your risks, and wishes of the library. 
  # How to inject / implement
  1. Copy your builded lib to lib/armeabi-v7a
  2. Load the library on Activity Start.
     
   The main activity of Unity is: ```com/unity/player/UnityPlayerActivity```
   
   
   ```Kotlin
   const-string v0, "_ozMod" # Library name

   invoke-static {v0}, Ljava/lang/System;->loadLibrary(Ljava/lang/String;)V
   ```
   Not sure? It need to be like
    [<img src="image/inj.png" alt="menu"/>](image/inj.png)

# Why menu crashed on start game?
This is due to ESP. Because initially ESP was made for the game [BPM](https://www.google.com/search?q=blockpost+mobile)

# Recomendations

1. This is the old project. If you really need to understand and build it, then do it by yourself, this project is no longer maintained.

# Used to create

OpenGL (GLESv2), EGL
