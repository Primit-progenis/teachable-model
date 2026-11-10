# Teachable Machine Image Demo

This repository contains a small browser page that runs an image classifier exported from Google's Teachable Machine. It loads the model in TensorFlow.js, reads frames from the webcam, and displays each class label with its prediction probability.

## How it works

1. Press **Start** to load `model.json` and `metadata.json` from `./my_model/`.
2. The page asks for webcam access and starts a mirrored 200-by-200 webcam view.
3. Each animation frame is passed to the model. The page updates the label list with the class names and confidence scores.

TensorFlow.js and the Teachable Machine image library are loaded from jsDelivr by the HTML page.

## Run it

Export an **Image Project** model from Teachable Machine and place its `model.json`, `metadata.json`, and required weight files in a `my_model/` directory beside the page. The model directory is not currently present in this repository, so the demo needs those exported files before it can load a model.

Serve the page from localhost or HTTPS, then open it in a browser and allow webcam access. A simple local static server can be used; opening the file directly may not provide the secure context required for webcam access.
