# Solana Binaries for version v2.3.6-jito 

## System Information
- **Ubuntu Version**: Ubuntu 22.04.5 LTS
- **Kernel Version**: 5.15.0-151-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
6b9fe09958a9c3f0aaa9983548698cf37dd7dce910ffa284594591dc488643a0  solana
26adba7273896fcb2e1086f6309d32d0ba74d64dd5d5b2dbb1640f25db264026  agave-validator
948d41f1d29cdce9252ef2270f944b31ac4f070b4b799fd567b7b291a1bf2878  solana-keygen
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

