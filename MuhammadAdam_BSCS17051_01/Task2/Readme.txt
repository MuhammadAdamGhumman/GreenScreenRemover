Once more the code is mostly the code from Task 0.

Key changes are the addition of the fucntion cv2.cvtColor() which is used to convert each frame from RGB to HSV so that we may find the correct colour we want to mask.

The "if" statement  "if (i==i):" was just to make it easier to quickly change the number of frames I was processing.

Next, a variable(invmask) is made which containts the image 'green_hand_background.jpg', for green hand video, and 'green_cloak_background.jpg' for green cloak video, which is a still frame of the background of the video without the green hand, as I would just change the value with which "i" was being compared to.

Next, two for loops are used to do all the masking and produce a final frame which has made the green hand loop like it's invisible.

The first loop denotes the x-axis pixels while the second denotes the y-axis pixels.

Inside the loops is an if statement which checks to see if the Hue of the pixel on the frame has a value between 30 to 60, for green hand video, and 57 to 70 for green cloak video. If it does that pixel is mapped as (0, 0, 0) in the mask array, else it is mapped as (255, 255, 255)
This creates a binary image which contains the masking of the green hand in the frame.

Everytime the Hue value is between 30 to 60, for green hand video, and 57 to 70 for green cloak video, the pixel of frame is also updated with a corresponding from the invmask variable to produce the invisibility effect.
