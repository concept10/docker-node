# AUTOGENERATED FILE
FROM resin/armv7hf-debian:jessie

ENV NODE_VERSION 5.12.0

RUN apt-get update && apt-get install ca-certificates --no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

RUN buildDeps='curl' \
	&& set -x \
	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends \
	&& rm -rf /var/lib/apt/lists/* \
	&& curl -SLO "http://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-armv7l.tar.gz" \
	&& echo "da51a7025772766453f330b3274a12381995e07d68c99c55357767171af4c538  node-v5.12.0-linux-armv7l.tar.gz" | sha256sum -c - \
	&& tar -xzf "node-v$NODE_VERSION-linux-armv7l.tar.gz" -C /usr/local --strip-components=1 \
	&& rm "node-v$NODE_VERSION-linux-armv7l.tar.gz" \
	&& apt-get purge -y --auto-remove $buildDeps \
	&& npm config set unsafe-perm true -g --unsafe-perm \
	&& rm -rf /tmp/*
