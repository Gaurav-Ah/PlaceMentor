# PlaceMentor – Flutter Android App
## Campus Placement Intelligence Platform
### Developed by: Gaurav A. Ahire | TY AI&DS – B(56)
### Guide: D. M. Avhad | K.K. Wagh Institute, Nashik

---

## ✅ WHAT'S INSIDE

| Screen         | Features                                              |
|----------------|-------------------------------------------------------|
| Splash Screen  | Animated logo + loading bar                           |
| Login Screen   | Student / Company role, department picker             |
| Dashboard      | Stats grid, news feed, profile progress, API key hint |
| Jobs           | Search + filter, match %, apply button                |
| Schedule       | Interview cards, confirm / review / cancel status     |
| ATS Checker    | Paste resume + JD → Gemini AI gives score & feedback  |
| Sentiment      | English & Hinglish → Positive / Negative / Neutral    |
| Profile        | Skills, stats, Gemini API key setup, app info         |

---

## 🛠 STEP-BY-STEP SETUP

### STEP 1 — Install Flutter SDK
1. Go to: https://docs.flutter.dev/get-started/install/windows
2. Download Flutter SDK zip → extract to `C:\flutter`
3. Add `C:\flutter\bin` to your system PATH
4. Run in terminal: `flutter doctor`
   - Fix any issues shown (Android SDK, etc.)

### STEP 2 — Install Android Studio
1. Download from: https://developer.android.com/studio
2. Install with default options
3. Open Android Studio → SDK Manager → install:
   - Android SDK Platform 34
   - Android SDK Build-Tools 34
4. Run `flutter doctor` again — all checkmarks should appear

### STEP 3 — Open the Project
1. Open Android Studio
2. Click "Open" → select the `placementor` folder (this folder)
3. Wait for Gradle sync to finish (~2-3 minutes first time)

### STEP 4 — Get Dependencies
Open terminal inside Android Studio (View → Tool Windows → Terminal):
```
flutter pub get
```

### STEP 5 — Connect Your Phone
1. On your Android phone: Settings → About Phone → tap "Build Number" 7 times
2. Go to Settings → Developer Options → enable "USB Debugging"
3. Connect phone via USB cable
4. Accept "Allow USB Debugging" prompt on phone
5. Run in terminal: `flutter devices`  (your phone should appear)

### STEP 6 — Run the App
```
flutter run
```
Or press the green ▶ Run button in Android Studio.

The app will install and launch on your phone automatically!

---

## ⚡ ENABLE AI FEATURES (ATS + Sentiment)

1. Go to: https://aistudio.google.com/app/apikey
2. Sign in with Google → click "Create API Key" → copy it
3. In the app → Profile tab → paste key → tap "Save API Key"
4. Now ATS Checker and Sentiment Analyzer work with real Gemini AI!

---

## 📁 PROJECT STRUCTURE

```
placementor/
├── lib/
│   ├── main.dart                  ← App entry + theme + colors
│   ├── models/
│   │   └── models.dart            ← AppUser, Job, Interview, AtsResult, SentimentResult
│   ├── services/
│   │   └── app_state.dart         ← State management + GeminiApi calls
│   ├── widgets/
│   │   └── widgets.dart           ← Reusable UI components
│   └── screens/
│       ├── splash_screen.dart     ← Animated splash
│       ├── login_screen.dart      ← Auth screen
│       ├── home_screen.dart       ← Bottom navigation shell
│       ├── dashboard_screen.dart  ← Home dashboard
│       ├── jobs_screen.dart       ← Job listings + apply
│       ├── schedule_screen.dart   ← Interview schedule
│       ├── ats_screen.dart        ← ATS Checker (Gemini AI)
│       ├── sentiment_screen.dart  ← Sentiment Analyzer (Gemini AI)
│       └── profile_screen.dart    ← Profile + API key
├── android/                       ← Android platform files
├── pubspec.yaml                   ← Dependencies
└── README.md                      ← This file
```

---

## 📦 DEPENDENCIES USED

| Package             | Purpose                          |
|---------------------|----------------------------------|
| google_fonts        | Syne + DM Sans typography        |
| http                | Gemini API calls                 |
| shared_preferences  | Save API key locally             |
| percent_indicator   | Progress bar widgets             |

---

## 🐛 COMMON ISSUES & FIXES

**"flutter not recognized"**
→ Add `C:\flutter\bin` to PATH and restart terminal

**Gradle sync failed**
→ File → Invalidate Caches → Restart

**App crashes on launch**
→ Run `flutter clean` then `flutter pub get` then `flutter run`

**Gemini API not working**
→ Check internet on phone; verify the API key is correct

**Phone not detected**
→ Install phone's USB driver; try different USB cable/port

---

## 📝 FOR YOUR REPORT

- **GitHub Link (Section 8):** Upload this folder to GitHub and paste the link
- **Tech Stack:** Flutter, Dart, Gemini 2.0 Flash API, SharedPreferences
- **Platform:** Android (minSdk 21 = Android 5.0+)
- **AI Features:** ATS Score Detection + Hinglish/English Sentiment Analysis
