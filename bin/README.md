## bin install


```bash
# TAG=v2.2.19-paladin
TAG=v2.3.2-jito
TAG=v2.2.20-jito
```

```bash
echo "export TAG=$TAG" >> $HOME/.bashrc
SOL_BIN="$HOME/.local/share/solana/install/releases/$TAG/solana-release/bin"
API_URL="https://api.github.com/repos/Hohlas/solana-fork/contents/bin/$TAG"
```

```bash
if ! command -v 7z >/dev/null; then
    echo "install p7zip"
    apt update && apt install p7zip-full -y
fi
cd
if [ -d "$SOL_BIN" ]; then
  rm -rf "$SOL_BIN"/*; echo "remove $SOL_BIN"
else
  mkdir -p $SOL_BIN; echo "make $SOL_BIN"
fi
curl -s "$API_URL" | jq -r '.[] | select(.type=="file") | .download_url' | while read url; do
  echo "Downloading $url"
  curl -L -o "$SOL_BIN/$(basename $url)" "$url"
  if [ $? -ne 0 ]; then
    echo "Failed to download $url"
  fi
done
cd $SOL_BIN
7z x solana.zip
chmod +x ./*
ln -sfn $HOME/.local/share/solana/install/releases/$TAG/solana-release $HOME/.local/share/solana/install/active_release

# add agave->solana links
ln -sfn $SOL_BIN/solana $SOL_BIN/agave
for file in agave-*; do # all files started "agave-"
    if [ -f "$file" ]; then # is exist
        ln -sf "$file" "${file/agave-/solana-}" # create link
        echo "create link for $file"
    fi
done

agave-validator --version
```


### Verify the checksums 
```bash
sha256sum -c checksum.txt
```


### Verify patch working 
```bash
tail -f ~/solana/solana.log | grep patch
```

