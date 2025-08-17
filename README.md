# LiveKit Orpheus TTS Plugin

A high-performance text-to-speech plugin for LiveKit agents using the Orpheus TTS model, featuring both streaming and non-streaming implementations.

## Features

- **Low Latency**: ~160ms time-to-first-byte (TTFB) on RTX 4090
- **Streaming Support**: Real-time audio generation with streaming capabilities
- **Multiple Voice Options**: Support for various fine-tuned voice models
- **LiveKit Integration**: Seamless integration with LiveKit agents framework

## Requirements

- LiveKit Agents v1.2 or higher
- [Orpheus streaming server](https://github.com/taresh18/orpheus-streaming) (recommended for best performance)

## Installation

1. Clone or download this plugin into your LiveKit-based agents project root directory
2. Ensure you have the Orpheus streaming server running

## Usage

Initialize your agent session with the LocalTTS plugin:

```python
from your_plugin_path import LocalTTS

session = AgentSession(
    # ... other configuration
    tts=LocalTTS(
        base_url="<orpheus_server_url>",  # e.g., "http://localhost:8000"
        voice="tara",  # or any other available voice
    )
)
```

## Fine-tuned Models

I have finetuned Orpheus on various custom voices, all are availabe on my huggingface:

- **Maya Voice**: [`taresh18/orpheus-maya`](https://huggingface.co/taresh18/orpheus-maya)
- **Lucy Voice**: [`taresh18/orpheus-lucy`](https://huggingface.co/taresh18/orpheus-lucy)
- **Anime Speech**: [`taresh18/orpheus-animespeech`](https://huggingface.co/taresh18/orpheus-animespeech)
- **AnimeVox Dataset**: [`taresh18/AnimeVox`](https://huggingface.co/datasets/taresh18/AnimeVox)

## Performance

- **Latency**: ~160ms TTFB on RTX 4090 GPU
- **Streaming**: Real-time audio generation and playback
- **Compatibility**: Tested with LiveKit Agents v1.2

