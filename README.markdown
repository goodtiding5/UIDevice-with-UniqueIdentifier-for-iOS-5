# Description

Apple stopped supporting a unique identifier for iOS. This source code solves the problem. It generates a unique identifier based on the mac address of the device in combination with the bundle identifier.

What you need to do:

- copy NSString+MD5Addition and UIDevice+IdentifierAddition to your project.

- use [[UIDevice currentDevice] uniqueDeviceIdentifier] to retrieve the unique identifier or

- use [[UIDevice currentDevice] uniqueGlobalDeviceIdentifier] to retrieve a global unique identifier (used for tracking between different apps).

- have fun and follow twitter.com/gekitz ;)

//Thanks to Erica Sadun for her UIDevice+Hardware Addition (used for the mac address retrieval).

# Improvement

- Fix a bug on the MD5 extension to NSString.
  The MD5 hash for an empty string (length = 0) should not be nil. (K Zhao)

# License
see license file.