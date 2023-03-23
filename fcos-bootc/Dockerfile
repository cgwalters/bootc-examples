FROM quay.io/fedora/fedora-coreos:stable
ADD copr-bootc.repo /etc/yum.repos.d
RUN rpm-ostree install -y bootc && ostree container commit
