# FheTranspilerCpp

**Note:** The next-generation FHE compiler framework, **[HEIR](https://github.com/google/heir)**, has succeeded this repository. We strongly recommend visiting the [HEIR GitHub repo](https://github.com/google/heir) and its official website [https://heir.dev](https://heir.dev) for the latest advancements.

## Overview

**FheTranspilerCpp** (formerly "fully-homomorphic-encryption") is an open-source library and toolchain designed to bridge the gap between standard C++ development and Fully Homomorphic Encryption (FHE). It functions as a compiler that converts standard C++ logic into FHE-compatible C++ code capable of operating on encrypted datasets.

### What is Fully Homomorphic Encryption (FHE)?

Fully Homomorphic Encryption is a cutting-edge cryptographic technique that allows mathematical operations to be performed on encrypted data without ever needing to decrypt it first. This creates a paradigm shift where data privacy and data processing can coexist seamlessly.

**The Problem:** Traditionally, if an app needed to process encrypted data, it had to:
1. Decrypt the data.
2. Perform the calculation.
3. Re-encrypt the results.
This exposes sensitive data to the application layer.

**The Solution:** FHE introduces a transformed computation `F'` that can be applied directly to the encrypted data. The result is an encryption of the desired output: `F(unencrypted_data) = Decrypt(F'(encrypted_data))`.

### The FHE C++ Transpiler

This project provides a general-purpose transpiler with a modular architecture. It allows researchers and developers to:

*   **Swap FHE Libraries:** Choose the underlying cryptographic backend.
*   **Define High-Level Logic:** Describe programs in standard C++.
*   **Target Specific Outputs:** Generate optimized FHE-C++ code.

By automating the translation of logic to FHE-compatible circuits, this tool minimizes the performance overhead typically associated with manual FHE implementation, aiming to make privacy-preserving computation viable for real-world applications.

## Architecture & Usage

For detailed implementation guides, examples, and the source code structure, please refer to the [`transpiler`](./transpiler/) subdirectory.

## Support & Legacy

While this repository will continue to receive critical updates, active development and major feature improvements are focused on the **HEIR** project. We are not accepting external contributions to this specific legacy repository at this time.