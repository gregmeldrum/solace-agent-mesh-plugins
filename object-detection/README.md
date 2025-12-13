# ObjectDetection SAM Plugin

Object detection from images using YOLOv12

This is a plugin for Solace Agent Mesh (SAM).
## Description

This plugin enables agents to perform object recognition on images. 

## Features
- Object detection in image


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
sam plugin add object-detection --plugin /path/to/object-detection/dist/object_detection-0.1.0-py3-none-any.whl
```
## Usage

## Examples

## License

See project license.

## Author

Greg Meldrum <greg.meldrum@solace.com>