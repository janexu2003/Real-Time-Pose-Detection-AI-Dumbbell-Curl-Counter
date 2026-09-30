# AI Dumbbell Curl Counter

A real-time computer vision application that tracks and counts dumbbell bicep curls using OpenCV and MediaPipe.

Inspired by [Nicholas Renotte's MediaPipe Pose Tracking tutorial](https://www.youtube.com/watch?v=Ae3SPjsXETc).

**Real-Time Pose Estimation**: Tracks 3D skeletal landmarks (Shoulder, Elbow, Wrist) using MediaPipe Pose.   
**Angle Calculation**: Computes the joint angle at the elbow in real-time using vector mathematics (arctan2).   
**Repetition & Stage Counting**:Detects "DOWN" stage when the arm is fully extended (elbow angle > $160^\circ$).Detects "UP" stage when the dumbbell is lifted (elbow angle < $30^\circ$).Increments the repetition counter automatically upon completing a valid rep.    
**HUD Overlay**: Displays dynamic rep counts, current rep stage (UP/DOWN), and real-time elbow angle directly on the live camera feed.