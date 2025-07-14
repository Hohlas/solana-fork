# Solana Binaries for version v2.2.20-jito 

## System Information
- **Ubuntu Version**: Ubuntu 24.04 LTS
- **Kernel Version**: 6.8.0-31-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
cdc2f19ade51749a44183fc5b1caecfac56ec5b970fd5ad730fce9fc5722c063  solana
5579a71d093018a65c2cc5872d899d900f366acee8e2d5cc565b96c5ebd76607  agave-validator
2bbc1f558c6ee713584a430bf7bb3ec336b3ed902e1c7a83bb0cc7844770597a  solana-keygen
```

### Verification Steps

1. **Download the binaries and checksum file**:
   - Binaries: [solana.zip](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.2.20-jito/solana.zip)
   - Checksum: [checksum.txt](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.2.20-jito/checksum.txt)

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

