Purpose
=====
LAMCompression is a category on NSData that provides data compression and decompression functionality by wrapping CompressionLib, a new library available on OS 10.11 and iOS 9.0

LAMCompression is written in Objective-C. For the Swift version see [Compression](https://github.com/leemorgan/NSData-Compression).

Installation
=====
To use the LAMCompression category in an app, just include the `NSData+LAMCompression.h` and `.m` files in your project. You will also need to include the `libcompression` library.

NSData Extensions
=====

    - (NSData *)lam_compressedDataUsingCompression:(LAMCompression)compression;
Returns a NSData object created by compressing the receiver using the given compression algorithm

<br>

    - (NSData *)lam_uncompressedDataUsingCompression:(LAMCompression)compression;
Returns a NSData object by uncompressing the receiver using the given compression algorithm

<br>

    + (NSData *)lam_dataWithContentsOfArchive:(NSString *)path;
Creates and returns a NSData object by decompressing the data from the file specified by path. Attempts to determine the appropriate decompression algorithm using the path's extension.

<br>

    + (NSData *)lam_dataWithContentsOfArchive:(NSString *)path usedCompression:(LAMCompression)compression;
Creates and returns a NSData object by decompressing the data from the file specified by path using the given compression algorithm.

<br>

    - (NSData *)lam_initWithContentsOfArchive:(NSString *)path;
Returns a NSData object initialized by decompressing the data from the file specified by path. Attempts to determine the appropriate decompression algorithm using the path's extension.

<br>

    - (NSData *)lam_initWithContentsOfArchive:(NSString *)path compression:(LAMCompression)compression;
Returns a NSData object initialized by decompressing the data from the file specified by path using the given compression algorithm.


Documentation
=====
The `NSData+LAMCompression` category is documented using standard Xcode doc comments.

In keeping with good Cocoa practices `NSData+LAMCompression` uses a `lam_` prefix for category methods.

The project has a dummy (skeleton) app which is included to support Unit Testing with Xcode. The app itself doesn't do anything interesting at all.


Supported OS & SDK Versions
=====
LAMCompression relies on CompressionLib which is only available in OS 10.11 and iOS 9.0 and later.


Background Information
=====

[Tinkering with CompressionLib](http://blog.shiftybit.net/tinkering-with-compressionlib/)

[Tinkering with CompressionLib (Part 2)](http://blog.shiftybit.net/tinkering-with-compressionlib-part-2)

[Tinkering with CompressionLib (Part 3)](http://blog.shiftybit.net/tinkering-with-compressionlib-part-3)

By [Lee Morgan](http://shiftybit.net). If you find this useful please let me know. I'm [@leemorgan](https://twitter.com/leemorgan) on twitter.


License
=====
The license is contained in the "License.txt" file.

