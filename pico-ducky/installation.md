
# Installation
- hold the reset button in the pico while connecting it to your system
- stop holding the reset button when it shows up in your file system
- copy the `flash_nuke.uf2` into pico to reset the pico
- The pico will now disconnect and reconnect
- copy the `circuitpython.uf2` into pico to install circuit python in the pico
- replace the lib directory and the code.py file on the pico with the one in the zip file
- create a file `payload.dd` where you will be scripting your own ducky script
- example payload
```dd
DELAY 3000

GUI r
DELAY 500
STRING powershell $obj = New-Object -ComObject WScript.Shell;  1..50 | ForEach-Object {  $obj.SendKeys( [char] 175 )  }; Start-Process 'https://www.youtube.com/watch?v=xvFZjo5PgG0&autoplay=1'
DELAY 250
ENTER
```
## payload reference
https://docs.hak5.org/hak5-usb-rubber-ducky/duckyscript-tm-quick-reference
