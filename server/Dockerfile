FROM buildpack-deps:stretch

ARG JRE_TAG=181

COPY server-jre-8u${JRE_TAG}-linux-x64.tar.gz /

RUN set -x \
 && mkdir -p /opt \
 && cd /opt       \
 && tar -xzf /server-jre-8u${JRE_TAG}-linux-x64.tar.gz \
 && mv jdk1.8.0_${JRE_TAG} jdk-1.8 \
 && chown -R root:root jdk-1.8     \
 && cd /                       \
 && tar -cJf rootfs.tar.xz opt \
 && rm -rf /opt

