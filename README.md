FFMPEG 
=====================
Use FFMPEG from PHP

Example:

Verify if this is a valid video file 

$ffmpeg = new FFMPEG('/path/to/your/video.mp4'); 
echo $ffmpeg->isValid(); //true; 