# VidSnapAI – AI-Powered Reel Generator 🎬

**VidSnapAI** is a Python-based web application that automates the creation of short videos and reels from images and text descriptions. It integrates Flask, ElevenLabs Text-to-Speech API, and FFmpeg to convert text into audio and combine it with images to generate vertical MP4 videos.

## ✨ Key Features

- **Image Upload:** Upload images in PNG, JPG, and JPEG formats.
- **Text-to-Speech:** Convert text descriptions into audio using ElevenLabs AI.
- **Automated Video Generation:** Combine uploaded images and generated audio into video reels.
- **FFmpeg Integration:** Automate video processing and rendering.
- **Background Processing:** Automatically detect and process newly uploaded content.
- **Unique File Management:** Organize uploaded files using UUID-based folders.
- **Video Gallery:** View generated reels through a web-based gallery.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Backend development |
| Flask | Web framework |
| HTML5 | Frontend structure |
| CSS3 | User interface styling |
| ElevenLabs API | AI text-to-speech |
| FFmpeg | Audio and video processing |
| Werkzeug | Secure filename handling |
| UUID | Unique file identification |

## 📁 Project Structure

```text
VidSnapAI/
│
├── .vscode/
├── reel/
├── sample_images/
│
├── static/
│   ├── css/
│   ├── reel/
│   ├── reels/
│   ├── songs/
│   └── images/
│
├── templates/
│   ├── base.html
│   ├── create.html
│   ├── gallery.html
│   └── index.html
│
├── user_uploads/
│
├── .gitignore
├── config.py
├── done.txt
├── generate_process.py
├── main.py
├── text_to_audio.py
└── README.md
```

## ⚙️ Installation and Setup

### Prerequisites

Make sure you have installed:

- Python 3.10 or later
- FFmpeg
- Git
- ElevenLabs API key

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Navigate to the Project Directory

```bash
cd VidSnapAI
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 4. Install Dependencies

```bash
pip install flask werkzeug elevenlabs
```

Install any additional packages required by your project modules.

### 5. Configure the ElevenLabs API Key

Create a local `config.py` file in the project root:

```python
ELEVENLABS_API_KEY = "your_elevenlabs_api_key"
```

**Security Note:** Keep `config.py` excluded from Git using `.gitignore`. Never expose your API key in a public repository.

### 6. Configure FFmpeg

Install FFmpeg and add its executable directory to your system PATH.

Verify installation:

```bash
ffmpeg -version
```

### 7. Run the Flask Application

Open a terminal and execute:

```bash
python main.py
```

### 8. Start the Background Video Processor

Open a second terminal in the project directory and execute:

```bash
python generate_process.py
```

### 9. Access the Application

Open your browser and visit:

```text
http://127.0.0.1:5000/
```

## 🔄 Application Workflow

1. Open the VidSnapAI web application.
2. Navigate to the video creation page.
3. Upload images and enter a text description.
4. Flask stores the uploaded content in a uniquely identified folder.
5. The background processor detects new uploads.
6. ElevenLabs converts the text description into an MP3 audio file.
7. FFmpeg combines the uploaded images with the generated audio.
8. The final video is exported in vertical MP4 format.
9. Generated reels can be accessed through the gallery.

## 🎥 Video Processing Specifications

| Specification | Details |
|---|---|
| Resolution | 1080 × 1920 |
| Orientation | Portrait |
| Frame Rate | 30 FPS |
| Video Codec | H.264 |
| Audio Codec | AAC |
| Audio Sample Rate | 44.1 kHz |
| Output Format | MP4 |

## 🤖 AI Integration

VidSnapAI uses the **ElevenLabs Text-to-Speech API** to transform user-provided text descriptions into audio.

Implementation includes:

- ElevenLabs Turbo v2.5 model.
- AI-based speech generation.
- Custom voice settings.
- MP3 audio output.
- Automated audio file storage.

## 📚 Core Concepts Implemented

- Python programming
- Flask web development
- File handling and uploads
- API integration
- UUID generation
- Directory management
- Text-to-speech conversion
- Subprocess execution
- Automated background processing
- Audio and video processing

## 🚀 Future Improvements

- AI-generated video scenes.
- Customizable video templates.
- Background music and sound effects.
- Additional transitions and visual effects.
- Video preview before downloading.
- Social media sharing integration.

## 👩‍💻 Author

**Tania Ray**
