# Text Rhythm Sequencer

[![Open the sequencer](https://img.shields.io/badge/Open_the_sequencer-%E2%96%B6-e2570f?style=for-the-badge)](https://schwebewerk.github.io/text-rhythm-sequencer/)

A single-page step sequencer for reviewing rhythmic ideas written as plain text.

```
|--|--|--|--
...._._._._.
x__x________
_x_x________
_________*__
_______*____
```

- One line per track, one character per step, loops forever.
- `_` and spaces are silent. Every other character triggers a sound.
- Each symbol gets its own synthesized sound (Web Audio, no samples), reassignable and mutable per symbol.
- No bars, no time signatures. Tempo is set in steps per minute.
- Edits apply while playing.

## Usage

Open `index.html` in a browser. No build step, no dependencies (fonts load from Google Fonts and fall back to system fonts offline).

- Space starts and stops when the text field is not focused, Ctrl/Cmd+Enter works inside it.
- Load a `.txt` file with "Open text file" or drop it onto the text field.
- "Shorter lines": either stay silent until the longest line ends, or repeat on their own length (polymeter).
- "Same symbol on two lines": either two separate sounds or one shared sound.

Text, tempo and sound assignments are kept in the browser's localStorage.
