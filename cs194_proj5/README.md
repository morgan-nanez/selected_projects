Project  5.1: Image Warping and Mosaicing {style="color: #5e9ca0;"}
=========================================

Shoot the Pictures
------------------

Here are the digitized input images I used. The top row is the an
outdoor view. It had a stright wire pole and building edges that can  be
used to make sure the alignment is correct. The bottom row is an indoor
view. It has a straight line at the top as well other sharp corners.

+--------------------------+--------------------------+--------------------------+
| ![source                 | ![source                 | ![source                 |
| 1](part1_inputs/outside1 | 1](part1_inputs/outside2 | 1](part1_inputs/outside3 |
| .jpg)Outside             | .jpg)                    | .jpg)                    |
| Image 1                  |                          |                          |
|                          | Outside Image 2          | Outside Image 3          |
+--------------------------+--------------------------+--------------------------+
| ![source                 | ![source                 | ![](part1_inputs/inside3 |
| 1](part1_inputs/inside1. | 1](part1_inputs/inside2. | .jpg)                    |
| jpg)                     | jpg)                     |                          |
|                          |                          | Inside Image 3           |
| Inside Image 1           | Inside Image 2           |                          |
+--------------------------+--------------------------+--------------------------+

Recover Homographies
--------------------

I used 10 corresponding points for each image when calculating the
transofrmation between two images.  Because I used 10 points, in order
to avoid an overdetermined system, I solved the homography using
least-squares.

Warp The Image / Image Rectification
------------------------------------

Here are the results of my warping. The first image is warping from a
trapezoid, or a square in different perspective, to a sqaure. The second
is a slanted building into somewhat of a rectangular building.

+--------------------------------------+--------------------------------------+
| ![source                             | ![source                             |
| 1](part1_inputs/trapezoid.jpg)       | 1](part1_outputs/rectifiedtrapezoid. |
|                                      | jpg)                                 |
| Trapezoid                            |                                      |
|                                      | Warped Trapezoid into Sqaure         |
+--------------------------------------+--------------------------------------+
| ![source                             | ![source                             |
| 1](part1_inputs/diagonal_building.jp | 1](part1_outputs/rectifieddiagonal_b |
| g)                                   | uilding.jpg)                         |
|                                      |                                      |
| Slanted Building                     | Warped Slanted Building into a       |
|                                      | Rectangle                            |
+--------------------------------------+--------------------------------------+

 

Blending Into Mosaic
--------------------

Below is the result of blending mulitple of my warped images together
into one image. I used a linear blending technique and whited out the
edges.

+--------------------------------------------------------------------------+
| ![source 1](part1_outputs/blended_outside.png)                           |
|                                                                          |
| Blended Outside Image                                                    |
+--------------------------------------------------------------------------+
| ![source 1](part1_outputs/blended_inside.png)                            |
|                                                                          |
| Blended Inside Image                                                     |
+--------------------------------------------------------------------------+

What I Learned
--------------

The most interesting thing that I learned was about creating and
applying homography transformations uniformly to an entire image. It's
very interesting how you can apply one transformation for an entire
image, just to switch perspective.

Project  5.2: Auto Stitching {style="color: #5e9ca0;"}
============================

Harris Interest Points
----------------------

Below is the result of getting Harris interest points on my images. The
points are shown overlaid a sample images

+--------------------------------------------------------------------------+
| ![source 1](part2_outputs/harris_points.jpg)                             |
|                                                                          |
| Harris Interest Points                                                   |
+--------------------------------------------------------------------------+

Adaptive Non-Maximal Suppression
--------------------------------

Below is the result of applying Adaptive Non-Maximal Suppression to the
Harris Points

+--------------------------------------------------------------------------+
| ![source 1](part2_outputs/plotted_points.jpg)                            |
|                                                                          |
| New Points                                                               |
+--------------------------------------------------------------------------+

Final Outcome
-------------

Below is the result after warping and blended the images (with same
logic as above), using the auto generated points

+--------------------------------------------------------------------------+
| ![source 1](part2_outputs/blended_inside.png)                            |
|                                                                          |
| Final Mosaic Indoor                                                      |
+--------------------------------------------------------------------------+

+--------------------------------------------------------------------------+
| ![source 1](part2_outputs/blended_outside.png)                           |
|                                                                          |
| Final Mosaic Outdoor                                                     |
+--------------------------------------------------------------------------+

What I Learned From Part B
--------------------------

The coolest thing I learned is the matching of features using gradients
and blurring! I'm amazing by how something seemingly trivial as SSD math
between two patches can match features quite accurately
