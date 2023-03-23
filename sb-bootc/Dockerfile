FROM quay.io/fedora/fedora-silverblue:rawhide
ADD copr-bootc.repo /etc/yum.repos.d
RUN rpm-ostree install bootupd bootc && bootupctl backend generate-update-metadata / && ostree container commit
