# Lumen

### Brightening Lives and Futures

Lumen is an assistive communication application designed to help people communicate when speaking is difficult.

Lumen provides multiple ways to create and communicate messages, including a visual communication board, keyboard input, saved phrases, and gesture-based controls. Messages can be converted into spoken communication using speech synthesis.

The goal of Lumen is to provide a flexible, accessible communication interface that can adapt to different users and interaction methods.

---

## Table of Contents

* [Overview](#overview)
* [How Lumen Works](#how-lumen-works)
* [Features](#features)
* [Getting Started](#getting-started)
* [Lumenboard](#lumenboard)
* [Basic Mode](#basic-mode)
* [Advanced Mode](#advanced-mode)
* [Letters and Spelling](#letters-and-spelling)
* [Preset Phrases](#preset-phrases)
* [Message Area](#message-area)
* [Speech Output](#speech-output)
* [Gesture Input](#gesture-input)
* [Default Gesture Model](#default-gesture-model)
* [Camera Input](#camera-input)
* [Gesture Navigation](#gesture-navigation)
* [Settings and Detection Speed](#settings-and-detection-speed)
* [Saved Phrases](#saved-phrases)
* [Custom Gesture Models](#custom-gesture-models)
* [Privacy](#privacy)
* [Troubleshooting](#troubleshooting)
* [Technology](#technology)
* [Project Structure](#project-structure)
* [Development](#development)
* [Building Lumen](#building-lumen)
* [Limitations](#limitations)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [Feedback](#feedback)
* [License](#license)

---

# Overview

Lumen is built around a simple communication pipeline:

**Gesture / Button**

**→**

**Lumen**

**→**

**Message**

**→**

**Speech**

A user can interact with Lumen directly through the interface or, when gesture recognition is enabled, use supported gestures to navigate and activate communication controls.

The system is designed so that communication does not require every message to be manually typed. Frequently used phrases can be accessed immediately, while Advanced mode provides tools for creating custom messages.

---

# How Lumen Works

Lumen supports three primary communication pathways.

### 1. Communication Board

Users can select predefined buttons containing frequently used words and phrases.

This provides rapid access to common communication needs without requiring the user to construct a message character by character.

### 2. Keyboard Input

Messages can be composed using direct keyboard input when available.

This allows users to create arbitrary messages without relying exclusively on predefined buttons.

### 3. Gesture Input

Lumen can use a Teachable Machine pose model to provide an alternative method of navigating the interface.

The default gesture system uses two classes:

* **Hello** — activates the currently selected button.
* **Nothing** — advances the selector.

This allows the communication board to be navigated using a small set of recognizable gestures.

---

# Features

Lumen currently includes:

* Accessible communication board
* Basic communication mode
* Advanced spelling mode
* Preset communication phrases
* Custom message composition
* Keyboard input
* Speech synthesis
* Gesture-based navigation
* Teachable Machine pose-model support
* Custom gesture model loading
* Saved phrases
* Local storage
* Adjustable gesture detection interval
* Camera-based gesture recognition
* Visual button-selection highlighting
* Emergency communication phrase
* Configurable communication interface

---

# Getting Started

Lumen can be accessed directly through the Lumen website.

To begin using gesture-based communication:

1. Open Lumen.
2. Allow camera access when prompted.
3. Wait for the gesture recognition model to load.
4. Position yourself clearly within the camera's field of view.
5. Open the communication board.
6. Use the board normally or enable gesture-based interaction.
7. Use the supported gestures to navigate and activate buttons.
8. Use **Say** when you want a composed message spoken aloud.

If gesture recognition is not needed, Lumen can be used through its standard interface without camera interaction.

---

# Lumenboard

The **Lumenboard** is Lumen's primary communication interface.

It organizes communication options, phrases, controls, and navigation functions into an accessible button grid.

The board is divided into different interaction modes so that frequently used communication options remain easy to access while more advanced functionality remains available when needed.

---

# Basic Mode

Basic mode is designed around commonly used communication phrases and controls.

It provides access to preset communication buttons as well as navigation to other parts of Lumen.

Example options include:

* **Hello**
* **Please**
* **Help**
* **Emergency**
* **Bathroom**
* **Turn on TV**

Basic mode is intended to minimize the number of interactions required to communicate frequently used messages.

Selecting a preset phrase sends it directly to speech output.

Basic mode also provides access to:

* Advanced mode
* Saved Phrases
* Settings

When gesture input is enabled, the selector moves through the available buttons and the **blue highlight** indicates the currently selected button.

---

# Advanced Mode

Advanced mode provides tools for creating custom messages.

Instead of relying exclusively on preset phrases, users can construct messages using individual letters and communication controls.

Advanced mode provides access to:

* Letter groups
* Individual letters
* Space
* Delete
* Delete All
* Say
* Save
* Back

This allows users to create messages that are not already included in the preset communication board.

---

# Letters and Spelling

Advanced mode organizes letters into groups to reduce the number of buttons displayed at once.

For example, users may select a group such as:

**ABCD**

or

**EFGH**

to access the individual letters within that group.

Selecting a letter adds that character to the current message.

The message can then be continued until the desired communication is complete.

Use **Back** to return to the Advanced menu.

---

# Preset Phrases

Lumen includes several ready-to-use phrases for common situations.

Current preset examples include:

| Button     | Purpose                     |
| ---------- | --------------------------- |
| Hello      | Basic greeting              |
| Please     | Polite request              |
| Help       | Request for assistance      |
| Emergency  | Communicate an emergency    |
| Bathroom   | Communicate a bathroom need |
| Turn on TV | Request an action           |

Preset phrases are designed to reduce the number of interactions required for frequently used communication.

When activated, the phrase can be sent directly to speech output.

---

# Message Area

The message area displays the text currently being composed.

It is available when using Advanced and Saved modes.

### Message controls

**Space**

Adds a space to the current message.

**Delete**

Removes the most recently entered character.

**Delete All**

Clears the current message.

**Say**

Sends the current message to speech output.

When available, the message field can also be edited directly using a keyboard.

---

# Speech Output

Lumen uses browser-based speech synthesis to convert text into spoken communication.

There are two primary speech pathways.

### Preset Speech

Preset communication phrases can be activated directly.

For example, activating a preset communication button can immediately send the corresponding phrase to speech output.

### Composed Speech

Messages created in Advanced or Saved mode can be spoken using **Say**.

Lumen attempts to use an English speech voice when one is available.

The status area indicates when speech output is active.

Speech behavior may vary depending on the operating system, browser, and available system voices.

---

# Gesture Input

Lumen supports gesture-based interaction through a Teachable Machine pose model.

Gesture input allows the user to navigate the communication interface without requiring conventional mouse or keyboard interaction.

The gesture system currently uses two classes:

| Gesture Class | Function                      |
| ------------- | ----------------------------- |
| **Nothing**   | Advances the selector         |
| **Hello**     | Activates the selected button |

The system separates navigation from activation:

**Nothing → Move**

**Hello → Select**

This allows a user to navigate through the interface using one gesture and activate a button using another.

---

# Default Gesture Model

Lumen's default gesture model is trained around a simple upper-body gesture involving the user's **left arm raised and held at approximately a right angle (90°)**.

The model contains two classes:

* **Hello**
* **Nothing**

The model distinguishes between these classes based on the trained pose patterns.

The default model is intended to recognize the user's left-arm position clearly within the camera frame.

## Recommended Positioning

For reliable recognition:

* Keep your left arm clearly visible.
* Hold the arm at approximately a 90° angle when performing the trained gesture.
* Keep your upper body within the camera's field of view.
* Maintain consistent lighting.
* Avoid significant visual obstruction.
* Keep your position relatively consistent.
* Hold the gesture throughout the detection interval.

The model's performance depends on the conditions under which it was trained and the environment in which it is used.

---

# Gesture Navigation

When gesture input is enabled, the currently selected communication button is visually indicated by a **blue highlight**.

The selector moves sequentially through available controls.

### Nothing

The **Nothing** gesture advances the selector to the next available button.

### Hello

The **Hello** gesture activates the currently highlighted button.

A simplified interaction cycle is:

```text
Nothing
   ↓
Next Button
   ↓
Nothing
   ↓
Next Button
   ↓
Hello
   ↓
Activate Button
```

This system allows communication controls to be accessed through repeated gesture interactions.

---

# Camera Input

The camera provides the video input required for gesture recognition.

Lumen requests camera permission when gesture functionality is initialized.

Gesture recognition generally works best when:

* The user is clearly visible.
* The upper body is unobstructed.
* Lighting is sufficient.
* The camera is positioned appropriately.
* Background distractions are minimized.
* The user remains within the camera frame.

Camera access is not required for standard communication-board functionality when gesture recognition is not being used.

---

# Settings and Detection Speed

Lumen provides a configurable gesture detection interval.

The detection interval determines how frequently Lumen evaluates the camera input for a recognized gesture.

The available range is:

**1–10 seconds**

### Shorter intervals

A shorter interval causes gesture recognition to be evaluated more frequently.

This can make the interface respond more often.

### Longer intervals

A longer interval provides additional time for the user to prepare and hold a gesture before recognition occurs.

### Default

The default detection interval is:

**5 seconds**

The interval can be changed through **Settings**.

---

# Saved Phrases

Saved Phrases allows frequently used custom messages to be stored for future communication.

To save a phrase:

1. Open Advanced mode.
2. Compose the desired message.
3. Select **Save**.
4. Open Saved Phrases.
5. Select the saved phrase when needed.

Saved phrases are stored locally on the device.

They remain available after the application is closed, provided the browser/application's local storage has not been cleared.

---

# Custom Gesture Models

Lumen supports custom Teachable Machine pose models.

This allows the gesture-recognition system to be adapted to different users, environments, or trained gesture patterns.

To load a custom model:

1. Create or obtain a compatible Teachable Machine pose model.
2. Ensure the model contains exactly two classes.
3. Name the classes:

   * `Hello`
   * `Nothing`
4. Copy the model URL.
5. Open Lumen Settings.
6. Enter the model URL.
7. Select **Load Model**.
8. Wait for the model to initialize.
9. Test both gesture classes.

## Required Classes

The model must contain exactly:

```text
Hello
Nothing
```

The names are significant because Lumen uses these classes to determine the appropriate interface action.

A model with differently named classes may not function correctly with Lumen's gesture controls.

---

# Custom Model Behavior

Custom models can use different physical gestures from the default model.

For example, a user could train a model around a different recognizable pose, provided the resulting model still exposes the required `Hello` and `Nothing` classes.

The model is responsible for recognizing the physical pose.

Lumen is responsible for interpreting the resulting class as an interface command.

This creates a separation between:

**Pose Recognition**

and

**Interface Control**

```text
Camera
   ↓
Pose Model
   ↓
Hello / Nothing
   ↓
Lumen Gesture Controller
   ↓
Navigation / Button Activation
```

---

# Local Storage

Lumen uses local browser storage for certain user-specific settings and data.

This includes:

* Saved phrases
* The most recently valid gesture-model URL
* Other locally configured application state where applicable

Because these values are stored locally, they are associated with the current device/browser environment.

Clearing browser or application storage may remove locally stored information.

---

# Privacy

Lumen requires camera access when gesture recognition is enabled.

Camera video is used as the input for pose recognition.

The camera is only required for features that use gesture recognition.

Saved phrases and the configured model URL are stored locally on the device.

Lumen does not require an online account for its basic communication functionality.

## Camera Processing

Gesture recognition uses camera input to determine which trained gesture class is currently being detected.

Users should review their browser and operating-system camera permissions to understand which applications have access to their camera.

---

# Troubleshooting

## Camera Isn't Working

If the camera is not functioning:

1. Confirm that camera permission has been granted.
2. Check that the correct camera is available.
3. Close other applications that may be using the camera.
4. Reload Lumen.
5. Reinitialize gesture recognition.

If the browser continues blocking camera access, review its site permissions.

---

## Gesture Isn't Being Detected

Try the following:

* Improve lighting.
* Make sure your upper body is visible.
* Keep your left arm visible.
* Hold the trained pose consistently.
* Remain inside the camera frame.
* Reduce visual obstructions.
* Hold the gesture for the entire detection interval.
* Confirm that the correct model is loaded.

If using a custom model, verify that the classes are exactly:

```text
Hello
Nothing
```

---

## Gesture Is Activating the Wrong Button

The selector advances sequentially.

If the selected button is not the desired button:

1. Use the **Nothing** gesture to advance.
2. Watch the blue highlight.
3. Stop when the desired button is selected.
4. Use **Hello** to activate it.

Remember that the selector does not jump directly to a button.

---

## Speech Isn't Playing

Check:

* Device volume
* Application/browser volume
* Browser tab mute state
* Available system speech voices
* Browser speech-synthesis support

Some browser environments may require an initial user interaction before speech synthesis can begin.

Speech behavior can also vary depending on the operating system and available voice engines.

---

## Buttons Aren't Responding

If buttons do not respond:

1. Confirm that Lumen has finished loading.
2. Confirm that the interface is visible.
3. If using gestures, verify that gesture recognition is active.
4. Check the selected button's blue highlight.
5. Reload the application if necessary.

---

## Custom Model Won't Load

Verify that:

* The model URL is valid.
* The model is a Teachable Machine **Pose** model.
* The model has exactly two classes.
* The classes are named `Hello` and `Nothing`.
* The model has finished training/exporting.
* The model URL is accessible.

---

# Technology

Lumen combines several web and desktop technologies to provide its communication functionality.

Major technologies used by the project include:

* **Electron** — desktop application framework
* **JavaScript** — application logic
* **HTML/CSS** — interface
* **p5.js** — interactive graphics and interface functionality
* **ml5.js** — machine-learning integration
* **TensorFlow.js** — machine-learning infrastructure
* **Teachable Machine** — customizable pose-model training
* **Web Speech API** — speech synthesis
* **Webcam / Media APIs** — camera input
* **localStorage** — local persistence

The project is currently designed primarily for **Windows**.

---

# Architecture

At a high level, Lumen can be viewed as several interconnected systems.

```text
                    ┌──────────────────┐
                    │      Camera      │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │  Pose Detection  │
                    └────────┬─────────┘
                             │
                    Hello / Nothing
                             │
                             ▼
┌──────────────┐     ┌──────────────────┐
│   Keyboard   │────►│                  │
└──────────────┘     │      Lumen       │
                     │     Controller   │
┌──────────────┐     │                  │
│ Communication│────►│                  │
│    Board     │     └────────┬─────────┘
└──────────────┘              │
                              ▼
                     ┌──────────────────┐
                     │     Message      │
                     └────────┬─────────┘
                              │
                              ▼
                     ┌──────────────────┐
                     │ Speech Synthesis │
                     └──────────────────┘
```

The communication interface acts as the central layer connecting direct input, gesture input, message construction, saved phrases, and speech output.

---

# Project Structure

The exact repository structure may evolve during development, but the project generally separates the application into interface, logic, assets, and configuration components.

A simplified representation is:

```text
Lumen/
├── assets/
├── models/
├── index.html
├── style.css
├── script.js
├── Electron.js
├── package.json
├── package-lock.json
└── README.md
```

Depending on the current release, additional files and directories may be present.

---

# Development

Lumen is currently in active development.

The project is being developed as an evolving assistive-communication platform rather than a finished medical or clinical device.

Development areas include:

* Communication interface improvements
* Gesture recognition
* Accessibility
* Speech output
* Customization
* User experience
* Documentation
* Reliability
* Additional platform support

Feedback and testing are welcome as the project continues to develop.

---

# Running the Project Locally

For developers who want to work with the source code, clone the repository and install its dependencies.

```bash
git clone <repository-url>
cd Lumen
npm install
```

Then start the development application:

```bash
npm start
```

If Windows PowerShell blocks the `npm.ps1` script, the Windows command can be invoked through:

```bash
npm.cmd start
```

The same approach can be used with other npm commands when necessary.

---

# Building Lumen

The project uses Electron Builder for application packaging.

After installing dependencies, a production build can be generated using the project's configured build command.

A typical workflow is:

```bash
npm install
npm run build
```

The exact build command may change as the project evolves, so refer to `package.json` for the authoritative scripts configured for the current version.

---

# Platform

## Current Platform

**Windows**

Lumen is currently developed and distributed primarily for Windows.

Support for additional operating systems may be explored as development continues.

---

# Limitations

Lumen is an actively developed project and has limitations.

### Gesture Recognition

Pose recognition depends on:

* Camera quality
* Lighting
* User positioning
* Model training
* Background conditions
* Detection interval
* Recognition accuracy

Gesture recognition should therefore not be assumed to be perfect.

### Speech Synthesis

Speech output depends partly on the speech-synthesis capabilities and voices available on the user's system.

### Custom Models

Custom gesture models must follow Lumen's required class structure:

```text
Hello
Nothing
```

Models that do not follow this structure may not operate correctly.

### Local Data

Saved phrases are stored locally rather than synchronized across devices.

Changing or clearing browser/application storage can remove saved data.

---

# Roadmap

Lumen's development roadmap may evolve as testing and feedback continue.

Potential development areas include:

* [ ] Expanded communication-board customization
* [ ] More flexible gesture configuration
* [ ] Improved gesture recognition
* [ ] Additional accessibility options
* [ ] Improved onboarding
* [ ] More speech configuration
* [ ] Expanded saved-phrase management
* [ ] Improved documentation
* [ ] Additional operating-system support
* [ ] Additional communication workflows
* [ ] Broader testing with different environments and users

This roadmap is not a guarantee of future functionality and may change as development progresses.

---

# Contributing

Lumen is an open development project, and feedback can help improve the application.

Potential contributions include:

* Bug reports
* Feature suggestions
* Accessibility feedback
* Gesture-model experimentation
* Documentation improvements
* Interface improvements
* Testing across different environments
* Code contributions

## Before Contributing

When reporting an issue, provide as much relevant information as possible, such as:

* Operating system
* Lumen version
* Browser/runtime environment
* Feature being used
* Steps to reproduce the issue
* Error messages
* Whether the default or a custom gesture model was being used

Avoid including private or sensitive information in issue reports.

---

# Feedback

Testing and feedback are particularly useful while Lumen is under active development.

If you find a problem or have an idea for improving Lumen, open an issue in the repository with a clear description of the problem or proposed improvement.

For bugs, explain:

**What happened → What you expected → How to reproduce it**

For feature requests, explain:

**What you want → Why it would be useful → How you imagine it working**

---

# Design Philosophy

Lumen is built around a simple principle:

> Communication should not depend on a single input method.

Different users may have different abilities, environments, and preferred interaction methods.

For that reason, Lumen combines:

**Preset communication**

*

**Custom message creation**

*

**Keyboard input**

*

**Gesture interaction**

*

**Speech output**

The objective is to give the user multiple pathways through the same communication system.

---

# Accessibility Philosophy

Lumen is designed with accessibility as a central consideration rather than as an additional feature.

The interface attempts to reduce unnecessary interaction by providing:

* Frequently used preset phrases
* Large communication controls
* Sequential gesture navigation
* Custom message construction
* Saved phrases
* Speech output
* Configurable gesture timing
* Custom gesture models

The project continues to evolve through development and testing.

---

# Project Status

**Lumen 2.0 — Active Development**

Lumen is currently under active development.

Features, interface behavior, documentation, and supported platforms may change between releases.

The repository should be considered a development project rather than a finalized clinical communication device.

---

# Acknowledgments

Lumen builds upon several open-source technologies and web APIs that make its functionality possible, including:

* Electron
* p5.js
* ml5.js
* TensorFlow.js
* Teachable Machine
* Web Speech API
* Web Camera / Media APIs

The project would not be possible without the broader open-source and machine-learning ecosystems supporting these technologies.

---

# License

See the repository's license file for the terms governing the use, modification, and distribution of Lumen.

---

# Final Note

Lumen is an evolving project.

The application is being developed with the goal of making communication technology more flexible and accessible while allowing the underlying interaction system to adapt to different users.

**Lumen**

**Brightening Lives and Futures.**
