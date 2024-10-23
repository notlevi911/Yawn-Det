# Drowsiness and Yawn Detection with Voice Alert Using Dlib

## Overview

This project implements a drowsiness and yawn detection system using Dlib and OpenCV. The goal is to monitor a user's facial expressions to detect signs of drowsiness and yawning, providing voice alerts to help prevent accidents due to fatigue.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)

## Features

- Real-time detection of drowsiness and yawning
- Voice alerts when drowsiness or yawning is detected
- Lightweight and efficient using Dlib’s facial landmark detection
- Compatible with both webcam and video files

## Requirements

- Python 3.7+
- OpenCV
- Dlib
- NumPy
- gTTS (Google Text-to-Speech)
- playsound

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/Drowsiness-Yawn-Detection.git
   cd Drowsiness-Yawn-Detection
   ```

2. Create a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Ensure you have Dlib installed correctly. You might need to install it from source if you encounter issues.

## Usage

To run the drowsiness and yawn detection on your webcam:

```bash
python detect.py --source webcam
```

To run the detection on a video file:

```bash
python detect.py --source path/to/video.mp4
```

### Command-Line Arguments

- `--source`: Choose between `webcam` or provide a path to a video file.
- `--alert`: (Optional) Enable/disable voice alerts (`true` or `false`).

## How It Works

1. **Face Detection**: The system uses Dlib’s pre-trained face detector to identify faces in the video stream.
2. **Facial Landmark Detection**: It extracts key facial landmarks to monitor eye openness and mouth movement.
3. **Drowsiness Detection**: Based on eye aspect ratio (EAR), the system determines if the user is drowsy.
4. **Yawn Detection**: The system identifies yawning based on mouth aspect ratio (MAR).
5. **Voice Alerts**: When drowsiness or yawning is detected, a voice alert is generated using gTTS.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your improvements or bug fixes. Ensure your code follows the style guide and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Feel free to customize this README to better suit your project's specifics!

```
Python3 drowsiness_yawn.py -- webcam 0		//For external webcam, use the webcam number accordingly
```

## Setups

Change the threshold values according to your need
```
EYE_AR_THRESH = 0.3
EYE_AR_CONSEC_FRAMES = 30
YAWN_THRESH = 10`	//change this according to the distance from the camera
```

## Acknowledgments

* https://www.pyimagesearch.com/



