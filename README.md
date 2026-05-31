# 🎤 Audio Processing & Transcription Tool

A powerful Python-based audio processing tool that automatically removes silence from audio files and transcribes speech to text with high accuracy.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.7+-green.svg)](https://python.org)

## 🌟 Features

- **Intelligent Silence Removal**: Automatically detects and removes silence segments from audio files
- **Multi-format Support**: Works with WAV, MP3, M4A, OGG, and FLAC audio formats
- **Speech-to-Text Transcription**: Uses Google Speech Recognition for accurate transcription
- **Database Integration**: SQLite database stores processing metadata and transcriptions
- **Duration Tracking**: Monitors original vs. processed audio durations
- **Configurable Parameters**: Customizable silence detection thresholds
- **Robust Error Handling**: Comprehensive error management and validation

##  Quick Start

### Prerequisites

- Python 3.7 or higher
- Internet connection (for Google Speech Recognition)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Amin-moniry/Audio-Processing-Transcription.git
   cd Audio-Processing-Transcription
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   python CONVERT_AUDIO_TO_TEXT_AND_REMOVE_SILENCE.py
   ```

## 📋 Usage

When you run the main script, you'll be prompted to provide:

1. **Audio file path**: Path to your input audio file
2. **Output file path**: Where to save the transcription (e.g., `output.txt`)
3. **Language code**: Language for transcription (e.g., `en-US`, `de-DE`, `fr-FR`)
4. **Silence parameters**:
   - Minimum silence length (milliseconds, e.g., `1000`)
   - Silence threshold (dB, e.g., `-40.0`)

### Example Usage
```bash
Enter the path to an audio file: ./audio/interview.mp3
Enter the path to save the transcription: ./transcriptions/interview.txt
Enter the language code: en-US
Minimum silence length in milliseconds: 1000
Silence threshold in dB: -40.0
```

## 📁 Project Structure

```
📁 Audio-Processing-Transcription/
├── 📜 CONVERT_AUDIO_TO_TEXT_AND_REMOVE_SILENCE.py  # Main entry point
├── 📜 Database_And_prepare_audio.py                # Database operations & audio preparation
├── 📜 Remove_silence_and_mesuere.py               # Silence removal & duration measurement
├── 📜 Speech_and_transcribe.py                    # Speech-to-text processing
├── 📜 requirements.txt                            # Project dependencies
├── 📜 LICENSE                                     # Apache 2.0 License
├── 📜 .gitignore                                  # Git ignore rules
└── 📜 README.md                                   # This file
```

## 🗄️ Database Schema

The application creates an SQLite database (`PODCAST.db`) with the following structure:

| Column              | Type      | Description                           |
|---------------------|-----------|---------------------------------------|
| id                  | INTEGER   | Primary key (auto-increment)          |
| input_path          | TEXT      | Original audio file path              |
| output_path         | TEXT      | Transcription output file path        |
| language            | TEXT      | Language code used for transcription  |
| original_duration   | REAL      | Duration of original audio (seconds)  |
| processed_duration  | REAL      | Duration after silence removal        |
| transcription       | TEXT      | Full transcription text               |
| created_at          | TIMESTAMP | Processing timestamp                  |

## 🔧 Configuration

### Supported Audio Formats
- **WAV** (recommended for best quality)
- **MP3** (most common format)
- **M4A** (Apple format)
- **OGG** (open-source format)
- **FLAC** (lossless compression)

### Language Codes
Common language codes for transcription:
- `en-US` - English (US)
- `en-GB` - English (UK)
- `de-DE` - German
- `fr-FR` - French
- `es-ES` - Spanish
- `it-IT` - Italian
- `ja-JP` - Japanese
- `ko-KR` - Korean

### Silence Detection Parameters
- **Minimum Silence Length**: Minimum duration (in ms) to consider as silence
  - Typical range: 500-2000ms
  - Lower values = more aggressive silence removal
- **Silence Threshold**: Volume level (in dB) below which audio is considered silence
  - Typical range: -30 to -50 dB
  - Lower values = more sensitive silence detection

## 📊 Output Files

The tool generates several files during processing:

1. **Processed Audio**: `[original_name]_no_silence.wav` - Audio with silence removed
2. **Transcription File**: User-specified text file containing the full transcription
3. **Database Record**: Entry in `PODCAST.db` with all processing metadata

## 🛠️ Dependencies

```
pydub>=0.25.1
SpeechRecognition>=3.8.1
```

Additional system requirements:
- **FFmpeg** (for audio format conversion)
- **Internet connection** (for Google Speech Recognition API)

## 📈 Performance Tips

- **Use WAV format** for fastest processing (no conversion needed)
- **Optimize silence parameters** based on your audio content:
  - Podcasts/interviews: 1000ms silence, -40dB threshold
  - Music: 500ms silence, -50dB threshold
  - Noisy environments: 2000ms silence, -30dB threshold

## 🔍 Troubleshooting

### Common Issues

**"Error: File not found"**
- Verify the audio file path is correct
- Ensure the file exists and is readable

**"Invalid input" for silence parameters**
- Ensure minimum silence length is a positive integer
- Ensure silence threshold is a negative number

**Transcription errors**
- Check your internet connection
- Verify the language code is correct
- Ensure the audio quality is sufficient for recognition

**Audio format not supported**
- Install FFmpeg for additional format support
- Convert audio to WAV format manually if needed

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Amin Moniry**
- GitHub: [@Amin-moniry](https://github.com/Amin-moniry)

## 🙏 Acknowledgments

- Google Speech Recognition API for transcription services
- PyDub library for audio processing
- SQLite for lightweight database functionality

---

⭐ **If you found this project helpful, please consider giving it a star!** ⭐
