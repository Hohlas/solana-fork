# Solana Binaries for version v2.3.2-jito 

## System Information
- **Ubuntu Version**: Ubuntu 22.04 LTS
- **Kernel Version**: 5.15.0-25-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
743684de21f78e5fd41671768de843f635bf90b99ea07dd91cab63ede46a72f8  solana
d43f3d8795f80af6527747077daf70e6817dfe683c9698d281c5639733f552c7  agave-validator
7de9afcddbf2752dc5b5778ba59ccde94c4481ff66f7ca8df7b2647674144e7a  solana-keygen
```

### Verification Steps

1. **Download the binaries and checksum file**:
   - Binaries: [solana.zip](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.3.2-jito/solana.zip)
   - Checksum: [checksum.txt](https://github.com/Hohlas/solana-fork/blob/main/bin/v2.3.2-jito/checksum.txt)

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

