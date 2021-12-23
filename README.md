# Seam_Carving
Seam Carving Algorithm Used to Crop Images

The purpose of this project was to implement a version of the seam carving algorithm used to crop images effectively in Photoshop. With seam carving, an imaged is cropped by
making a seam across it that contains one pixel line. Each pixel from within the seam is then removed from the image. In order to determine which pixels to include
in the seam, each pixel is given an energy value depending on how important it is for the image to be recognizable. At each iteration, the seam used to crop
consists of the set of pixels that have the least total energy.

To determine which seam has the least total energy efficiently, the dynamic programming was used. The idea was to create a two-dimensional
matrix that represents the energy of each pixel in the image in the corresponding matrix position. From there, a second matrix was filled from the bottom
to the top with the least-cost path from that point to the bottom of the matrix. From there, finding the least cost seam was simply a matter of picking the least-cost
path at the top of the matrix and choosing the minimum of the three values just below that position. In the cases when a pixel at the edge of the image was evaluated,
the minimum of the bottom two pixels was picked.
