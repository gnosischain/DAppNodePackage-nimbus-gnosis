ARG UPSTREAM_VERSION

FROM ghcr.io/gnosischain/gnosis-nimbus-eth2:v23.3.2${UPSTREAM_VERSION}

USER root
RUN apt update && apt install curl jq -y

COPY entrypoint.sh /usr/bin/entrypoint.sh
COPY auth-token /home/user/nimbus-eth2/build/data/auth-token
COPY jwtsecret.hex /jwtsecret

ENTRYPOINT [ "entrypoint.sh" ]