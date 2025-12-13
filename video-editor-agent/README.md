# VideoEditorAgent SAM Plugin
Video editing using ffmpeg. 

This is a plugin for Solace Agent Mesh (SAM).
## Description

This plugin enables agents to edit videos using ffmpeg

## Features
- Video trimming
- Video concatenation
- Video format conversion
- Video filters


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
sam plugin add video-editor --plugin /path/to/video-editor-agent/dist/video_editor_agent-0.1.0-py3-none-any.whl
```
## Usage

## Examples

## License

See project license.

## Author

Greg Meldrum <greg.meldrum@solace.com>