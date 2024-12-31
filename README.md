# Inconsistent Barcode Detection in Expo Camera API

This repository demonstrates a bug in Expo's Camera API where the `onBarCodeScanned` function is not consistently called. This leads to unreliable barcode scanning functionality.

## Bug Description

The issue occurs when using a custom `onBarCodeScanned` function with the Expo Camera API.  In some instances, the function is not triggered even when barcodes are clearly visible within the camera's view.  This inconsistency makes the barcode scanning feature unreliable.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the required dependencies.
3. Run `expo start` to start the Expo development server.
4. Observe the inconsistent behavior of the barcode scanning functionality. The `onBarCodeScanned` function may or may not be called when a barcode is detected.

## Solution

The provided solution addresses the inconsistency by adding an event listener and continuously monitoring for barcode scans. While not ideal, this workaround ensures consistent detection.