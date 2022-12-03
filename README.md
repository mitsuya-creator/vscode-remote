# VSCODE Remote Development 
This repository created as reminder that i had ever installed and run this extension work
and run perfectly on my mobile device.

## Reference/source guide
[dev.to/josiasaurel](https://dev.to/josiasaurel/how-to-install-vscode-on-android-5f8d)


## How to Install
I will assume you know how to use terminal, in this guide, we will use the most popular
android terminal, yep, that's  called Termux .

1. Install [Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk)
or you will find latest version in their [Github](https://github.com/termux/termux-app#github)
2. Install ubuntu in your andorid device, it's targeted for such systems. Copy paste the following 
command and wait to finish installing 
```
pkg install wget openssl-tool proot -y && hash -r && wget https://raw.githubusercontent.com/EXALAB/AnLinux-Resources/master/Scripts/Installer/Ubuntu/ubuntu.sh && bash ubuntu.sh
```
once done, run this command 
```
./start-ubuntu.sh
```
3. when you are in ubuntu terminal  which is marked by ` root@localhost:~# ` , you can run the 
following command to grab the editor
```
wget https://github.com/cdr/code-server/releases/download/2.1698/code-server2.1698-vsc1.41.1-linux-arm64.tar.gz
```
4. Extract that file use this command
```
tar -xvf code-server2.1698-vsc1.41.1-linux-arm64.tar.gz
```
congrats, you have extracted that file. Now you can remove the archive optionally to free up some 
space else you're going to use later. 
` The files are no more in an executable format, they need to be placed in a /bin folder`

5. copy file that you have extracted to `/bin` folder . use this command
```
cp code-server2.1698-vsc1.41.1-linux-arm64/code-server /bin
```

## Final
You can call editor by running command `code-server` anywhere in your terminal
```
root@localhost:~# code-server
```
FINAL NOTE : Each time you launch it, you'll see a new password and it can be annoying.
so let set a password in our environment variabel, use this command
```
export PASSWORD="<your password>"
```
remove the `<>` mark, example
```
export PASSWORD="12345678"
```

# Preview
Run command `code-server` 
```
root@localhost:~# code-server
```
then open your browser, in addressBox type `http://localhost:8080` then Enter
And Login Using password you have made.
