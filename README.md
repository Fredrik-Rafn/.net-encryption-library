# Encryption Library for .NET

## Introduction

A simple and secure encryption algorithm.

It encrypts and decrypts Byte[] instead of 32bit integer array, and the key is also the Byte[].

In addition to providing the API of Byte[] encryption and decryption, it also provides some methods to handle String and Base64 encode.

## Installation

```sh
git clone https://github.com/selfmade1337/.net-encryption-library.git
```

## Usage

```csharp
using System;
using System.Diagnostics;
using encryptor;

namespace Example {
    class MainClass {
        public static void Main (string[] args) {
            String str = "Hello World！";
            String key = "1234567890";
            Byte[] encrypt_data = ENCRYPTOR.Encrypt(str, key);
            String decrypt_data = ENCRYPTOR.DecryptToString(encrypt_data, key);
            Debug.Assert(str == decrypt_data);
        }
    }
}


```
