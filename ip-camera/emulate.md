Pull rtsp server if not found:
sudo docker pull aler9/rtsp-simple-server
Run rtsp server:
sudo docker run --rm -it --network=host aler9/rtsp-simple-server
Run ffmpeg, change ‘192.168.1.177’ to your IP address: 
ffmpeg -stream_loop -1 -re -i case1.mp4 -c copy -f rtsp rtsp://192.168.1.177:8554/mystream
Run/Restart our docker compose:
sudo docker-compose up
