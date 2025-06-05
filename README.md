# Chatterbox TTS Server 🎤

![Chatterbox TTS Server](https://img.shields.io/badge/Chatterbox%20TTS%20Server-Ready-brightgreen) ![GitHub Repo stars](https://img.shields.io/github/stars/Anshudhattarwal/Chatterbox-TTS-Server) ![GitHub forks](https://img.shields.io/github/forks/Anshudhattarwal/Chatterbox-TTS-Server) ![GitHub issues](https://img.shields.io/github/issues/Anshudhattarwal/Chatterbox-TTS-Server)

Welcome to the **Chatterbox TTS Server**! This repository allows you to self-host the powerful Chatterbox Text-to-Speech (TTS) model. With a user-friendly Web UI and flexible API endpoints, you can easily integrate TTS capabilities into your applications. 

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Predefined Voices](#predefined-voices)
- [Voice Cloning](#voice-cloning)
- [Large Text Processing](#large-text-processing)
- [Execution Options](#execution-options)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Releases](#releases)

## Features

- **User-Friendly Web UI**: Easily manage TTS tasks with an intuitive interface.
- **Flexible API Endpoints**: Compatible with OpenAI standards for seamless integration.
- **Predefined Voices**: Choose from a variety of voices to suit your needs.
- **Voice Cloning**: Create unique voice profiles for personalized TTS.
- **Large Text Processing**: Handle substantial text inputs without issues.
- **Execution on GPU/CPU**: Optimize performance based on your hardware capabilities.

## Installation

To get started, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Anshudhattarwal/Chatterbox-TTS-Server.git
   cd Chatterbox-TTS-Server
   ```

2. **Install Dependencies**:
   Make sure you have Python 3.7 or higher. Then, run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Server**:
   Start the server with:
   ```bash
   python app.py
   ```

4. **Access the Web UI**:
   Open your browser and navigate to `http://localhost:8000`.

## Usage

Once the server is running, you can use the Web UI to interact with the TTS model. You can input text, select a voice, and generate audio files. 

### Example Request
To use the API, send a POST request to the `/synthesize` endpoint with the following JSON body:

```json
{
  "text": "Hello, welcome to Chatterbox TTS!",
  "voice": "default"
}
```

## API Endpoints

### Synthesize

- **Endpoint**: `/synthesize`
- **Method**: POST
- **Request Body**:
  - `text`: The text you want to convert to speech.
  - `voice`: The voice you want to use (optional).

### List Voices

- **Endpoint**: `/voices`
- **Method**: GET
- **Description**: Returns a list of available voices.

### Voice Cloning

- **Endpoint**: `/clone`
- **Method**: POST
- **Request Body**:
  - `voice_sample`: Audio sample for cloning.
  
## Predefined Voices

Chatterbox TTS comes with several predefined voices. You can list these voices using the `/voices` endpoint. Each voice has its unique characteristics, allowing you to choose the best fit for your application.

## Voice Cloning

Voice cloning allows you to create a personalized voice profile. To clone a voice, provide an audio sample to the `/clone` endpoint. The server will process the sample and create a new voice profile that you can use in your TTS requests.

## Large Text Processing

The server can handle large texts efficiently. If your input text exceeds a certain length, the server will automatically split it into manageable chunks. This ensures smooth processing without losing any content.

## Execution Options

You can run the Chatterbox TTS Server on both GPU and CPU. If you have a compatible GPU, the server will utilize it for faster processing. If not, it will fall back to CPU execution. 

### Configuration

To configure the execution options, edit the `config.json` file in the root directory. You can specify the following settings:

```json
{
  "use_gpu": true,
  "max_text_length": 5000
}
```

## Contributing

We welcome contributions to improve the Chatterbox TTS Server. If you have ideas, bug fixes, or new features, please fork the repository and submit a pull request.

### Steps to Contribute

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes.
4. Commit and push your changes.
5. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or feedback, please open an issue in the repository or contact the maintainer directly.

## Releases

To download the latest release, visit the [Releases](https://github.com/Anshudhattarwal/Chatterbox-TTS-Server/releases) section. Follow the instructions provided there to download and execute the files.

For any issues or updates, please check the "Releases" section in the repository.

---

Thank you for your interest in the Chatterbox TTS Server! We hope you find it useful for your projects.