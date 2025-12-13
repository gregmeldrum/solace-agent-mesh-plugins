# LocalTts SAM Plugin

An agent plugin for Solace Agent Mesh that provides text to speech. 

## Description

This plugin enables agents to perform text to speech operations using VibeVoice. 

## Features
Access to four high-quality voices:
  - Carter (male voice)
  - Davis (male voice)
  - Emma (female voice)
  - Grace (female voice)

Enables the ability for SAM to respond to users verbally. 


## Installation

### 1. Build the Plugin

From the plugin directory:

```bash
sam plugin build
```

This creates a wheel file in the `dist/` directory.

### 2. Install in Your SAM Project

```bash
cd /path/to/your/sam/project
sam plugin add local-tts --plugin /path/to/local-tts/dist/local_tts-0.1.0-py3-none-any.whl
```
## Usage

## Examples

## License

See project license.

## Author

Greg Meldrum <greg.meldrum@solace.com>