# Kuzu iOS Integration

This repository contains the necessary components and instructions for integrating [Kuzu](https://kuzudb.com/) - a high-performance graph database - into iOS applications.

## Contents

- Header files for integrating with Kuzu's C API
- Integration guide with detailed installation instructions
- Example Swift code for using Kuzu in an iOS application

## Example Usage

For a working example of this integration, see the demo repository:
[https://github.com/johnbenac/kuzo-ios-test](https://github.com/johnbenac/kuzo-ios-test)

## Integration Overview

To integrate Kuzu into your iOS application:

1. Add the `Kuzu.xcframework` to your Xcode project
2. Add the required `-lc++` linker flag
3. Create an Objective-C Bridging Header to import the Kuzu C API
4. Initialize the database with iOS-appropriate memory settings
5. Use the C API to execute Cypher queries

For detailed integration instructions, see [KUZU_IOS_INTEGRATION.md](KUZU_IOS_INTEGRATION.md) in this repository.

## iOS-Specific Considerations

When using Kuzu on iOS, you must configure it with appropriate resource constraints:

- Buffer pool size: 16MB (not default/0)
- Max threads: 1 (not default/0)
- Max DB size: 64MB (not 2GB)
- Checkpoint threshold: 1MB (not 5MB)

These settings are critical for reliable operation on iOS devices.

## License

This integration follows the same licensing as the Kuzu database project.

## Contributing

Contributions to improve the iOS integration are welcome. Please submit issues or pull requests to help enhance this project.
