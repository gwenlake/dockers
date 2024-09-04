FROM nvidia/cuda:12.6.0-cudnn-runtime-ubuntu24.04
RUN apt-get update -y && apt-get install -y --no-install-recommends \
    python3 python3-pip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*