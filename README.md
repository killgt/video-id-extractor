# Video ID Extractor

[![Travis build status](https://travis-ci.org/visionappscz/video-id-extractor.png?branch=master)](https://travis-ci.org/visionappscz/video-id-extractor)
[![PHP 7 ready](http://php7ready.timesplinter.ch/visionappscz/video-id-extractor/badge.svg)](https://travis-ci.org/visionappscz/video-id-extractor)
[![Dependency Status](https://www.versioneye.com/user/projects/5927e25e6725bd00166483bd/badge.svg?style=flat-square)](https://www.versioneye.com/user/projects/5927e25e6725bd00166483bd)

This library extracts video IDs from links to hosted videos.

The supported services are:
* [youtube](https://www.youtube.com) 
* [facebook](https://www.facebook.com)
* [vimeo](https://www.vimeo.com)

## Getting Started

### Installing

Install with composer
```
require visionappscz/video-id-extractor
```

### Usage example
```
use VideoIdExtractor\Extractor\VideoIdExtractException;
use VideoIdExtractor\Extractor\YoutubeVideoIdExtractor;  
  
...
  
$extractor = new YoutubeVideoIdExtractor();
try {
    $videoId = $extractor->extract('http://www.youtube.com/watch?v=uWhV5wSyxTI');
} catch (VideoIdExtractException $e) {
    die('The supplied link is not valid.)
}
```
