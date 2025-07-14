# Solana Binaries for version v2.2.19-jito 

## System Information
- **Ubuntu Version**: Ubuntu 24.04 LTS
- **Kernel Version**: 6.8.0-31-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
46fbd4ea4a1956bf99665e9bd1f3cd47a680aa9c61c2722188785108cd25cfb7  solana
cabc66dfcd52152a6d500c5917e3f5a02f0f4fc67b69ae1fd25973bb7bcad471  agave-validator
2bbc1f558c6ee713584a430bf7bb3ec336b3ed902e1c7a83bb0cc7844770597a  solana-keygen
```

### Verification Steps

1. **Download the binaries and checksum file**:
   - Binaries: [solana.zip](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.2.19-jito/solana.zip)
   - Checksum: [checksum.txt](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.2.19-jito/checksum.txt)

2. **Extract the zip archive**:
   ```bash
   unzip solana.zip
   ```

3. **Verify the checksums**:
   On Linux/macOS:
   ```bash
   sha256sum -c checksum.txt
   ```
   Expected output:
   ```
   solana: OK
   solana-validator: OK
   solana-keygen: OK
   ```

   On Windows (PowerShell):
   ```powershell
   Get-FileHash -Path .\solana -Algorithm SHA256 | Format-List
   Get-FileHash -Path .\agave-validator -Algorithm SHA256 | Format-List
   Get-FileHash -Path .\solana-keygen -Algorithm SHA256 | Format-List
   ```
   Compare the output with the values in `checksum.txt`.

