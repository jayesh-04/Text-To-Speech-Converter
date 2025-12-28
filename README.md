# 🎙️ Text To Speech Converter
[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/jayesh-04/Text-To-Speech-Converter)

A clean, modern, and responsive web application that converts typed text into speech using the Web Speech API. Users can enter text, select from available system voices, and listen instantly.

## 🚀 Live Demo

You can try the live application here:
**[https://jayesh-04.github.io/Text-To-Speech-Converter/](https://jayesh-04.github.io/Text-To-Speech-Converter/)**

## ✨ Features

*   **Dynamic Voice Selection**: Automatically loads and lists all voices available in your browser or operating system.
*   **Instant Playback**: Converts text to speech in real-time with a single button click.
*   **Modern UI**: A sleek interface with a gradient background and user-friendly controls.
*   **Fully Responsive**: The layout adapts seamlessly to desktop, tablet, and mobile screens.
*   **Zero Dependencies**: Built with vanilla HTML, CSS, and JavaScript. No frameworks or libraries needed.
*   **Lightweight & Fast**: Runs entirely in the browser using the native Web Speech API for excellent performance.

## 🔧 How It Works

The application leverages the browser's built-in `SpeechSynthesis` interface to function.

1.  **Initialize Speech Synthesis**: An instance of `SpeechSynthesisUtterance` is created to configure the speech output.
    ```javascript
    let speech = new SpeechSynthesisUtterance();
    ```

2.  **Load Voices**: The `onvoiceschanged` event is used to fetch the list of available voices from the browser. The dropdown menu is populated dynamically with these voices.
    ```javascript
    let voices = [];
    let voiceSelect = document.querySelector("select");

    window.speechSynthesis.onvoiceschanged = () =>{
        voices = window.speechSynthesis.getVoices();
        speech.voice = voices[0]; // Set a default voice
        voices.forEach((voice, i) => (voiceSelect.options[i]) = new Option(voice.name, i));
    };
    ```

3.  **Speak Text**: An event listener on the "Listen" button takes the text from the `textarea`, assigns it to the `speech` object, and calls `window.speechSynthesis.speak()` to start the audio playback.
    ```javascript
    document.querySelector("button").addEventListener("click",()=>{
        speech.text = document.querySelector("textarea").value;
        window.speechSynthesis.speak(speech);
    })
    ```

## 🛠️ Getting Started

To run this project locally, follow these simple steps.

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/jayesh-04/Text-To-Speech-Converter.git
    ```

2.  **Navigate to the project directory:**
    ```sh
    cd Text-To-Speech-Converter
    ```

3.  **Open the application:**
    Open the `docs/index.html` file in your web browser. No C installation or local server is required.

## 💻 Tech Stack

*   **HTML5**: For the structure and content of the application.
*   **CSS3**: For styling, including the gradient background and responsive design.
*   **JavaScript (ES6)**: For application logic and interactivity.
*   **Web Speech API**: For the core text-to-speech functionality.

## 👨‍💻 Author

**Jayesh Jitendra Borase**
*   **GitHub**: [@jayesh-04](https://github.com/jayesh-04)
