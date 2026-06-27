## How-to

### Сreate a catalog

```bash
mkdir -p /etc/xbps.d
```

### add hampa repository-x86_64-glibc

```bash
cat <<'EOF' > /etc/xbps.d/99-repository-hampa.conf
repository=https://github.com/ngoding-id/hampa/releases/latest/download/
EOF
```

### Add a public key to sign the repository

```bash
sudo wget -O /var/db/xbps/keys/f5:a9:de:96:d4:f0:69:14:9d:01:76:5e:44:20:95:35.plist https://github.com/ngoding-id/hampa/raw/refs/heads/main/repo-keys/x86_64/f5:a9:de:96:d4:f0:69:14:9d:01:76:5e:44:20:95:35.plist
```

### Update the repository

```bash
sudo xbps-install -Su
```
