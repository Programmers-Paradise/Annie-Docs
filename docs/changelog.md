# Changelog

All notable changes to the Annie documentation website will be documented in this file.

## [Unreleased]

### Changed

- Updated urllib3 from 2.5.0 to 2.6.0 to address security vulnerabilities (CVE-2025-66471, CVE-2025-66418)
- Added brotli>=1.2.0 dependency for enhanced security in HTTP content decompression
- Ensures compatibility with urllib3 2.6.0's improved handling of decompression bombs and chained encodings
- Dropped Python 3.9 support from CI testing (Python 3.9 reaches end of life in October 2025, and newer dependencies require Python 3.10+)

### Security

- Fixed potential decompression bomb vulnerabilities through urllib3 2.6.0 update
- Fixed potential DoS attack via unlimited chained encodings through urllib3 2.6.0 update
- Added brotli 1.2.0+ for security fixes in brotli decompression

### Notes

- No code changes were required as the codebase does not use the deprecated urllib3 APIs (HTTPResponse.getheaders(), HTTPResponse.getheader())
- The repository only uses urllib3 indirectly through the requests library
