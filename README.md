# HEALSparse Tutorial for LSST

In sky surveys, we often want to characterize the different properties of our survey such as the limiting magnitudes for 5-sigma detections, the average seeing conditions for exposures, or just simply the coverage in different bands! If we want to do this for an ENTIRE sky survey (especially one as big as LSST!), we're going to need to be smart about how we do it! Enter: HEALSparse!

HEALsparse builds off the idea of a HEALpix map, which stands for **H**ierarchical **E**qual **A**rea iso**L**atitude **Pix**elization. More can be found [here](https://healpix.sourceforge.io/). Essentially, you're able to take a 1-dimensional array and project it onto the entire sky following their algorithm. It was developed for analysis of the CMB, but lots of the cool and quirky cosmologist and survey science folks love to use it!

HEALsparse implements sparse matiricies to make high resolution HEALpix maps of sky surveys quickly and efficiently. Since large portions of the sky often have the same value, its easier to instead create a low-resoltuion HEALpix map, and if there is coverage in one of these low-resolution pixels, we can store a high-resolution map in the low-resolution pixel. This might sound confusing and if it does that's okay because it does still lowkey feel like magic to me, but it works and that's all a gal can ask for! 

Anyways, here's a tutorial for folks since one could imagine that this won't be the last time this question comes up!