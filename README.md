# android-code-injection-test
How to start:
1. Download Android SDK to use `adb` tools.
2. Download and install GenyMotion Android Emulator (rooted)
3. Download `frida-server` image for Android from https://github.com/frida/frida/releases   
4. Copy `frida-server` image file to `/data/local/tmp/` path of emulator device. (you can use `adb push` command or just drag & drop the file)    
5. Use `adb shell "chmod 755 /data/local/tmp/{frida server file name}"` to set proper permissions for `frida-server` file.
6. Run `frida-server` using `adb shell "/data/local/tmp/{firda server file name} &"` command.    
7. Download and install `python 3.7`.
8. Create a python environment and name it what you want, then activate it.
9. In your env, use `pip install frida-tools` to install frida python package.
10. To see if everything works fine, in command line use `frida-ps -U`. this command will show a list of emulator device processes.
11. Download and install `rps.apk` from https://github.com/ctfs/write-ups-2015/blob/master/seccon-quals-ctf-2015/binary/reverse-engineering-android-apk-1/rps.apk  
12. Run `rsp` app on emulator and then run `python ctf.py`. you will see the injected code works. 

References:    
https://frida.re/docs/android/    
https://github.com/frida/frida/releases   
https://github.com/ctfs/write-ups-2015/blob/master/seccon-quals-ctf-2015/binary/reverse-engineering-android-apk-1/rps.apk    
https://book.hacktricks.xyz/mobile-apps-pentesting/android-app-pentesting/frida-tutorial    
https://forum.xda-developers.com/t/official-xposed-for-lollipop-marshmallow-nougat-oreo-v90-beta3-2018-01-29.3034811/    
https://labs.f-secure.com/tools/drozer/    
https://github.com/m9rco/Genymotion_ARM_Translation/blob/master/package/Genymotion-ARM-Translation_for_8.0.zip    
