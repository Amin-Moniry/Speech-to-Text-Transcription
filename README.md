<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&height=220&color=0:1a1400,50:5c4a00,100:1a1400&text=SPEECH-TO-TEXT&fontColor=F5C518&fontSize=52&fontAlign=50&fontAlignY=55&animation=fadeIn&stroke=F5C518&strokeWidth=1&desc=Silence%20Removal%20%7C%20Multi-Format%20%7C%20SQLite%20Logging&descAlign=50&descAlignY=75&descSize=15&descColor=f7d966" width="100%"/>

<br/>

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&weight=700&size=20&duration=4000&pause=800&color=F5C518&center=true&vCenter=true&width=700&height=45&lines=%E2%96%B6+ENGINE+BOOT+%E2%80%94+TRANSCRIPTION+READY;%E2%97%8F+DETECT+%C2%B7+STRIP+%C2%B7+TRANSCRIBE+%C2%B7+LOG;%E2%96%B6+MULTI-FORMAT+%7C+GOOGLE+SPEECH+API;%E2%97%8F+WAV+%C2%B7+MP3+%C2%B7+M4A+%C2%B7+OGG+%C2%B7+FLAC"/>

<br/>

<a href="LICENSE"><img src="https://img.shields.io/badge/%E2%96%A3%20LICENSE-Apache%202.0-F5C518?style=for-the-badge&labelColor=1a1400"/></a>
<a href="https://python.org"><img src="https://img.shields.io/badge/%E2%97%88%20PYTHON-3.7+-F5C518?style=for-the-badge&logo=python&logoColor=F5C518&labelColor=1a1400"/></a>
<a href="https://github.com/Amin-Moniry/Speech-to-Text-Transcription"><img src="https://img.shields.io/badge/%E2%96%B6%20FORMAT-WAV%20%2F%20MP3%20%2F%20M4A-F5C518?style=for-the-badge&labelColor=1a1400"/></a>
<a href="https://github.com/Amin-Moniry/Speech-to-Text-Transcription"><img src="https://img.shields.io/badge/%E2%97%8F%20SPEECH-Google%20API-F5C518?style=for-the-badge&logo=google&logoColor=F5C518&labelColor=1a1400"/></a>
<a href="https://github.com/Amin-Moniry/Speech-to-Text-Transcription/stargazers"><img src="https://img.shields.io/github/stars/Amin-Moniry/Speech-to-Text-Transcription?style=for-the-badge&color=F5C518&labelColor=1a1400&label=%E2%98%85%20STARS"/></a>

<br/><br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

</div>

---

<div align="center">

## `◈` Overview

</div>

<div align="center">

**Speech-to-Text Transcription** is a modular Python tool for automated audio cleanup and accurate transcription. It detects and strips silence segments from any supported audio file, then routes the cleaned audio through **Google Speech Recognition** to produce a full text transcription — logging every run, duration delta, language, and output path to a local **SQLite** database for full traceability.

Built for podcasters, researchers, and developers who need a lightweight, configurable, offline-first processing layer. All parameters — silence thresholds, minimum duration, output language, and file paths — are entered at runtime with no code changes required.

</div>

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

<div align="center">

## `◈` Features

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=13&duration=3000&pause=999999&color=F5C518&center=true&vCenter=true&width=500&height=28&lines=%E2%97%89+Core+capabilities+of+the+engine"/>

<small>

