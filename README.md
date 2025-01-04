# Expo Image Component URI Issue

This repository demonstrates a bug in the Expo `Image` component where it fails to load local images if the URI contains special characters (spaces, accented characters, etc.). The issue is that the image load fails silently, without any errors in the console, making it difficult to debug.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe that the image with special characters in the URI fails to load. 

## Solution

The solution involves URL-encoding the URI before passing it to the `Image` component's `source` prop. This ensures that the special characters are properly handled.

## Contributing

Contributions are welcome!