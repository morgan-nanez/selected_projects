Project 3: Face Morhping
========================

Overview
--------

In this project, I  produce a "morph" animation of my face into someone else's face. I also compute the mean  of a population of faces and extrapolate from the population mean to create a caricature of myself.

 

### Defining Correspondences

I begin by importing two images, one of me and one of Jennifer Lawrence.

<table>
<col width="50%" />
<col width="50%" />
<tbody>
<tr class="odd">
<td align="left"><p><img src="inputs/morgan_face.jpeg" alt="Morgan face" /></p>
<p>My face</p></td>
<td align="left"><p><img src="inputs/jen_face.jpg" alt="jen_face" /></p>
<p>AOC's face</p></td>
</tr>
</tbody>
</table>

I use the previously defined aligning method that was provided to us in Project 2 to align and reshape the images into the same measurments. I then manually inputted 25 corresponding points on each image that will be used to create a triangulation of the image for morhping purposes

### Computing the "Mid-way Face"

First, I computed the avergae shape. This involved going through each corressponding points for the images, and calculating the average bewteen the two. Then, I compute the triangulation from the avgerage points and get coressponding points on each image. Then, I calculate the transformation matrix bewteen the mid-way point and the original image, apply this tranfomration on each triangle to attain the warped image, and finally  interpolate the color pixels from original image to get the color of the warped picture.

<table>
<col width="100%" />
<tbody>
<tr class="odd">
<td align="left"><p><img src="outputs/morphed_midway.jpg" alt="midway face" /></p>
<p>Mid-way face</p></td>
</tr>
</tbody>
</table>

 

 

### The Morph Sequence

To get the morphing sequence, I created 30 frames, iterating over a warp\_frac, which affects the shape, and a  dissolve\_frac, which affects the the color.

<table>
<col width="100%" />
<tbody>
<tr class="odd">
<td align="left"><p><img src="outputs/morph.gif" alt="morph.gif" /></p>
<p>Morph video</p></td>
</tr>
</tbody>
</table>

### The "Mean face" of a population

I computed the mean face of females' straight faces from the Danes dataset. I then morphed my face to the mean face, and the  mean face to my geometry.

![mean face](outputs/avg_morphs/morph_average.jpg)

Mean Face

<table>
<col width="33%" />
<col width="33%" />
<col width="33%" />
<tbody>
<tr class="odd">
<td align="left"><p><img src="imm_face_db/08-1f.jpg" alt="face 1 reg" /></p>
<p>Face 1</p></td>
<td align="left"><p><img src="imm_face_db/12-1f.jpg" alt="Face 2" /></p>
<p>Face 2</p></td>
<td align="left"><p><img src="imm_face_db/35-1f.jpg" alt="Face 3" /></p>
<p>Face 3</p></td>
</tr>
<tr class="even">
<td align="left"><p><img src="outputs/avg_morphs/morph0.jpg" alt="face 1 morph" /></p>
<p>Face 1 Morphed</p></td>
<td align="left"> 
<p><img src="outputs/avg_morphs/morph4.jpg" alt="face 1 morph" /></p>
<p>Face 2 Morphed</p></td>
<td align="left"><p><img src="outputs/avg_morphs/morph6.jpg" alt="face 1 morph" /></p>
<p>Face 2 Morphed</p>
 </td>
</tr>
</tbody>
</table>

![me to mean](outputs/me_morphed_to_avg.jpg)

My face morphed to mean geometry

![Mean geometry morphed to my face](outputs/avg_morphed_to_me.jpg)

Mean geometry morphed to my face

 

### Caricatures: Extrapolating from the mean

To produce a caricature of myself I used the average points calculated above and then extrapolated from those by computing a new set of points, caricature points.

<table>
<col width="100%" />
<tbody>
<tr class="odd">
<td align="left"><p><img src="outputs/my_caricature.jpg" alt="caricature" /></p>
<p>Caricature</p></td>
</tr>
</tbody>
</table>

### Bells and Whistles

One: Different Gender

<table>
<col width="33%" />
<col width="33%" />
<col width="33%" />
<tbody>
<tr class="odd">
<td align="left"><p><img src="outputs/gif_morph_gender/gender_shape.gif" alt="Morphing Just Shape" /></p>
<p>Morphing Just Shape</p></td>
<td align="left"><p><img src="outputs/gif_morph_gender/gender_app.gif" alt="Morphing Just Appearence" /></p>
<p>Morphing Just Appearence</p></td>
<td align="left"><p><img src="outputs/gif_morph_gender/gender_full.gif" alt="Full Morph" /></p>
<p>Full Morph</p></td>
</tr>
</tbody>
</table>

Two: Different Facial expression

<table>
<col width="33%" />
<col width="33%" />
<col width="33%" />
<tbody>
<tr class="odd">
<td align="left"><p><img src="outputs/gif_morph_face/face_shape.gif" alt="Morphing Just Shape" /></p>
<p>Morphing Just Shape</p></td>
<td align="left"><p><img src="outputs/gif_morph_face/face_app.gif" alt="Morphing Just Appearence" /></p>
<p>Morphing Just Appearence</p></td>
<td align="left"><p><img src="outputs/gif_morph_face/face_full.gif" alt="Full Morph" /></p>
<p>Full Morph</p></td>
</tr>
</tbody>
</table>


