# steganography
The Jupyter Notebook shows how to hide image A under image B. The idea is very simple.

1. Convert image A from RGB to binary, i.e., a black and white image. For image A, pixel values are just 0 or 1. Now the shape is (width, height).

2. Convert pixel values of image B to binary numbers. For image B, pixel values are binary numbers within 8 bits. Now the shape is still (width, height, 3).

3. Choose one channel of image B. Replace the last digit of the pixel values of that channel with the pixel values of A.

4. Convert the binary pixel values of image B back to decimal numbers. And we are done with the encoding part!

As for the decoding part, we can just undo what we have done. Find the channel we have chosen, convert the pixel values of the encoded image to binary numbers, then extract the last digit.

Note: The decoded image is a black and white image, so there is some information loss. Also the decoded image might be resized.
