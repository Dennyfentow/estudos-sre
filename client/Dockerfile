FROM debian@sha256:859ea45db307402ee024b153c7a63ad4888eb4751921abbef68679fc73c4c739

USER root

COPY ./client.sh /scripts/client.sh

RUN apt update && \
        apt install curl -y && \
        chmod +x /scripts/client.sh

ENTRYPOINT ["/scripts/client.sh"]
