ARG CUDA_VERSION="12.6.0"
ARG UBUNTU_VERSION="24.04"

FROM nvidia/cuda:$CUDA_VERSION-cudnn-devel-ubuntu$UBUNTU_VERSION

# Install Python plus openssh, which is our minimum set of required packages.
RUN apt-get update -y && \
    apt-get install -y python3 python3-pip python3-venv && \
    apt-get install -y --no-install-recommends openssh-server openssh-client git git-lfs && \
    python3 -m pip install --upgrade pip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Install pytorch
RUN pip3 install --no-cache-dir -U torch torchvision torchaudio
