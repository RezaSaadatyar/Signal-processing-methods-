
**Welch's Method for Smooth Spectral Decomposition**<br/>
Welch's method is a technique for estimating the power spectral density (PSD) of a signal. It improves upon the periodogram method by dividing the signal into overlapping segments, applying a window function to each segment, and averaging the resulting periodograms to obtain a smoother PSD estimate.<br/>
**Steps:**
- `Segmentation:` Divide the signal into overlapping segments to preserve information.
- `Windowing:`Apply a window function (e.g., Hamming) to each segment to reduce spectral leakage.
- `Computing Periodograms:` Calculate the squared magnitude of the discrete Fourier transform (DFT) for each windowed segment.
- `Averaging Periodograms:` Average the individual periodograms to obtain the final smoothed PSD estimate.<br/>
If $P_i(f)$ is the periodogram of the $i^{th}$ segment and N is the total number of segments, then the smoothed PSD estimate, S(f), is given by:
$S(f) = \frac{1}{N} \sum_{i=1}^{N} P_i(f)$<br/>

| Aspect                        | Welch's Method                                         | FFT (Fast Fourier Transform)                          |
|-------------------------------|--------------------------------------------------------|------------------------------------------------------|
| **Purpose**                   | Estimate Power Spectral Density (PSD)                  | Compute the Discrete Fourier Transform (DFT)        |
| **Output**                    | Smoothed PSD estimate                                  | Complex-valued spectrum with amplitudes and phases   |
| **Segmentation**              | Divides signal into overlapping segments               | Analyzes the entire signal without segmentation      |
| **Windowing**                 | Applies window function to each segment                | Typically applied to reduce spectral leakage         |
| **Averaging**                 | Averages periodograms from different segments          | No explicit averaging, provides global frequency view|
| **Resolution**                | Provides smoother representation of spectral content   | High-frequency resolution, but may suffer from leakage|
| **Use Case**                  | Effective for non-stationary signals, reduces variance | General-purpose for frequency analysis of a signal    |
---


