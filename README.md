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

1. **Download:** Go to the [Releases page](https://github.com/aritlhq/mentari-ai-p2c-public/releases) and download the
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


## How to Get Mentari Token
1. Open Mentari website and login to your account.
2. Open Inspect Element (Right click > Inspect).
<img width="354" height="378" alt="image" src="https://github.com/user-attachments/assets/7fce356e-5127-4c17-ba60-9eac3ddbb97e" />

4. Copy this code.
```
try {
  console.log(JSON.parse(localStorage.getItem('access'))?.[0]?.token || 'Token not found.');
} catch {
  console.error('Invalid access data.');
}
```
5. Paste into Console.
6. Click Enter.
<img width="911" height="238" alt="image" src="https://github.com/user-attachments/assets/58371d65-1557-4ffe-acc9-aa02dd39802b" />

7. Now, you have obtained your bearer token (`eyJhbGciOiJIUzI1NiIsInR5cCI6Ik...`).
8. Paste it into `config.txt`. Set it as the value of the `MENTARI_TOKEN` variable.

## How to Get Gemini Token
1. Go to https://aistudio.google.com/prompts/new_chat
2. Click `Get API Key`.
<img width="1920" height="1000" alt="image" src="https://github.com/user-attachments/assets/11b3d38e-a0e7-49c2-9aa1-aff09cd1177c" />

3. Click `Create API Key`.
<img width="1909" height="921" alt="image" src="https://github.com/user-attachments/assets/3a00d956-e2cc-4e12-a0d4-715f1575b4e7" />

4. Select a project from your existing Google Cloud projects.
<img width="701" height="368" alt="image" src="https://github.com/user-attachments/assets/7f9d67db-0c41-4937-b895-9f785a981ddb" />

6. Click `Create API Key in existing project`.
7. Your API Key successfuly generated.
<img width="878" height="336" alt="image" src="https://github.com/user-attachments/assets/5841dfec-8a78-4631-92c2-30adaef87656" />

9. Copy and paste into `config.txt`
