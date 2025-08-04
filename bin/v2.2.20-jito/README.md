# Solana Binaries for version v2.2.20-jito 

## System Information
- **Ubuntu Version**: Ubuntu 22.04 LTS
- **Kernel Version**: 5.15.0-25-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
8686a8acc11df2fd6b53458290a9eee42ab0c42250b939a850762c6d2b42b0dd  solana
ba147320bf3f8d8f4f18bc581af59618f1827481c0056ecd48f553b9d5f342dd  agave-validator
ce4cbab703ca320982e82b6b25cca9837c87061f794accf7f6456f7e091794ff  solana-keygen
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

