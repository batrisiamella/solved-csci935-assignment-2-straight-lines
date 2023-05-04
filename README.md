Download Link: https://assignmentchef.com/product/solved-csci935-assignment-2-straight-lines
<br>
Design a C or C++ (ANSI standard) program that can extract object edges and detect the presence of straight lines.

<h1>BACKGROUND</h1>

Automated visual quality control and visual monitoring of industrial assembly lines are the application areas where computer vision has proven its efficiency. Vision systems can operate continuously and provide measurement of critical parameters such as position and orientation of objects, their shape, colour, etc. An obvious advantage of such systems is the possibility of controlling image acquisition process optimising illumination, position of cameras and background colour. As a result, images used for automated visual inspection have good quality in terms of contrast and SNR.

Your program shall include the following stages:

<ol>

 <li>Rescale the image down by the factor of 2, to reduce computational complexity of the subsequent stages</li>

 <li>Extract boundaries of objects using 3×3 gradient operators</li>

 <li>Save the generated b/w image bmp</li>

 <li>Detect the presence of straight lines and measure their orientation with the precision 3<sup>o</sup></li>

 <li>Extract boundaries of objects using binary morphology</li>

 <li>Save the generated b/w image bmp</li>

 <li>Detect the presence of straight lines and measure their orientation with the precision 3<sup>o</sup> Compare performance and efficiency of both methods and reflect your observations, findings and conclusions in the report assignment2report.txt</li>

</ol>

<h1>DESIGN SPECIFICATION</h1>

You need to use OpenCV library to implement the solution.

It can be tested using asm2.bmp test image. Since information about colour is not required, it contains only 8bit/pix luminance component. The image size is 640×480.

Your program shall produce:

<ol>

 <li>Two 8bit/pix black/white (b/w) images bmp and morphology.bmp ( size 320×240), which represent object boundaries obtained by two boundary extraction methods. The level of background should be set to 0 (black), while the pixels corresponding to boundaries are set to 255 (white). <em> </em></li>

</ol>

<em>Comments:</em> You may try to apply a LPF before the gradient-based method to improve overall accuracy of edge detection. If needed, you can also apply binary morphological methods ( erosion, dilation, etc) to smooth boundaries obtained as a thresholded output of the gradient-based method.




Considering the second solution, before applying the morphological boundary detection method, you need to binarize the input image first. The test image provided has a very high contrast and therefore selection of a threshold is not very difficult. For asm2.bmp the threshold can be set around 90-100.




<ol start="2">

 <li>For each boundary detection method you need to printout parameters of all detected lines in the following format:</li>

</ol>




Line detection in a b/w image produced by gradient operators:

Line 1 is detected.  Orientation = … degrees  Line 2 is detected.  Orientation = … degrees <em>or</em>

No straight lines detected




Having implemented and tested the program, you should investigate some practical aspects of boundary extraction and straight-line detection. For example:

<ul>

 <li>You can compare accuracy and computational complexity of two boundary detection methods</li>

 <li>You can evaluate efficiency of edge detection with LPF pre-processing and without it</li>

 <li>You can measure computational complexity and execution time of Hough Transform – You can analyze sensitivity of your system to noise by running the program with the second test image bmp</li>

</ul>

Your observations, findings and conclusions must be summarized in the report  assignment2report.txt

<strong> </strong>