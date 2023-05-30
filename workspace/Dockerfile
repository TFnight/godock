# 建立 base image
ARG GODOCK_GO_VERSION
FROM golang:${GODOCK_GO_VERSION}

# 設置工作目錄
WORKDIR /var/go

# 設置環境變數
ARG GODOCK_APP_PATH_HOST
ARG GODOCK_EXTENSION_SODIUM
ARG GODOCK_EXTRA_HTOP

# 安裝 libsodium，若 EXTENSION_SODIUM 為 false 則不安裝
RUN if [ ${GODOCK_EXTENSION_SODIUM} = true ]; then \
      apt-get update && apt-get install -y libsodium-dev; \
    fi

# 安裝 htop，若 EXTRA_HTOP 為 false 則不安裝
RUN if [ ${GODOCK_EXTRA_HTOP} = true ]; then \
      apt-get update && apt-get install -y htop; \
    fi

RUN go env -w GO111MODULE=on