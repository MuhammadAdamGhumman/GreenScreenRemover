As in Task0, the video to edit is accessed through cv2.VideoCapture('green_hand.mp4') function.

Most of the code is the same as Task0, excpect for the fact that this time all frames of the video are processed, not just every 10th.

As well as the smiley face, which I have added through 3 for loops.

These for loops only run on the first 100 frames of the video because of the "if" statment they are enclosed in

For the shapes the for loops change the colour values of all the frames in their range(which depicts the pixels), the values are changed to (0, 0, 0) which is black.

It outputs a video "green_hand_smiley.avi"