# Just a duplicate of https://github.com/containers/bootc/blob/main/docs/install.md#injecting-ssh-keys-in-a-container-image except with *my* SSH key
FROM ghcr.io/cgwalters/c9s-oscore
RUN mkdir -p /usr/etc-system/ && \
    echo 'AuthorizedKeysFile /usr/etc-system/%u.keys' >> /etc/ssh/sshd_config.d/30-auth-system.conf && \
    echo 'ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIOQkQHeKan3X+g1jILw4a3KtcfEIED0kByKGWookU7ev walters@verbum.org' > /usr/etc-system/root.keys && chmod 0600 /usr/etc-system/*.keys && \
    ostree container commit
