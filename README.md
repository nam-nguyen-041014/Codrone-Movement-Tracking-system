# CoDrone Movement Tracking System

  What started out as a side project became an important module that I soon found very interesting. Wanting to create a camera based module that tracks movements, I got out many tutorials and learned many things to master this skill. The subject soon bloomed into many different projects, this one included. For the module I am showing you now, I combined movement tracking with drones (The class I was taking back then), and created a module where I controlled the drone using body movements.

---

## Startoff:

  Firstly, I started off with a basic camera module,(which basically just activated my camera) and from there I officially started! I began researching pose landmark detection guides, and found one with the exact name! It was a Google site collaborating with OpenCV, a visual and pose detecting library (which frankly, I only used to set up the camera) in which they made the pose landmark detection system I used as part of my code! To make the movement tracking script, I used OpenCV along with another library, Mediapipe. Then I created the feed with OpenCV using this line of code: -self.cap = cv2.VideoCapture(self.video_source)- and started on the actions. It took quite a bit, but then finalized on creating variables that I could later use for other lines and functions.

---

## Creating the actions:

  As said in previously, I soon found out that variables would work best for this type of code. I created the line 'self.action_#_angle(the # symbol would be replaced with numbers later on) to store my motions. I wanted to do some basic exercise movements, so I did a simple dumbbell lifting action using 3 landmarks;wrist, elbow, and shoulder. It needed to be called from the library, so I used a line to bring it into my code (example:LEFTwrist = np.array([landmarks[self.mp_pose.PoseLandmark.LEFT_WRIST.value].x,landmarks[self.mp_pose.PoseLandmark.LEFT_WRIST.value].y])). I had to make sure to include all of the landmarks, or else I couldn't make full angles.

## Calculating the Action Angles:




