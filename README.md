# DisHost Documentation

Welcome to the official documentation for DisHost, a file hosting tool that allows you to host files up to 75GB for free for life. This page will guide you through using DisHost and provide code examples to help you get started.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
  - [Uploading Files](#uploading-files)
  - [Downloading Files](#downloading-files)
- [SDK Integration](#sdk-integration)
- [FAQ](#faq)

## Introduction

DisHost is a user-friendly file hosting service that offers generous storage for your files. It's easy to use, and you can start hosting your files quickly and efficiently.

## Installation

You can use DisHost via our SDK, which simplifies the process of uploading and downloading files. To integrate DisHost into your project, follow these steps:

1. Download the DisHost SDK.
(private alpha SDK cannot be downloaded!)
2. Include the SDK in your project.


# Example for including the DisHost SDK in your project 
drag the Sdk in and import it


## Usage

### Uploading Files

To upload a file using DisHost, use the following code:
```csharp
using DisHost;

// Specify the file path you want to upload
string filePath = "path/to/your/file.ext";
//private key for later delete if wish
int PrivateKey = 100;
// Upload the file
DisHost.Upload(filePath, PrivateKey);
```

### Downloading Files

To download a file using DisHost, use the following code:

```csharp
using DisHost;

// Specify the file ID and the desired file name
string fileId = "your-file-id";
string saveName = "downloaded-file.ext";

// Download the file
DisHost.DownloadFile.Download(fileId, saveName);
```

## SDK Integration

The DisHost SDK makes it easy to integrate DisHost into your project. It provides functions for uploading and downloading files, as demonstrated above.

### Uploading Files

The `DisHost.Upload(string filePath)` method allows you to upload files to DisHost. Simply provide the path to the file you want to upload, and the SDK takes care of the rest.

### Downloading Files

The `DisHost.DownloadFile.Download(string fileId, string saveName)` method allows you to download files from DisHost. Specify the file ID and the desired file name for the downloaded file.

## FAQ

**Q: Is DisHost really free for life?**
A: Yes, DisHost offers free hosting for files up to 75GB with no time limits.

**Q: How can I manage my hosted files?**
A: You can manage your hosted files through the DisHost SDK while uploading you give it a private key to request a delete do as the following.
```csharp
using DisHost;

// Specify the Reason to delete the file
string Reason = "I no longer wish to have my files here.";
//private key provided on deletion
int PrivateKey = 100;
// Remove file from server
DisHost.Remove(Reason, PrivateKey);
```

**Q: Can I use DisHost for commercial purposes?**
A: Yes, you can use DisHost for both personal and commercial purposes.

For more information and updates, please visit our [GitHub repository](https://github.com/Troyydev/DisHost).

If you have any questions or need further assistance, feel free to [contact our support team](mailto:support@troyyhelps.co.uk).

Happy hosting with DisHost!
