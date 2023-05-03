# Image_Homography_Panoramic_CV2

## Assignment: Features, Matching and Homographies

### Part 1:

Homography-based planar object detection (4 pts)
The goal of this part of the assignment is to develop a system for localizing a planar textured
object in an image, when the texture does not present repetitive structures.
The classical pipeline to solve the textured object localization consists of the following steps 1)
extract local features, 2) extract scale- and orientation-independent feature descriptors, 3)
match the local features in the query image using the model and query descriptors, and 4)
robustly estimate the homography matrix between the model and the query image.
Once the camera resection has been performed from an estimated homography, this
information is used to insert another image, with the correct perspective, that appears to be
part of the original scene.

### Part 2: 
Stitch multiple images together to create a wide view panorama (5 pts)
The goal of this part of the assignment is to combine five horizontally overlapping photographs
into a single panoramic image. Images must be supplied in left-to-right order.
Before you can warp your images to align them, you need to recover the parameters of the
transformation between each pair of images. Once you get this far, you should be able to
“rectify” each image and create an image mosaic. You can leave one image unwarped and
warp the other images over its projection, or you can warp all images over a new projection.

- Optional 1 (1 pts): If you join only five images, you will not have any difficulty, as it is a
simple process. But in the case of joining seven, you will see that the images near the
sides start to distort. Instead of projecting the mosaic on a plane, try using another
surface, such as a sphere or cylinder to avoid this unwanted effect.
- Optional 2 (1 pts): In order to create a panorama, it is necessary that the images are
labeled in such a way that the order of the images is obtained from left to right. Try to
eliminate this condition and design an algorithm that constructs a panorama without
the knowledge of the order of the images.
Note: You cannot use the Stitcher class provided by OpenCV.
