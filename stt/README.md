# Speech-to-Text Setup

## What I've Installed

- **OpenAI Whisper** - State-of-the-art speech recognition

## Setup

### 1. Install Whisper (already done)

```bash
pip3 install openai-whisper
```

### 2. Create audio recording script

```bash
bash /root/.openclaw/workspace/record_audio.sh
```

### 3. Transcribe audio

```bash
python3 /root/.openclaw/workspace/stt.py recording.wav
```

## Manual Recording

### Using arecord (Linux terminal):
```bash
arecord -d 10 -f S16_LE -r 16000 recording.wav
```

### Using ffmpeg:
```bash
ffmpeg -f lavfi -i "anullsrc=r=16000:cl=mono" -t 10 -c:a pcm_s16le recording.wav
```

## Usage Example

```bash
# Record 15 seconds of audio
bash /root/.openclaw/workspace/record_audio.sh 15

# Or record manually then transcribe
arecord -d 10 -f S16_LE -r 16000 my_audio.wav
python3 /root/.openclaw/workspace/stt.py my_audio.wav
```

## Features

- **Model**: Whisper base (fast, good accuracy)
- **Format**: WAV 16kHz mono
- **Output**: Text transcript

## Requirements

- Python 3.x
- ffmpeg or arecord (for recording)

## Notes

- Whisper will download the base model (~140MB) on first run
- Subsequent runs use cached model
- Model: `base` (fast, good for general use)
- Can change to `small`, `medium`, `large` for better accuracy
