# cyclotron_emission

`cyclotron_emission` is a Python notebook to calculate the cyclotron emission spectrum of a blob of homogeneous plasma of certain temperature in a uniform magnetic field of a certain strength, as observed at a certain angle. It was written by Nadia Zakamska. This notebook is written for Python 3, and it depends on `numpy, scipy, matplotlib`. For illustration purposes it also uses `IPython`. If you use `cyclotron_emission` in your research, please cite https://ui.adsabs.harvard.edu/abs/2022arXiv221114945L/abstract.

The notebook is fully self-contained. It starts with snapshots of the relevant equations with references provided. Then it defines and tests some ancillary functions. Then it defines the main function (`ComputeSpec`), which codes the analytical expressions basically exactly as they were written in the original papers. 

After this, there is an extensive library of comparison of the spectral calculations with the published results, which reveals that the code produces infuriatingly similar, but not identical results to those that appear in the literature. In particular, the overall shape of the spectral energy distribution (SED) calculated using my code seems a little off and biased toward the shorter wavelengths in comparison to published works. It is possible that there is a coding mistake. If you find the coding mistake, please contact me as soon as possible. 

## Contact

Feel free to contact me: zakamska@jhu.edu

