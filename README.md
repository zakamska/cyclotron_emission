# cyclotron_emission

`cyclotron_emission` is a Python notebook to calculate the cyclotron emission spectrum of a blob of homogeneous plasma of certain temperature in a uniform magnetic field of a certain strength, as observed at a certain angle using equations from Chanmugam and Dulk 1981 (hereafter CD81). It was written by Nadia Zakamska. This notebook is written for Python 3, and it depends on `numpy, scipy, matplotlib`. For illustration purposes it also uses `IPython`. If you use `cyclotron_emission` in your research, please cite Liu et al. 2023 https://ui.adsabs.harvard.edu/abs/2023MNRAS.522.2719L/abstract. 

The notebook is fully self-contained. It starts with snapshots of the relevant equations with references provided. Then it defines and tests some ancillary functions. Then it defines the main function (`ComputeSpec`), which codes the analytical expressions basically exactly as they were written in the original CD81 paper, with one modification to express the electron density in terms of the dimensionless Lambda as defined in Schwope et al. 1990. 

After this, there is an extensive library of comparison of the spectral calculations with the published results, which reveals that the code produces infuriatingly similar, but not identical results to those that appear in the literature. In particular, the overall shape of the spectral energy distribution (SED) calculated using my code seems a little off and biased toward the shorter wavelengths in comparison to published works. It is possible that there is a coding mistake. If you find the coding mistake, please contact me as soon as possible. 

This code explicitly assumes that the index of refraction (eq. 1 from CD81) and ray-refractive index (eq. 7 from CD81) are exactly 1. In practice, the deviations from 1 are proportional to the square of the ratio of the plasma frequency to the observed frequency. This ratio is in the ballpark of 1e-15 for typical cataclysmic variables, and therefore I have decided to lighten the code and not include eq. 1 nor propagate plasma frequency as a parameter of the model, especially since I don't have the ray-refractive index from eq. 7 anyway. I have a longer and heavier code which propagates a non-zero plasma frequency through the equations and I have verified that it makes no difference for the relevant situations. I have also verified that the calculations presented here are in agreement with Meggitt and Wickramasinghe 1982 in the optically thin case (which is the one they are considering).  

## Contact

Feel free to contact me: zakamska@jhu.edu

