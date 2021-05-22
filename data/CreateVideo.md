`ffmpeg -r 30 -start_number 60 -i ../../cam_front_center/20180810150607_camera_frontcenter_000000%03d.png -frames:v 900 -vcodec libx264 -pix_fmt yuv420p -x264-params crf=28:keyint=30:bframes=0 -tune fastdecode front_center.mkv`

`ffmpeg -r 30 -start_number 60 -i ../../cam_rear_center/20180810150607_camera_rearcenter_000000%03d.png -frames:v 900 -vcodec libx264 -pix_fmt yuv420p -x264-params crf=28:keyint=30:bframes=0 -tune fastdecode rear_center.mkv`

`ffmpeg -r 30 -start_number 60 -i ../../cam_side_left/20180810150607_camera_sideleft_000000%03d.png -frames:v 900 -vcodec libx264 -pix_fmt yuv420p -x264-params crf=28:keyint=30:bframes=0 -tune fastdecode side_left.mkv`

`ffmpeg -r 30 -start_number 60 -i ../../cam_side_right/20180810150607_camera_sideright_000000%03d.png -frames:v 900 -vcodec libx264 -pix_fmt yuv420p -x264-params crf=28:keyint=30:bframes=0 -tune fastdecode side_right.mkv`

`mkvmerge.exe -o Gaimersheim.mkv front_center.mkv side_left.mkv side_right.mkv rear_center.mkv`
