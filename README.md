# amele-builds

**MCP-capable [amele](https://github.com/lasthumanintheloop/amele) binaries for every platform** — published by Loxigo Software.

Built from `lasthumanintheloop/amele` at commit `415f781` (MCP support: `amele mcp login|status|logout`). All binaries include the embedded MCP runtime — there is no MCP-less build here, by rule.

## Assets (v0.1.1-mcp)

| File | Platform |
|---|---|
| `amele-linux-amd64` | Linux x86-64 |
| `amele-linux-arm64` | Linux ARM64 (64-bit Pi / ARM server) |
| `amele-linux-arm` | Linux ARMv7 (32-bit Raspberry Pi OS) |
| `amele-darwin-amd64` | macOS Intel |
| `amele-darwin-arm64` | macOS Apple Silicon |
| `amele-windows-amd64.exe` | Windows x86-64 |
| `amele-windows-arm64.exe` | Windows ARM64 |
| `SHA256SUMS` | checksums for every asset above |

## Verify

```bash
sha256sum -c SHA256SUMS
```

## Signing status

- **Windows:** to be signed with the GlobalSign EV certificate (update planned).
- **macOS:** unsigned for now (Developer ID + notarization planned).

## Usage

[kahya](https://github.com/loxigosoftware/kahya)'s `install.py` fetches the
matching asset from this release automatically (SHA256-verified). Direct
download works too — the binaries are plain static executables:

```bash
curl -L -o amele https://github.com/loxigosoftware/amele-builds/releases/download/v0.1.1-mcp/amele-linux-amd64
chmod +x amele
./amele mcp status
```