| <sub>`▶` Feature</sub> | <sub>Description</sub> | <sub>Status</sub> |
|:-----------------------:|:----------------------:|:-----------------:|
| <sub>Silence Detection</sub> | <sub>Configurable dB threshold and minimum duration (ms) — per-run at runtime</sub> | <sub>✅</sub> |
| <sub>Multi-Format Support</sub> | <sub>WAV, MP3, M4A, OGG, FLAC — FFmpeg handles conversion automatically</sub> | <sub>✅</sub> |
| <sub>Speech-to-Text</sub> | <sub>Google Speech Recognition — 10+ language codes supported</sub> | <sub>✅</sub> |
| <sub>SQLite Logging</sub> | <sub>Every run logged with paths, durations, language, transcription, and timestamp</sub> | <sub>✅</sub> |
| <sub>Duration Tracking</sub> | <sub>Original vs. processed duration delta recorded and stored per run</sub> | <sub>✅</sub> |
| <sub>Runtime Configuration</sub> | <sub>All detection settings entered interactively — no config file or code edits needed</sub> | <sub>✅</sub> |
| <sub>Error Handling</sub> | <sub>Validated inputs, format checks, and descriptive error messages on failure</sub> | <sub>✅</sub> |
| <sub>Batch Processing</sub> | <sub>Run the engine across an entire folder of audio files in one pass</sub> | <sub>⏳</sub> |
| <sub>Offline Transcription</sub> | <sub>Whisper backend — no internet required</sub> | <sub>⏳</sub> |
| <sub>Subtitle Export</sub> | <sub>SRT / VTT output alongside plain text transcription</sub> | <sub>⏳</sub> |

</small>

</div>

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

<div align="center">

## `◈` Tech Stack

| Layer | Technologies |
|:-----:|:------------:|
| **Audio Processing** | PyDub — silence detection, segmentation, and WAV export |
| **Speech Recognition** | SpeechRecognition — Google Speech API wrapper |
| **Format Conversion** | FFmpeg — MP3, M4A, OGG, FLAC → WAV |
| **Database** | SQLite3 — local metadata and transcription storage |
| **Language** | Python 3.7+ |

</div>

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

## `◈` Project Structure

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=13&duration=3000&pause=999999&color=F5C518&center=false&vCenter=true&width=540&height=28&lines=%E2%96%B6+Repository+layout+%E2%80%94+Speech-to-Text+Transcription"/>

```
Speech-to-Text-Transcription/
│
├── CONVERT_AUDIO_TO_TEXT_AND_REMOVE_SILENCE.py   ← Main entry point
├── Database_And_prepare_audio.py                  ← DB operations & audio preparation
├── Remove_silence_and_mesuere.py                  ← Silence removal & duration tracking
├── Speech_and_transcribe.py                       ← Google Speech API transcription
│
├── requirements.txt                               ← Python dependencies
├── LICENSE                                        ← Apache 2.0
├── .gitignore
└── README.md
```

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

## `◈` Installation

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=13&duration=3000&pause=999999&color=F5C518&center=false&vCenter=true&width=500&height=28&lines=%E2%96%B6+Setup+in+three+steps"/>

