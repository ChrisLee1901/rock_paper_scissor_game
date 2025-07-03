# Rock Paper Scissors Hand Gesture Game

A real-time Rock Paper Scissors game using computer vision and hand gesture recognition. Play against the AI using your webcam and hand gestures!

## 🎮 Features

- **Real-time Hand Detection**: Uses OpenCV and CVZone for accurate hand tracking
- **Gesture Recognition**: Recognizes Rock (fist), Paper (open hand), and Scissors (peace sign) gestures
- **AI Opponent**: Computer randomly selects moves to compete against
- **Score Tracking**: Keeps track of wins for both player and AI
- **Interactive UI**: Visual feedback with countdown timer and game results
- **Webcam Integration**: Live video feed for gesture detection

## 🎯 Game Rules

- **Rock** (Fist): Beats Scissors, loses to Paper
- **Paper** (Open hand): Beats Rock, loses to Scissors  
- **Scissors** (Peace sign): Beats Paper, loses to Rock

## 🛠️ Technologies Used

- **Python 3.x**
- **OpenCV** - Computer vision and image processing
- **CVZone** - Hand tracking and detection
- **NumPy** - Array operations (dependency of OpenCV)

## 📋 Prerequisites

- Python 3.7 or higher
- Webcam/Camera
- Windows/macOS/Linux

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ChrisLee191/rock-paper-scissors-game.git
   cd rock-paper-scissors-game
   ```

2. **Install required packages**
   ```bash
   pip install opencv-python
   pip install cvzone
   ```

3. **Ensure you have the Resources folder with required images:**
   - `BG.png` - Background image
   - `1.png` - Rock gesture image
   - `2.png` - Paper gesture image  
   - `3.png` - Scissors gesture image

## 🎮 How to Play

1. **Run the game:**
   ```bash
   python main.py
   ```

2. **Start the game:**
   - Press `'s'` key to start a new round
   - Position your hand in front of the camera
   - Wait for the 3-second countdown

3. **Make your gesture:**
   - **Rock**: Close your fist (all fingers down)
   - **Paper**: Open your hand (all fingers up)
   - **Scissors**: Show peace sign (index and middle finger up)

4. **View results:**
   - The AI's choice will be displayed
   - Scores are updated automatically
   - Press `'s'` again for another round

## 📁 Project Structure

```
rock-paper-scissors-game/
│
├── main.py                 # Main game logic
├── README.md              # Project documentation
└── Resources/             # Game assets
    ├── BG.png            # Background image
    ├── 1.png             # Rock gesture image
    ├── 2.png             # Paper gesture image
    └── 3.png             # Scissors gesture image
```

## 🎯 Key Components

### Hand Detection
- Uses CVZone's HandDetector for real-time hand tracking
- Processes finger positions to determine gestures
- Supports single-hand detection for optimal performance

### Game Logic
- Implements classic Rock Paper Scissors rules
- Random AI move generation
- Score tracking and winner determination

### Visual Interface
- Live webcam feed display
- Countdown timer for move preparation
- Score display for both player and AI
- Visual overlay of AI's choice

## 🔧 Configuration

You can modify these parameters in `main.py`:

- **Camera resolution**: Change `cap.set(3, 640)` and `cap.set(4, 480)` values
- **Timer duration**: Modify the condition `if timer > 3:` to change countdown time
- **Hand detection sensitivity**: Adjust HandDetector parameters

## 🐛 Troubleshooting

### Common Issues:

1. **Camera not working:**
   - Ensure your webcam is connected and not being used by other applications
   - Try changing the camera index: `cv2.VideoCapture(1)` instead of `cv2.VideoCapture(0)`

2. **Hand detection not accurate:**
   - Ensure good lighting conditions
   - Keep your hand clearly visible in the camera frame
   - Avoid background clutter

3. **Missing Resources error:**
   - Verify all image files are present in the Resources folder
   - Check file names match exactly (case-sensitive)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Future Enhancements

- [ ] Add multiplayer support
- [ ] Implement different difficulty levels
- [ ] Add sound effects and music
- [ ] Create a web-based version
- [ ] Add gesture training mode
- [ ] Implement best-of-X rounds gameplay
- [ ] Add replay functionality

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [CVZone](https://github.com/cvzone/cvzone) for the excellent hand tracking module
- [OpenCV](https://opencv.org/) for computer vision capabilities
- Rock Paper Scissors game concept and rules

⭐ **If you found this project helpful, please give it a star!** ⭐
