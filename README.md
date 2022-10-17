# Gstreamer_RTSP

```bash
gst-launch-1.0 v4l2src device=/dev/video0 ! video/x-raw, framerate=30/1, width=640, height=480 \
! videobox border-alpha=1 top=-2 bottom=-2 left=-2 right=-2 ! videomixer name=mix \
! autovideosink sync=0 \
v4l2src device=/dev/video2 ! video/x-raw, framerate=30/1, width=320, height=240 \
! videoconvert ! mix.
```