![01](https://img.shields.io/badge/01-Clone_Repository-F5C518?style=flat-square&labelColor=1a1400) &nbsp; Clone the project to your local machine.

```bash
git clone https://github.com/Amin-Moniry/Speech-to-Text-Transcription.git
cd Speech-to-Text-Transcription
```

![02](https://img.shields.io/badge/02-Install_Dependencies-F5C518?style=flat-square&labelColor=1a1400) &nbsp; Install Python packages and FFmpeg.

```bash
pip install -r requirements.txt
```

```bash
# FFmpeg is required for non-WAV format conversion
# Ubuntu / Debian:  sudo apt install ffmpeg
# macOS:            brew install ffmpeg
# Windows:          https://ffmpeg.org/download.html
```

![03](https://img.shields.io/badge/03-Run_Engine-F5C518?style=flat-square&labelColor=1a1400) &nbsp; Launch the main script and follow the prompts.

```bash
python CONVERT_AUDIO_TO_TEXT_AND_REMOVE_SILENCE.py
```

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

## `◈` Usage

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=13&duration=3000&pause=999999&color=F5C518&center=false&vCenter=true&width=520&height=28&lines=%E2%96%B6+Runtime+prompts+and+parameter+guide"/>

The engine prompts for five inputs at runtime:

```bash
Enter the path to an audio file:          ./audio/interview.mp3
Enter the path to save the transcription: ./transcriptions/interview.txt
Enter the language code:                  en-US
Minimum silence length in milliseconds:   1000
Silence threshold in dB:                  -40.0
```

### `◈` Silence Detection Parameters

**Minimum Silence Length** — duration in milliseconds that must be silent before a segment is cut.
Range: `500`–`2000` ms. Lower = more aggressive removal.

**Silence Threshold** — volume level in dB below which audio is treated as silence.
Range: `-30` to `-50` dB. Lower = more sensitive detection.

Recommended settings by content type:

| Use Case | Min Silence | Threshold |
|:--------:|:-----------:|:---------:|
| Podcast / Interview | 1000 ms | -40 dB |
| Music | 500 ms | -50 dB |
| Noisy Environment | 2000 ms | -30 dB |

### `◈` Supported Language Codes

`en-US` · `en-GB` · `de-DE` · `fr-FR` · `es-ES` · `it-IT` · `ja-JP` · `ko-KR` and any code supported by the Google Speech Recognition API.

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

<div align="center">

## `◈` Database Schema

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=13&duration=3000&pause=999999&color=F5C518&center=true&vCenter=true&width=520&height=28&lines=%E2%97%89+PODCAST.db+%E2%80%94+SQLite+table+structure"/>

<small>

| <sub>Column</sub> | <sub>Type</sub> | <sub>Description</sub> |
|:-----------------:|:---------------:|:----------------------:|
| <sub>`id`</sub> | <sub>INTEGER</sub> | <sub>Primary key — auto-increment</sub> |
| <sub>`input_path`</sub> | <sub>TEXT</sub> | <sub>Original audio file path</sub> |
| <sub>`output_path`</sub> | <sub>TEXT</sub> | <sub>Transcription output file path</sub> |
| <sub>`language`</sub> | <sub>TEXT</sub> | <sub>Language code used for transcription</sub> |
| <sub>`original_duration`</sub> | <sub>REAL</sub> | <sub>Duration of original audio (seconds)</sub> |
| <sub>`processed_duration`</sub> | <sub>REAL</sub> | <sub>Duration after silence removal (seconds)</sub> |
| <sub>`transcription`</sub> | <sub>TEXT</sub> | <sub>Full transcription output text</sub> |
| <sub>`created_at`</sub> | <sub>TIMESTAMP</sub> | <sub>Processing timestamp</sub> |

</small>

</div>

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

## `◈` Output Files

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=13&duration=3000&pause=999999&color=F5C518&center=false&vCenter=true&width=520&height=28&lines=%E2%96%B6+Three+artifacts+generated+per+run"/>

**Processed Audio** — `[original_name]_no_silence.wav` — the cleaned audio with all silence removed, exported as WAV regardless of input format.

**Transcription File** — user-specified path — plain text file containing the full Google Speech output of the processed audio.

**Database Record** — new row in `PODCAST.db` — stores all paths, durations, language code, full transcription, and processing timestamp.

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

## `◈` Troubleshooting

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=13&duration=3000&pause=999999&color=F5C518&center=false&vCenter=true&width=500&height=28&lines=%E2%96%B6+Common+issues+and+fixes"/>

**File not found** — Verify the audio file path is correct and the file is readable by the current user.

**Invalid silence parameters** — Minimum silence length must be a positive integer (ms). Silence threshold must be a negative number (dB).

**Transcription errors** — Check your internet connection. Google Speech Recognition requires an active connection. Verify the language code matches the spoken language and that audio quality is sufficient.

**Unsupported audio format** — Install FFmpeg for automatic conversion. Alternatively, convert to WAV manually before running the engine.

```bash
# Ubuntu / Debian
sudo apt install ffmpeg

# macOS
brew install ffmpeg
```

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

## `◈` Roadmap

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=13&duration=3000&pause=999999&color=F5C518&center=false&vCenter=true&width=480&height=28&lines=%E2%96%B6+Planned+improvements"/>

- [ ] Batch mode — process an entire folder of audio files in a single run
- [ ] Whisper backend — fully offline transcription with no internet dependency
- [ ] SRT / VTT subtitle export alongside plain text output
- [ ] Speaker diarization — label transcript segments by detected speaker
- [ ] GUI control panel for parameter input and run history browsing

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

## `◈` Contributing

1. Fork the repository via the **Fork** button on GitHub.
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit with a descriptive message: `git commit -m "Add: brief description"`
4. Push to your fork: `git push origin feature/your-feature-name`
5. Open a **Pull Request** against the `master` branch of this repository.

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

<div align="center">

## `◈` License

This project is licensed under the **Apache License 2.0**.

Free to use, modify, and distribute with attribution to **Amin Moniry** as the original author. See [LICENSE](LICENSE) for complete terms.

`©` 2025 Amin Moniry (AminTivanix2) — All Rights Reserved

</div>

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

---

<div align="center">

## `◈` Contact

<br/>

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=14&duration=2000&pause=400&color=F5C518&center=true&vCenter=true&width=500&height=30&lines=%E2%96%B6+Reach+out+through+any+channel+below"/>

<br/>

<table>
<tr>
<td align="center" width="210">
<a href="https://github.com/Amin-Moniry">
<img src="https://img.shields.io/badge/◈_GITHUB-Amin--Moniry-F5C518?style=for-the-badge&logo=github&logoColor=F5C518&labelColor=1a1400&color=2b2000" width="200"/>
</a>
</td>
<td align="center" width="210">
<a href="https://t.me/amintivanix2">
<img src="https://img.shields.io/badge/◈_TELEGRAM-@amintivanix2-F5C518?style=for-the-badge&logo=telegram&logoColor=F5C518&labelColor=1a1400&color=2b2000" width="200"/>
</a>
</td>
<td align="center" width="210">
<a href="mailto:amintivanix2@gmail.com">
<img src="https://img.shields.io/badge/◈_EMAIL-amintivanix2-F5C518?style=for-the-badge&logo=gmail&logoColor=F5C518&labelColor=1a1400&color=2b2000" width="200"/>
</a>
</td>
</tr>
<tr>
<td align="center" width="210">
<a href="https://allin1wrench.ir">
<img src="https://img.shields.io/badge/◈_WEBSITE-allin1wrench.ir-F5C518?style=for-the-badge&logo=firefox&logoColor=F5C518&labelColor=1a1400&color=2b2000" width="200"/>
</a>
</td>
<td align="center" width="210" colspan="2">
<a href="https://github.com/Amin-Moniry/Speech-to-Text-Transcription/issues">
<img src="https://img.shields.io/badge/◈_ISSUES-Report_a_Bug-F5C518?style=for-the-badge&logo=githubactions&logoColor=F5C518&labelColor=1a1400&color=2b2000" width="200"/>
</a>
</td>
</tr>
</table>

</div>

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<div align="center">

<br/>

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&weight=700&size=15&duration=3500&pause=900&color=F5C518&center=true&vCenter=true&width=720&height=50&lines=%E2%96%B6+Engineered+by+Amin+Moniry+(AminTivanix2);%E2%97%8F+Every+word+matters.+No+silence+survives.;%E2%96%B6+PyDub+%C2%B7+Google+Speech+%C2%B7+SQLite+%C2%B7+Apache+2.0+%C2%B7+2025"/>

<br/>

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:1a1400,50:5c4a00,100:1a1400&height=160&section=footer&text=Built%20with%20precision%20%E2%80%94%20AminTivanix2&fontSize=26&fontAlign=50&fontAlignY=55&fontColor=F5C518&animation=fadeIn&stroke=F5C518&strokeWidth=0.5" width="100%"/>

</div>
