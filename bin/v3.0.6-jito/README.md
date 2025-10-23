# Solana Binaries for version v3.0.6-jito 

## System Information
- **Ubuntu Version**: Ubuntu 22.04.5 LTS
- **Kernel Version**: 5.15.0-142-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
99d632a369766a99132498e4f035d8877b160b1792418c200bfb93c7b6ccc86d  solana
6f6d5f02ed91b5e7aae2d8a0e0e85bd0208fa6f932baea2191bd2ca4e4f459a8  agave-validator
da09bf3b3f4147abe0f3fb5a1b8374c99431b77a59e2f8d66e0427e300911ab6  solana-keygen
```

### Verification Steps

1. **Download the binaries and checksum file**:
   - Binaries: [solana.zip](https://github.com/Hohlas/solana-fork/blob/main/bin/v3.0.6-jito/solana.zip)
   - Checksum: [checksum.txt](https://github.com/Hohlas/solana-fork/blob/main/bin/v3.0.6-jito/checksum.txt)

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

