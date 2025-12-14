# JPEG Image Compression – Mini Project

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

 **JPEG image compression**, demonstrating the full baseline JPEG pipeline using Python. This project focuses on frequency-domain compression, exploiting perceptual redundancy, and rate–distortion trade-offs.

---

## 📌 Project Highlights

* End-to-end JPEG compression workflow
* Block-based **8×8 DCT** implementation
* Quantization and reconstruction analysis
* Objective quality evaluation (**MSE, PSNR**)
* Visual comparison of original vs compressed images

---

## 📂 Repository Structure

```
├── JPEG_Compression__miniProject.ipynb   # Main implementation notebook
├── input_images/                         # Test images (user-provided)
├── output_images/                        # Reconstructed images
├── README.md                             # Project documentation
```

---

## 🧠 JPEG Compression Pipeline

1. **RGB → YCbCr Conversion**
   Separates luminance and chrominance to exploit properties of the human visual system.

2. **Block Segmentation**
   Image divided into non-overlapping **8×8 blocks**.

3. **2D Discrete Cosine Transform (DCT)**
   Converts spatial-domain data into frequency-domain coefficients with energy compaction.

4. **Quantization (Lossy Stage)**
   DCT coefficients are quantized using JPEG-standard matrices, controlling compression strength.

5. **Zig-Zag Scanning (Conceptual)**
   Rearranges coefficients for efficient entropy coding.

6. **Reconstruction**
   Dequantization followed by inverse DCT (IDCT).

---

## ⚙️ Requirements

```bash
pip install numpy opencv-python pillow matplotlib
```

---

## ▶️ How to Run

```bash
jupyter notebook JPEG_Compression__miniProject.ipynb
```

1. Load an image into the input directory
2. Run cells sequentially
3. Observe compression stages and metrics

---

## 📊 Evaluation Metrics

* **Mean Squared Error (MSE)**
* **Peak Signal-to-Noise Ratio (PSNR)**

These metrics quantify reconstruction quality and compression loss.

---

## 🔍 Key Observations

* Low-frequency DCT coefficients carry most visual information
* Quantization dominates compression efficiency
* Higher compression introduces blocking and ringing artifacts
* Luminance fidelity is perceptually more critical than chrominance

---

## 🚀 Applications

* Image storage and transmission
* Multimedia systems
* Embedded vision systems
* Computer vision preprocessing

---

## ⚠️ Limitations

* Baseline JPEG only
* Simplified / conceptual entropy coding
* No rate-control optimization

---

## 📚 References

1. G. K. Wallace, “The JPEG Still Picture Compression Standard,” *IEEE Trans. Consumer Electronics*, 1992.
2. R. C. Gonzalez, R. E. Woods, *Digital Image Processing*, Pearson, 2018.
3. K. R. Rao, P. Yip, *Discrete Cosine Transform*, Academic Press, 2014.
4. W. B. Pennebaker, J. L. Mitchell, *JPEG Still Image Data Compression Standard*, Springer, 1993.

---

