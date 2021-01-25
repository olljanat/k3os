ARG REPO
ARG TAG
FROM ${REPO}/k3os-base:${TAG}

ARG ARCH
ENV ARCH ${ARCH}
ENV VERSION 127b96e897abd3633724274b4be51165ebcd42d8
ADD https://raw.githubusercontent.com/olljanat/k3s/install/allow-specify-user/install.sh /output/install.sh
ENV INSTALL_K3S_COMMIT=${VERSION} \
    INSTALL_K3S_SKIP_START=true \
    INSTALL_K3S_BIN_DIR=/output
RUN chmod +x /output/install.sh
RUN /output/install.sh
RUN echo "${VERSION}" > /output/version
