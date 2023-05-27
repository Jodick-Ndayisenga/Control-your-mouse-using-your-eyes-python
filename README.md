# Eye controller

This code performs eye-controlled mouse movements and clicks using the webcam and facial landmark detection. Here's how it works:

    The code imports the necessary modules: cv2 for capturing video from the webcam and image processing, mediapipe for facial landmark detection, and pyautogui for controlling the mouse cursor.

    The webcam capture is initialized using cv2.VideoCapture(0).

    The face mesh detection model is initialized using mp.solutions.face_mesh.FaceMesh() with the refine_landmarks=True option to enable more accurate landmark detection.

    The screen size is retrieved using pyautogui.size().

    Inside the main loop:
        A frame is read from the webcam using cam.read().
        The frame is flipped horizontally using cv2.flip() to mirror it.
        The frame is converted to RGB format using cv2.cvtColor().
        The face mesh detection model processes the RGB frame using face_mesh.process(), and the output is