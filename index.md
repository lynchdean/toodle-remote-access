# OS configuration:

## PuTTY (For Windows):
*  Download [PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html)
*  Run putty.exe
* Select the 'Connection>SSH>Tunnels' category.
* 
   1. Type "8080" in the source port.
   2. Underneath, select 'Dynamic' and 'Auto'.
   3. Click 'Add'.
* Select the 'Connection>SSH' category.
* Tick the 'Don't start a shell or command at all' box.
* Select the 'Session' category at the top.
* Enter the host name (\<username\>@student.computing.dcu.ie) and port (22).
* Select SSH as the connection type underneath.
* Save the configuration under any name you like.

## Linux/Mac
Use this command:
> ssh -D 127.0.0.1:8080 -f -C -q -N \<username\>@student.computing.dcu.ie

# Browser configuration:

## Firefox:
* Settings > Preferences > Advanced > Network > Settings...
* Select "Manual proxy configuration:"
* In the 'SOCKS Host' field type "127.0.0.1" and in the adjacent 'Port' field type "8080".
* Ensure SOCKS v5 is selected.
* Click OK.

To launch:
* In PuTTY (Or through the terminal on Linux/Mac), load your configuration and enter your password in the shell.
* To test if it worked successfully, just check your IP address through the browser. It should be 136.206.x.

## Chrome:
* Create a copy of your Google Chrome shortcut. (eg. Desktop Shortcut)
* Right click it and select properties.
* In the 'Target' field, add the text below on to the end after the file path to chrome.exe, making sure there's a space in between.

> --proxy-server="socks5://127.0.0.1:8080"

* It should look something like this:

> "C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --proxy-server="socks5://127.0.0.1:8080"

* Rename the shortcut to anything you like and place it anywhere.

To launch:
* Close any Chrome windows you have open.
* Ensure no Chrome processes are running before launching or else it may not work. Do this by ending each Google Chrome task in Task Manager or by un-ticking the 'Continue running background apps when Chrome is closed' box in the Chrome advanced settings near the bottom.
* In PuTTY (Or through the terminal on Linux/Mac), load your configuration and enter your password in the shell.
* Launch Chrome using the new shortcut.
* To test if it worked successfully, just check your IP address through the browser. It should be 136.206.x.

