# Face-API Essential Functionality Test

This test verifies that all the essential components you're using in your project still work correctly:

- ✅ TinyFaceDetector
- ✅ FaceLandmark68Net (with methods like `getLeftEye()`)
- ✅ FaceRecognitionNet (face descriptors)
- ✅ FaceExpressionNet
- ✅ LabeledFaceDescriptors
- ✅ FaceMatcher

## Setup

1. **Install canvas dependency:**
   ```bash
   npm install canvas
   ```

2. **Run the test:**
   ```bash
   node test-essential.js
   ```

## What the test does

1. Loads all 4 models from the `./model` directory
2. Creates a simple test image
3. Runs face detection with all features
4. Tests landmarks extraction (including `getLeftEye()` used in your code)
5. Tests face descriptors and FaceMatcher (for face recognition)
6. Tests expression detection
7. Provides a comprehensive summary

## Expected Output

You should see:
- ✅ Model loading confirmation
- Face detection results (may not detect faces in simple test image)
- Landmarks, descriptors, and expressions availability confirmation
- Test summary showing all components are working

## Note

The simple test image may not contain a detectable face - this is normal. The important part is that all models load successfully and the API functions are available and working.

For a real-world test, you can modify the script to load an actual photo instead of the generated test image.

## Troubleshooting

If you see module errors:
- Make sure you're in the face-api directory
- Ensure `canvas` is installed: `npm install canvas`
- Check that the `dist/face-api.esm.js` file exists
- Check that the `model/` directory contains the 4 required model files

If canvas installation fails, you may need to fix npm permissions:
```bash
sudo chown -R $(whoami) ~/.npm
```

