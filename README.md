## JPEG Image Compressor

A JPEG-style image compressor, implementing core ideas behind real-world JPEG compression including:

- RGB -> YCbCr colour space conversion
- Chroma subsampling (4:2:0)
- Discrete Cosine Transform (DCT)
- Quantization
- Image reconstruction using Inverse DCT

---

## Discrete Cosine Transform (DCT)

Instead of storing pixels directly, DCT asks:

> “Can we express this image as a sum of cosine waves?”

It leverages the fact that the human eye is far more sensitive to **brightness (luminance)** than subtle **colour variations (chrominance)**.

Thus, visually insignificant high-frequency details can be discarded with minimal perceptual loss.

So after applying DCT:

- low-frequency coefficients carry most of the important visual information
- high-frequency coefficients are often tiny and can be compressed or thrown away
