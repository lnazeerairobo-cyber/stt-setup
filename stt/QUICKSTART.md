# 🎤 Speech-to-Text Quick Start

## ✅ Done
- OpenAI Whisper installed
- Recording script ready
- GitHub repo created

## 🚀 Quick Start

```bash
# Record and transcribe audio (10 seconds by default)
bash /root/.openclaw/workspace/record_audio.sh

# Record for 30 seconds
bash /root/.openclaw/workspace/record_audio.sh 30

# Or transcribe existing file
python3 /root/.openclaw/workspace/stt.py your_audio.wav
```

## 📊 Results
Whisper transcribes your voice into text instantly!

## 🔗 GitHub
https://github.com/lnazeerairobo-cyber/stt-setup

---

**Note**: On first use, Whisper will download the model (~140MB). Subsequent runs will be faster.
