# Solana Binaries for version v2.2.19-jito 

## System Information
- **Ubuntu Version**: Ubuntu 22.04 LTS
- **Kernel Version**: 5.15.0-25-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
4cc0d18a993f2d43429fc56ee78285325faf65fb8d483d92b177de8982b50ce0  solana
f57cf9d63b30ddd56f48c3e27ca52832d8abc221d03ece92b3a0ba27ba1e9ebf  agave-validator
8cb9e1a4ecde439654004628f8d9b99b734d291283992ab296f6e635fd90174a  solana-keygen
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

