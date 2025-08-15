# Solana Binaries for version v2.3.6-jito 

## System Information
- **Ubuntu Version**: Ubuntu 24.04.2 LTS
- **Kernel Version**: 6.8.0-60-generic

## Binary Checksums
To verify the integrity of the downloaded binaries, compare their SHA-256 checksums with the values below:

```bash
1972425ff24ddf1d6c2968389f22f0e21113d4e6cd4ce3a3ea44c129a04516cf  solana
eefec961c35ef6778311f1391a38f1244a65bf257d373ee9dc0045337f89427b  agave-validator
d1f453b347309b47da99238d74eae4b6042e30bc43b36131bf870fcf7971039c  solana-keygen
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

