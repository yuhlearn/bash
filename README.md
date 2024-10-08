# bash
A collection of Bash scripts.

## extract

Unpacks password protected (and not prassword protected) archives in parallel by going through a text file with a line separated list of passwords and trying each one in turn. It automatically checks the current path for archives and tries to unpack all of them. Works seamlessly with archives split into multiple parts. Handles 7z, rar, and zip files. 

**Requirements:** 
7z, unrar

## videnh

Use AI to enhance videos. Enhances the quality of the video with Real-ESRGAN, doubles the frame rate with RIFE interpolation and allows for custom output frame size, among other things. It uses ncnn Vulcan implementations of Real-ESRGAN and RIFE to be more platform independent. 

**Requirements:**
[Real-ESRGAN ncnn Vulkan](https://github.com/xinntao/Real-ESRGAN/) (executable as `realesrgan`),
[RIFE ncnn Vulkan](https://github.com/nihui/rife-ncnn-vulkan) (executable as `rife`),
ImageMagick,
ffmpeg

## framerestore

Replaces duplicate frames in videos with RIFE interpolated frames. Goes through the video frame by frame and checks if the next frame was the same as the previous. Then replaces the duplicates with interpolated frames, generated from the first duplicate and the next non-duplicate frame.

**Requirements:**
[RIFE ncnn Vulkan](https://github.com/nihui/rife-ncnn-vulkan) (executable as `rife`),
ffmpeg,
idiff (part of `openimageio-tools` package on Debian)
