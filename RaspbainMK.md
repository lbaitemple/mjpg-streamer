Install mjpeg-streamer for a new raspbian system.  

```
sudo apt install python-opencv  -y
sudo apt install python-protobuf  -y 
sudo apt-get install libsdl-image1.2-dev -y
sudo apt-get install libsdl-dev -y
sudo  apt-get install libprotobuf-c1 -y 
sudo  apt-get install libprotobuf-c-dev -y
sudo apt install -yqq cmake-curses-gui -y
sudo apt-get install libjpeg8-dev imagemagick libv4l-dev cmake -y
wget https://raw.githubusercontent.com/gonzalo/gphoto2-updater/master/gphoto2-updater.sh && chmod +x gphoto2-updater.sh && sudo ./gphoto2-updater.sh
git clone https://github.com/lbaitemple/mjpg-streamer
cd mjpg-streamer/mjpg-streamer-experimental
make
sudo make install
sudo ./mjpg_streamer -i "./input_uvc.so -f 10 -r 640x320 -n -y" -o "./output_http.so -w ./www -p 8080"
```
