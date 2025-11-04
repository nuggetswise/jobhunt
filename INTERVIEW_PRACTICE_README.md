# 🎯 Interview Practice Assistant

A simple, free interview practice tool using only Claude API and browser features!

## What It Does

- **AI Interviewer**: Claude asks you interview questions
- **Real-time Speech Recognition**: Your answers are transcribed automatically (FREE!)
- **Live Metrics**: Tracks words per minute, filler words, duration
- **Instant Feedback**: Claude analyzes your answers and gives improvement tips
- **Video Preview**: See yourself while practicing

## How to Use

### Step 1: Get Your Claude API Key

1. Go to https://console.anthropic.com/
2. Sign in with your Claude account
3. Go to "API Keys" section
4. Create a new API key (or use existing)
5. Copy the key (starts with `sk-ant-...`)

### Step 2: Run the App

**Option A - Double Click (Easiest)**
```bash
# Just double-click the file:
interview-practice.html
```

**Option B - Use a Local Server (Recommended)**
```bash
# If you have Python installed:
python3 -m http.server 8000

# Then open: http://localhost:8000/interview-practice.html
```

### Step 3: Start Practicing

1. **Paste your Claude API key** in the settings
2. **Choose interview type**: Behavioral, Technical, Case Study, etc.
3. **Enter your role**: e.g., "Senior Software Engineer"
4. **Select company style**: FAANG, Startup, Corporate, etc.
5. **Click "Start Interview"** - Claude will ask a question
6. **Click "Start Answering"** - Speak your answer
7. **Click "Stop Answering"** - Get instant feedback!

## Features

### Real-Time Metrics
- **Words Per Minute**: Optimal is 140-160 WPM
- **Filler Words**: Tracks "um", "uh", "like", etc.
- **Duration**: See how long you've been speaking

### Smart Analysis
- Claude evaluates your answer quality
- Provides specific improvement suggestions
- Rates your response out of 10
- Asks relevant follow-up questions

### No Cost (Except Claude API)
- Uses browser's built-in speech recognition (FREE)
- Uses your webcam/mic (FREE)
- Only cost is Claude API calls (~$0.01 per question)

## Browser Requirements

**Best Experience:**
- ✅ Google Chrome
- ✅ Microsoft Edge
- ✅ Safari (Mac)

**Not Supported:**
- ❌ Firefox (no Web Speech API)

## Privacy

- Everything runs in YOUR browser
- No data is stored anywhere
- Only your answers are sent to Claude API
- Video never leaves your computer

## Tips for Best Results

1. **Speak Clearly**: The speech recognition works best with clear pronunciation
2. **Good Lighting**: Help yourself see your body language
3. **Quiet Environment**: Reduces transcription errors
4. **Practice Regularly**: Do 2-3 questions per day
5. **Review Feedback**: Claude's suggestions are valuable!

## Troubleshooting

### "Please allow camera and microphone access"
- Click "Allow" when the browser asks for permissions
- Check browser settings if you accidentally denied access

### "Speech recognition not supported"
- Use Chrome or Edge browser
- Speech recognition doesn't work in Firefox

### "API error: 401"
- Your API key is invalid or expired
- Get a new key from https://console.anthropic.com/

### "API error: 429"
- You've hit rate limits
- Wait a few minutes and try again
- Consider upgrading your Claude API plan

### Speech Recognition Not Working
- Make sure you're using HTTPS or localhost
- Check microphone permissions in browser settings
- Try refreshing the page

## Cost Estimate

**Claude API Usage:**
- ~1,000 tokens per question + answer + feedback
- ~$0.003 per question with Claude 3.5 Sonnet
- **$0.30 for 100 practice questions**

Very affordable for serious interview prep!

## Next Steps / Future Improvements

Want to enhance this tool? Here are ideas:

1. **Save Practice Sessions**: Store history in localStorage
2. **Video Analysis**: Add body language feedback
3. **LinkedIn Integration**: Research your interviewer
4. **Company Database**: Store company-specific questions
5. **Progress Tracking**: Chart improvement over time
6. **Export Reports**: Download practice session summaries

## Technical Details

**Built With:**
- Vanilla JavaScript (no frameworks!)
- Web Speech API (speech-to-text)
- MediaDevices API (webcam/mic)
- Claude 3.5 Sonnet API (AI interviewer)
- Pure CSS (no dependencies)

**Single File**: Everything is in one HTML file - no build process, no npm, no complexity!

## Questions?

This tool was built with Claude Code. Modify the HTML file to customize:
- Interview questions style
- Feedback format
- UI colors/layout
- Metrics tracked

Enjoy your interview practice! 🚀
