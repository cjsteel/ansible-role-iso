# ansible-role-iso.md

An ansible role that ensures we have a checksummed local copy of an iso file.

## clone role

    git clone https://github.com/cjsteel/ansible-role-iso.git iso

## dest
 	
* dest is an absolute path of where to download the file to.
* if dest is a directory, either the server provided filename or, if none provided, the base name of the URL on the remote server will be used.
* If a directory, force has no effect.
* !!! If dest is a directory, the file will always be downloaded (regardless of the force option), but replaced only if the contents changed.

- name: ensure we have ubuntu-12.04.5-desktop-amd64.iso locally.
  get_url:
    url=http://releases.ubuntu.com/12.04/ubuntu-12.04.5-desktop-amd64.iso
    dest=files/ubuntu-12.04.5-desktop-amd64.iso
    sha256sum=d1f10ea7ca59266567fa8d2522ad800e1aa063f139630f925d2484d8e169b4c2

- name: ensure we have ubuntu-12.04.5-desktop-amd64.iso locally.
  get_url:
    url=http://releases.ubuntu.com/12.04/ubuntu-12.04.5-server-amd64.iso
    dest=files/ubuntu-12.04.5-server-amd64.iso
    sha256sum=af224223de99e2a730b67d7785b657f549be0d63221188e105445f75fb8305c9

http://releases.ubuntu.com/12.04/ubuntu-12.04.5-server-amd64.iso

http://releases.ubuntu.com/12.04/ubuntu-12.04.5-desktop-amd64.iso
http://releases.ubuntu.com/12.04/ubuntu-12.04.5-desktop-amd64.iso.torrent


http://releases.ubuntu.com/12.04/SHA256SUMS

http://releases.ubuntu.com/12.04/SHA256SUMS.gpg

## example

- name: download file with check
  get_url:
    url=http://example.com/path/file.conf
    dest=/etc/foo.conf
    checksum=sha256:b5bb9d8014a0f9b1d61e21e796d78dccdf1352f23cd32812f4850b878ae4944c
  get_url:
    url=http://example.com/path/file.conf
    dest=/etc/foo.conf
    checksum=md5:66dffb5228a211e61d6d7ef4a86f5758

