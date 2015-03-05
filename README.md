# XCT-Processing
bpcroom

SOFTWARE REQUIREMENTS:
===================================================
Written in Python v3.3 with standard numerical package dependencies (Numpy, Scipy, Matplotlib, etc.).

OVERVIEW:
===================================================
This package is facilitates processing of  XCT data. Standard input is in the form of 2D slices of the reconstructed XCT data, which are often saved as TIF images or other lossless image formats.

Although these "raw" slices contain rich information about the reconstructed specimen, they are very large and unwieldy (e.g., 1000+ 1 megapixel, 16 bit images...). Naturally the first order of business is reducing data to a manageable size, which is performed by intensity- and geometry-based segmentation methods. By assign thresholds for different constituent materials, we can assign similar-material voxels a single color. These simplified images can reduce a ~5 MB slice into a ~30 KB image.

We can easily process these segmented images to calculate statistics of interest, such as porosity or other volume fractions. Futhermore, we can identify spatial trends in the data. In the case of a fiber reinforced composite, we can calculate fiber orientation by correlating imitation fiber elements against the segmented image; strong correlation suggests that the reconstructed image contains fiber orientation similar to the imitation fiber.
