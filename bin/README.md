## bin install


```bash
TAG=v2.2.12-jito
```

```bash
SOL_BIN="$HOME/.local/share/solana/install/releases/$TAG/solana-release/bin"
API_URL="https://api.github.com/repos/Hohlas/solana-fork/contents/bin/$TAG"
echo "0.45 4 0 24" > ~/solana/mostly_confirmed_threshold
# apt update && apt install p7zip-full -y
```

```bash
mkdir -p "$SOL_BIN"; rm -r $SOL_BIN/*
# Получаем список файлов и скачиваем каждый
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
```

```bash
tail -f ~/solana/solana.log | grep patch
```
validator confirmed
![image](https://github.com/user-attachments/assets/53697a6d-de2a-48fe-aa23-36aded879381) 
validator not in authorized list
![image](https://github.com/user-attachments/assets/122150a6-5617-4b2e-bb3d-77be19a953a2)


