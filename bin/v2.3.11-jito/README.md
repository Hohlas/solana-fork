# Solana Binaries for version v2.3.11-jito 

## System Information
- **Ubuntu Version**: Ubuntu 22.04.5 LTS
- **Kernel Version**: 5.15.0-142-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
db3a99c6fde5b61f9f93241995d8805074989c28351268b114f856cb70253980  solana
5e6b3ec8d1a96a695ff80c2c820a3d6844cfa24e4ad4f6f5fc63a66d3fba86d2  agave-validator
082388880e08e3f7aa8ffd01e817aab75e652a84103e7a058f7281aba46d7773  solana-keygen
```

### Verification Steps

1. **Download the binaries and checksum file**:
   - Binaries: [solana.zip](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.3.11-jito/solana.zip)
   - Checksum: [checksum.txt](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.3.11-jito/checksum.txt)

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

