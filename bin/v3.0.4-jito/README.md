# Solana Binaries for version v3.0.4-jito 

## System Information
- **Ubuntu Version**: Ubuntu 22.04.5 LTS
- **Kernel Version**: 5.15.0-142-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
fc0e2d0d1c773091f8d0bd754116652a2ccef684915710d6e3d4f1d92ff65af3  solana
cb95d31e38e26264b9a616f78e56f642539e9fa4db6fea200ada7eceed46af67  agave-validator
749ad7a2a28aced4771679a1d88cec14f1b641a4a4b8e0bc3927fabedbed1ba0  solana-keygen
```

### Verification Steps

1. **Download the binaries and checksum file**:
   - Binaries: [solana.zip](https://github.com/Hohlas/solana-fork/blob/main/bin/v3.0.4-jito/solana.zip)
   - Checksum: [checksum.txt](https://github.com/Hohlas/solana-fork/blob/main/bin/v3.0.4-jito/checksum.txt)

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

