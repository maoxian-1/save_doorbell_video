FROM python:3.9
LABEL org.opencontainers.image.source="https://github.com/maoxian-1/save_doorbell_video"
LABEL maintainer="v1st233@gmail.com"

WORKDIR /app

COPY requirements.txt ./
COPY app.py ./
# COPY sources.list /etc/apt/sources.list
RUN apt-get update && \
    apt-get install -y \
    ffmpeg \
    libva-drm2 \
    libva2 \
    vainfo \
    i965-va-driver \
    && apt-get clean
RUN pip install -r requirements.txt

CMD ["python3","app.py"]
