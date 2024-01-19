# DisHost Documentation

Welcome to the official documentation for DisHost, your trusted file hosting solution that allows you to store files of up to 75GB for free, for life. This comprehensive guide will walk you through using DisHost and provide you with code examples to help you get started.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
  - [Uploading Files](#uploading-files)
  - [Downloading Files](#downloading-files)
- [SDK Integration](#sdk-integration)
- [FAQ](#faq)

## Introduction

DisHost is a user-friendly file hosting service that offers generous storage for your valuable files. It is designed for ease of use, allowing you to get started quickly and efficiently.

## Installation

You can seamlessly integrate DisHost into your projects by using our SDK, which simplifies the process of uploading and downloading files. To integrate DisHost into your project, follow these simple steps:

1. Download the DisHost SDK.
   (Please note that the private alpha SDK is not available for download at this time.)

2. Include the SDK in your project.

```csharp
// Example for including the DisHost SDK in your project
// Simply drag and drop the SDK into your project directory and import it.
```

## Usage

### Uploading Files

To upload a file using DisHost, utilize the following code snippet:

```csharp
using DisHost;

// Specify the file path you want to upload
string filePath = "path/to/your/file.ext";

// Upload the file with an optional private key for later deletion
int privateKey = 100;
DisHost.Upload(filePath, privateKey);
```

This code will also log your unique ID for the uploaded file in the debug logs.

### Downloading Files

To download a file from DisHost, employ the following code:

```csharp
using DisHost;

// Specify the file ID and the desired file name for saving
string fileId = "your-file-id";
string saveName = "downloaded-file.ext";

// Download the file
DisHost.DownloadFile.Download(fileId, saveName);
```

You can retrieve the file ID either from the upload process or from Discord using the bot.

## SDK Integration

The DisHost SDK streamlines the integration of DisHost into your projects by providing easy-to-use functions for both uploading and downloading files, as illustrated above.

### Uploading Files

The `DisHost.Upload(string filePath, int privateKey)` method facilitates file uploads to DisHost. Simply specify the file's path, and the SDK will handle the rest. Optionally, you can provide a private key for later file deletion.

### Downloading Files

The `DisHost.DownloadFile.Download(string fileId, string saveName)` method enables you to download files from DisHost. Specify the file ID and the desired name for saving the downloaded file.

## FAQ

**Q: Is DisHost genuinely free for life?**
A: Absolutely. DisHost provides free file hosting for up to 75GB, with your storage limit increasing over time as you continue to use our services.

**Q: Are my files hosted indefinitely?**
A: Not exactly. To maintain your files, you must renew them by accessing our Discord channel and using the /renew command followed by the file ID and private key. This renewal is required every 14 days; otherwise, your files will be permanently deleted.

**Q: Are there any drawbacks to using DisHost?**
A: Yes, there is a 1-minute cooldown period for each removal request.

**Q: How can I manage my hosted files?**
A: Managing your hosted files is simple with the DisHost SDK. During the upload process, you provide a private key for later deletion. To remove a file, use the following code:

```csharp
using DisHost;

// Specify the reason for deleting the file
string reason = "I no longer wish to host my files here.";

// Provide the private key used during upload
int privateKey = 100;

// Remove the file from the server
DisHost.Remove(reason, privateKey);
```

**Q: Can I use DisHost for commercial purposes?**
A: Absolutely, DisHost can be used for both personal and commercial purposes.

For additional information and updates, please visit our [GitHub repository](https://github.com/Troyydev/DisHost).

If you have any questions or require further assistance, do not hesitate to [contact our dedicated support team](mailto:support@troyyhelps.co.uk).

Thank you for choosing DisHost for your hosting needs! Happy hosting!
