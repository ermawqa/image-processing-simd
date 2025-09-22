# SIMD-based Image Tone Mapping

This project was developed as part of the **Grundlagenpraktikum Rechnerarchitektur** at TUM.

---

## 🧩 Project Summary

The program performs grayscale conversion and tone value correction on `.ppm` images using:

- Command-line argument parsing (`getopt_long`)
- Grayscale conversion using human visual coefficients
- Interpolation of tone value coefficients
- SIMD optimization with **SSE** and **AVX** for performance

---

## 🧪 Performance

- **SSE**: ~7× faster than scalar version (V0)
- **AVX**: ~11× faster than scalar version, 1.5× faster than SSE

Benchmarks were run on an Intel i5 (11th Gen) CPU using automated scripts.

---

## 🗂️ File Structure

- `src/` — Core source code
- `res/` — Sample images (input/output)
- `benchmarks/` — Performance scripts and results
- `docs/` — Project documentation, including [Vortrag.pdf](docs/Vortrag.pdf)

---

## 📷 Example Command

```bash
./main ../res/uhren_tum.ppm -o output.pgm -V 2 --coeffs 2,3,1

---

## 🛠️ Technologies Used
	•	C/C++
	•	Netpbm image format
	•	SIMD intrinsics: SSE, AVX
	•	Benchmarking with gettimeofday
	•	Memory checks: Valgrind, Sanitizer

## 👥 Contributors
	•	Cagatay Cem Aksoy
	•	Ron Spannagel
	•	Yermukhamed Shakhman
