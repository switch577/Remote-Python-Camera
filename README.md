# Remote-Python-Camera
A bodge to send a video feed over the network

<b>Even though this script has an option for a password, it is not secure. Anyone who can MITM the connection will be able to find the secret and connect to the server</b>

<b>NOTE: this was simply a 1-day bodge I needed to get a remote camera feed. It is buggy and unfinished.<br>In my testing, this does not work with raspberry pi camera modules on aarch64 Raspbian.</b>

Required Packages:<br>
<b>python3-tk on Debian Bookworm</b><br>
tk<br>
opencv-python<br>
pillow<br>

# Arguments:
./main.py  
  -s --server | run as server  
  --passwd    | set a password for the server  

when running as server:
it will automatically open a socket server listening at the specified listen port and listen address (rserver.py, line 10,11)

when running as client:
it will ask for an IP and a port, and if the server is password protected, a password. After inputted, a window will open showing the camera stream.
