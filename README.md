FFMPEG 
=====================
Use FFMPEG from PHP

> **IMPORTANT!**

> This class DON'T depend/need of `ffmpeg-php` php extension.

## Requirements

* FFmpeg binary <https://ffmpeg.org/download.html>
* PHP 5
    * PCRE (Perl-Compatible)
    * Program execution Functions <http://php.net/manual/en/ref.exec.php>

Examples
---------------------

**Verify if this is a valid file**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4');

> if(!$ffmpeg){ print 'Fail FFMPEG'; }

> print $ffmpeg->isValid(); //true; 

> print $ffmpeg->isVideo(); //true; 

> print $ffmpeg->isAudio(); //false; 


**Get metadata**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4');

> if(!$ffmpeg){ print 'Fail FFMPEG'; }

> $metadata = $ffmpeg->getMetadata();

> print $metadata['duration']; // 30 seconds

> print $metadata['width']; // 1920

> print $metadata['height']; // 1080


**Debug metadata**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4');

> if(!$ffmpeg){ print 'Fail FFMPEG'; }

> print_r($ffmpeg->getMetadata());


**Convert video to flv**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4');

> if(!$ffmpeg){ print 'Fail FFMPEG'; }

> $ffmpeg->convert('/path/for/the/new/flv/video.flv');
