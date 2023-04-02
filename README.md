# yt-uploader

Script that uploads a video to youtube. This can come in handy when doing youtube automatization. 
The script is written based on the documentation provided in https://developers.google.com/youtube/v3/guides/uploading_a_video with a little changes to
fit my needs.

## Prerequisities
Installed dependencies:
- pip3 install httplib2
- pip3 install google-api-python-client
- pip3 install oauth2client

## Example Usage
```bash
python3 yt-uploader.py --path=<path_to_video_dir> \
             --title="My new video of foo bar" \
             --description="$vid_desc" \
             --keywords="foo,bar" \
             --category="17" \
             --privacyStatus="public"
```

Arguments:
- `path_to_video_dir` should be a directory that contains:
   1. the video named as `compiled.mp4` in subdirectory `videos` -  `path_to_video_dir/videos/compiled.mp4`
   2. `client_secrets.json` file that contains the OAuth credentials that will be used for video upload. These credentials can be generated in your
   Google Cloud project that will be uses to uplad the video. This project has to complete the
   [Youtube service audit|https://support.google.com/youtube/contact/yt_api_form?hl=en] if you want the uploaded videos to be publicly visible.
