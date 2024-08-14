# Video Compression Script

This bash script compresses video files into MP4 format using FFmpeg. It's designed to create smaller, web-friendly versions of video files while maintaining reasonable quality.

## Features

- Converts input video to MP4 format
- Disables audio stream in the output
- Uses H.264 codec for wide compatibility
- Ensures QuickTime support with yuv420p pixel format
- Creates output in a separate 'out' directory

## Prerequisites

- Bash shell
- FFmpeg installed and accessible in your PATH

## Usage

1. Make the script executable:
   ```
   chmod +x compress-video.sh
   ```

2. Run the script with a video file as an argument:
   ```
   ./compress-video.sh path/to/your/video.mov
   ```

3. The compressed video will be saved in the `out/` directory with the same filename but with a .mp4 extension.

## Notes

- The script currently only outputs MP4 files. WebM conversion is commented out but can be enabled if needed.
- Audio is disabled in the output (-an flag in FFmpeg command). Remove this flag if you want to keep audio.
- The script uses the following FFmpeg settings:
  - libx264 codec
  - yuv420p pixel format
  - Baseline profile (for maximum compatibility)

## Acknowledgments

Inspired by: https://gist.github.com/Vestride/278e13915894821e1d6f
