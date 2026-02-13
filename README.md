# GrenLogger iOS SDK

Lightweight, secure logging SDK for Apple platforms.

## Requirements

| Platform | Minimum Version |
|----------|----------------|
| iOS      | 15.0           |
| macOS    | 12.0           |
| tvOS     | 15.0           |
| watchOS  | 8.0            |

- Swift 5.9+
- Xcode 15+

## Installation

### Swift Package Manager

Add GrenLogger to your project using Xcode:

1. **File** > **Add Package Dependencies...**
2. Enter the repository URL:
   ```
   https://github.com/grendowdev/grenlogger-ios
   ```
3. Select version **1.0.4** (or "Up to Next Major Version")
4. Add **GrenLogger** to your target

Or add it to your `Package.swift`:

```swift
dependencies: [
    .package(url: "https://github.com/grendowdev/grenlogger-ios", from: "1.0.4")
]
```

## Quick Start

```swift
import GrenLogger

// Initialize with your API key
GrenLogger.initialize(apiKey: "your-api-key")

// Log messages at different levels
GrenLogger.debug("Debug info", metadata: ["key": "value"])
GrenLogger.info("User signed in")
GrenLogger.warning("Disk space low")
GrenLogger.error("Request failed", metadata: ["code": 500])
GrenLogger.fatal("Unrecoverable error")

// Flush pending logs
GrenLogger.flush()

// Shutdown when done
GrenLogger.shutdown()
```

## Features

- **Zero configuration** — just an API key
- **SSL certificate pinning** — always enabled, cannot be disabled
- **Offline buffering** — logs are queued and sent when connectivity is restored
- **Automatic batching** — efficient network usage
- **All Apple platforms** — iOS, macOS, tvOS, watchOS

## Documentation

Full documentation available at [docs.grenlogger.app](https://docs.grenlogger.app)

## License

MIT License. See [LICENSE](LICENSE) for details.

