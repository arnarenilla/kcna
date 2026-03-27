FROM almalinux:8

LABEL maintainer="Sander <mail@sandervanvugt.nl>"

COPY sander.repo /etc/yum.repos.d/

RUN dnf -y update && \
    dnf -y install bash nmap iproute && \
    dnf clean all

ENTRYPOINT ["/usr/bin/nmap"]
CMD ["-sn", "172.17.0.0/24"]
