- Input/Output (I/O) is the process of trasnfering data either to or from a storage medium.
- C# uses the System.IO namespace
  - has several types to allow reading/writing of files and streams both sync and async
  - also allows compression and decompression
- a *file* is a named collection of bytes with persistant storage
  - uses directory paths, disk storage, and file and directory names 
- A *stream* is a sequence of bytes that can be read or written to a "backing store"
  - a backing store can be several different mediums such as disks or memory
  - there are different kind of streams such as network, memory, and pipe streams.
- Files and directories
  - there are several types in the System.IO namespace to interact with files and directories
  - used to get/set properties, and retrieve collections based on a search query
  - Some Common types 
    *File* - provides static methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.
    *FileInfo* - provides instance methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.
    *Directory* - provides static methods for creating, moving, and enumerating through directories and subdirectories.
    *DirectoryInfo* - provides instance methods for creating, moving, and enumerating through directories and subdirectories.
    *Path* - provides methods and properties for processing directory strings in a cross-platform manner. 
- using System.IO requires the use of 'robust' exception handling.
- Streams
  - Three Fundamental operations
    - Reading - transferring data from a stream into a data structure
    - Writing - transferring data to a stream from a data source
    - Seeking - querying and modifying the current position within a stream
  - Commonly used classes
    - FileStream – for reading and writing to a file.
    - IsolatedStorageFileStream – for reading and writing to a file in isolated storage.
    - MemoryStream – for reading and writing to memory as the backing store.
    - BufferedStream – for improving performance of read and write operations.
    - NetworkStream – for reading and writing over network sockets.
    - PipeStream – for reading and writing over anonymous and named pipes.
    - CryptoStream – for linking data streams to cryptographic transformations.
- Reading and writing to streams is very resource heavy so the process can be done async
- Compression: process of reducing the size of a file for storage
  - Decompression: extracting the information of compressioned file to a usable format
  - Commonly used classes
  - ZipArchive – for creating and retrieving entries in the zip archive.
  - ZipArchiveEntry – for representing a compressed file.
  - ZipFile – for creating, extracting, and opening a compressed package.
  - ZipFileExtensions – for creating and extracting entries in a compressed package.
  - DeflateStream – for compressing and decompressing streams using the Deflate algorithm.
  - GZipStream – for compressing and decompressing streams in gzip data format.
- Isolated storage
  - a way to store data that provides safety and isolation using defined ways to associate the saved date with the code
  - uses viritual file system