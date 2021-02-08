At first cv2.VideoCapture('green_hand.mp4') is used to load the video.

Then each frame in the video is first stored in a variable called "frame" and then an "if" statement, which only gives a true value when every 10th frame is accessed, stores the video in an empty array called new_video.

Then the new_video array is converted into a numpy array so that it maybe be used to convert it back into a video.

It outputs a video "new_video.avi"