# Solana Binaries for version v3.0.0 

## System Information
- **Ubuntu Version**: Ubuntu 22.04.5 LTS
- **Kernel Version**: 5.15.0-142-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
5b8ff7915298271235280a26d7ff1c5f3ad285fffc4c5d3c04d01ed50d39c99f  solana
29607ade3f5a68200265839763ccec172b061dd2b351ce087af153bb9ccd396f  agave-validator
24be357ceebb5a664dc917733a932a16e9b36bde079c6106782ff604a611bbfe  solana-keygen
```

### Verification Steps

1. **Download the binaries and checksum file**:
   - Binaries: [solana.zip](https://github.com/Hohlas/solana-fork/blob/main/bin/v3.0.0/solana.zip)
   - Checksum: [checksum.txt](https://github.com/Hohlas/solana-fork/blob/main/bin/v3.0.0/checksum.txt)

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

