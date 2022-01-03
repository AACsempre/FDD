# FDD
## Frequency Domain Decomposition (FDD).
The FDD is a popular method used in structural health monitoring. It is a modal analysis technique which generates a system realization using the frequency response given output measurements.

## Content
Given a set of accelerograms of time series data, the FDD method used in these scripts involves first estimating the power spectral density (PSD) matrices, and then perform their singular value decomposition (SVD). After this, the eigenfrequencies can be determined, either manually or automatically.<br>
<br>
In this notebook, it is first possible to obtain the Fast Fourier Transform (FFT) and the cross PSD from the raw time series data. The PSD can be plotted. Then, after the SVD is computed, the first singular vectors can also be plotted. In this script, the estimation of the modal eigenfrequencies should be made manually, after all SVD data is collected. <br>
<br>
The FDD make use of the python pandas, numpy and scipy libraries. Matplotlib is also used for the plots.<br>
<br>
The input data file consists of a csv file. Each column corresponds to an accelerogram. The first rows might correspond to a header, which can be ignored. <br>
The input parameters are contained within the notebook, as follows: <br>
- folder_inp: input folder name <br>
- file_inp: data input file name <br>
- folder_out: output folder name <br>
- h_cor: Do not consider first h_cor rows (Header) <br>
- Freq: Sample Frequency [Hz] <br>
- npers: Length of each segment <br>

## References
[1] Brincker, R., Zhang, L., & Andersen, P. (2001). Modal identification of output-only systems using frequency domain decomposition. Smart materials and structures, 10(3), 441. doi:10.1088/0964-1726/10/3/303.<br>
[2] https://www.mathworks.com/matlabcentral/fileexchange/50988-frequency-domain-decomposition-fdd <br>
