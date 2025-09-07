# Mentari AI-P2C (AI Powered Course Completer)

An AI-powered CLI tool to automate coursework on the Mentari academic platform.

<img width="963" height="415" alt="image_2025-09-07_19-16-38" src="https://github.com/user-attachments/assets/e7854ab1-7dfe-45c1-a7ba-c73dcfd2cad6" />

## Features

- **AI-Powered Answers:** Integrates with Google's Gemini AI to provide intelligent, context-aware answers for quizzes.
- **Interactive Course Selection:** A clean interface to select one or more courses to process.
- **Standalone Executable:** Packaged into a single `.exe` file that runs on Windows without needing Node.js installed.
- **External Configuration:** Easily update your authentication tokens by editing a simple `config.txt` file, no
  rebuilding required.
- **Real-Time Logging:** Colorful, easy-to-read logs show the bot's progress and actions as they happen.

## Tech Stack

- **Runtime:** Node.js
- **Language:** JavaScript (ES6 Modules)
- **CLI Interface:** Inquirer, Chalk
- **AI:** Google Gemini API
- **Build Process:** esbuild, pkg, rcedit

## How to Use (For End-Users)

1. **Download:** Go to the [Releases page](https://github.com/aritlhq/mentari-ai-p2c/releases) and download the
   latest `mentari-ai-p2c.zip` file.

2. **Extract:** Unzip the downloaded file into a new folder anywhere on your computer.

3. **Configure:** In the same folder, rename `config-example.txt` to `config.txt`. Open it and paste the following,
   replacing the placeholders with your actual credentials:

   ```ini
   MENTARI_TOKEN=your_long_bearer_token_from_the_mentari_platform
   GEMINI_API_KEY=your_google_gemini_api_key
   ```

4. **Run:** Double-click the `mentari-ai-p2c.exe` file. The application will start in a new terminal window.

This project was created for educational and experimental purposes only. Using automation for academic coursework may
violate your institution's academic integrity policy. The author is not responsible for any misuse of this software.
Please use it responsibly.

## License

This project is licensed under the MIT License.
