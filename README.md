<h1>🎙️ Text-To-Speech Converter</h1>

A clean, modern, and responsive web application that converts typed text into speech using the Web Speech API.
Users can enter any text, select from available system voices, and listen instantly with a single click.

<h2>🔗 Live Demo</h2>
👉 https://jayesh-04.github.io/Text-To-Speech-Converter/

<h2>🧾 Project Overview</h2>

This Text-to-Speech application provides a simple and intuitive interface that allows users to:

🔊 Convert any text into clear, natural-sounding speech

🎙️ Choose from multiple available system voices

🚀 Enjoy a fully responsive UI with modern styling

⚡ Experience fast performance with zero dependencies

🧩 Works directly in the browser — no backend required

Built using HTML, CSS, and JavaScript with the native Web Speech API.

<h2>🖼️ Features</h2>
✔️ Dynamic Voice Loading

Automatically loads all available voices from the user's device.

✔️ Real-Time Text-to-Speech

Speaks the text instantly using SpeechSynthesisUtterance.

✔️ Modern UI

Designed with gradient backgrounds, rounded controls, and clean typography.

✔️ Responsive Layout

Works smoothly on desktops, tablets, and mobile devices.

✔️ Single Page App

No framework — lightweight, fast, and efficient.

<h2>📂 Project Structure</h2>
├── index.html<br>
├── style.css<br>
├── script.js<br>
└── images/<br>
         ├── dropdown.png<br>
         └── play.png

<h2>⚙️ How It Works</h2>
1. SpeechSynthesis Setup<br>
let speech = new SpeechSynthesisUtterance();<br>
let voices = [];

2. Load Voices Automatically<br>
window.speechSynthesis.onvoiceschanged = () => {<br>
    voices = window.speechSynthesis.getVoices();<br>
    speech.voice = voices[0];<br>
    voices.forEach((voice, i) => (voiceSelect.options[i] = new Option(voice.name, i)));<br>
};

3. Trigger Speech Output<br>
document.querySelector("button").addEventListener("click", () => {<br>
    speech.text = document.querySelector("textarea").value;<br>
    window.speechSynthesis.speak(speech);<br>
});

<h2>⚙️ Setup Instructions</h2>
1. Clone this Repository
git clone https://github.com/yourusername/TextToSpeechConvertor.git

2. Navigate to the Folder
cd TextToSpeechConvertor

3. Run the Project

Open index.html in any modern browser.

No installations or dependencies required.

<h2>📸 Preview</h2>

Add your screenshots here:

![Screenshot](images/your_screenshot.png)

<h2>🧰 Tech Stack</h2>

<ul>
<li>HTML5</li>

<li>CSS3</li>

<li>JavaScript (ES6)</li>

<li>Web Speech API</li>
</ul>

<h2>👨‍💻 Author</h2>

Jayesh (Your Name Here)<br>
Frontend Developer | Java | Web Enthusiast<br>
🔗 GitHub: https://github.com/yourusername
