# Solana Binaries for version v2.3.6-jito 

## System Information
- **Ubuntu Version**: Ubuntu 22.04 LTS
- **Kernel Version**: 5.15.0-25-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
bea196638883183ccb5ef6af1933e7464ebedc7a618c635f92db620eacb36221  solana
33663483125b9c6495f29a5bcb5d54fa86705e5cab928c707a29975ad68992ff  agave-validator
336205671e3ebf1daa730c5c2ddede4edbd28222db1e0cbf82c308e2e1ae5c33  solana-keygen
```

### Verification Steps

1. **Download the binaries and checksum file**:
   - Binaries: [solana.zip](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.3.6-jito/solana.zip)
   - Checksum: [checksum.txt](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.3.6-jito/checksum.txt)

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

