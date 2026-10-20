# checksum (HTML)

A single-file, offline tool to hash files in your browser and check them against a digest someone gave you. Nothing is uploaded.

- **One file**: `checksum.html`. Open it in a browser. No install, no server.
- **Offline by design**: a Content-Security-Policy (`connect-src 'none'`) blocks all network connections from the page.
- **Algorithms**: SHA-256 (recommended), BLAKE2b-512 (same as `b2sum`), BLAKE3 (same as `b3sum`), SHA-512 and MD5 (only for older checksum files).
- **Verify**: paste a hash, or a whole `.sha256` / checksum file, and the page tells you which algorithm matches.
- **Many files at once**: choose, drop or paste files; copy a report or download `checksums.txt`.
- **Large files**: files are read as a stream, in pure JavaScript with no dependencies.
- **Self-test**: the page checks its own hash code against known vectors on load.

## Use

1. Open `checksum.html` in a browser (ideally while offline).
2. Choose or drop one or more files.
3. Optionally paste the expected hash to check it.

MD5 does not prove a file was not swapped; use SHA-256 or BLAKE2b for that.

## Verify the download

```
sha256sum -c SHA256SUMS
```

## Value-4-Value

This tool is free to use, no ads, no tracking. It runs on the Value-4-Value model: if it saved you time, give back what it was worth to you at https://allesvoorbitcoin.be/donate

## License

MIT, see [LICENSE](LICENSE).
