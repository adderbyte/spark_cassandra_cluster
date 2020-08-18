FROM nvcr.io/nvidia/pytorch:20.03-py3

COPY requirements.txt /tmp/
RUN pip install -r /tmp/requirements.txt

ENV PYTHONPATH="/workspace"
WORKDIR /workspace

## bash file build-ffmpeg.sh added
ADD build-ffmpeg.sh build-ffmpeg.sh

## set bash file to privilege mode
RUN chmod +x build-ffmpeg.sh

## Build essential files 




RUN apt-get update && apt-get install -y git build-essential yasm cmake libtool libc6 libc6-dev unzip wget libnuma1 libnuma-dev frei0r-plugins-dev libgnutls28-dev libass-dev libmp3lame-dev libopencore-amrnb-dev libopencore-amrwb-dev libopenjp2-7-dev libopus-dev librtmp-dev libsoxr-dev libspeex-dev libtheora-dev libvo-amrwbenc-dev libvorbis-dev libvpx-dev libwebp-dev libx264-dev libx265-dev libxvidcore-dev


# build the bash file 

RUN ./build-ffmpeg.sh