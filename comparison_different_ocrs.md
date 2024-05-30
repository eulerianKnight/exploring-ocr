# A Comparitive Study between different OCRs



## Tesseract

### PROS

- Optimized for CPU, and has wrappers in multiple programming languages
- Still a better open-source option for scanned documents
- Multilingual and other configuration options
- Has Docker support

### CONS

- Since it uses the classical page layout analysis technique, text detection is not as accurate compared to its deep learning peers and cannot be directly used for scene text detection. However, using CRAFT /EAST for Text Detection(Deep learning models and supports multilingual text detection) and then using Tesseract for Text Recognition will yield better results in STR.
- Not Optimized for GPU and batch processing

## EasyOCR

### PROS

- Well suited for Scene Text Recognition
- Pytorch Deep learning models for Detection, Recognition
- Implementation roadmap shows configurable options for Detection, Recognition and Decoding steps in the future, and also Handwritten Recognition
- GPU support and batch prediction, faster compared to Tesseract’s OpenCL version
- Multilingual and Vertical Text Support
- Includes Options for Whitelisting, Blacklisting, output_format, Image manipulations

### CONS

- Slower than Tesseract in CPU Mode
- Not better than Tesseract for Scanned Documents

## PaddleOCR

### PROS

- End-to-End OCR Models
- Data Synthesis and Semi-Automated OCR annotation solutions
- Multilingual OCR Support
- Different Inference and Serving Options, Benchmarks

### CONS

- Has dependency on paddlepaddle
- Need to use external libraries for Paddle to Pytorch / ONNX conversion

