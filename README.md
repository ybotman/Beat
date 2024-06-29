# Beat Analysis Project (R3)

## Overview

This project is focused on analyzing the beat and pulse of music tracks, particularly for tango music. The application allows users to upload audio files, visualize the waveform, annotate sections and phrases, and analyze beats using `librosa`.

## Project Structure

- **Frontend**: Built with Next.js, providing a modern, responsive UI for interacting with the application.
- **Backend**: Built with FastAPI, handling audio processing and serving as the API backend.

## Features

1. **Audio Upload and Management**:
   - Users can upload WAV audio files.
   - Uploaded files are stored on the server.
   - A list of uploaded audio files is displayed.

2. **Waveform Visualization**:
   - The waveform of the uploaded audio is visualized using `wavesurfer.js`.
   - Users can interact with the waveform to play, pause, and seek within the audio.

3. **Section Annotation**:
   - Users can add, edit, and delete sections (e.g., Intro, Section 1, Bridge) on the waveform.
   - Each section has a label, ordinal number, and start time.
   - Sections are displayed visually on the waveform.

4. **Beat Analysis with Librosa**:
   - The audio file is analyzed to detect beats and pulses using `librosa`.
   - A JSON structure representing the 32-bar form, including sections, phrases, and bars, is generated.
   - The analysis results are displayed on the UI.

5. **Interactive Audio Playback**:
   - Users can play, pause, and seek within the audio.
   - A progress bar indicates the current playback position.
   - Clicking on the progress bar allows users to jump to specific points in the audio.

6. **Annotation and Analysis Display**:
   - The 32-bar form is displayed as a grid with clickable sections, phrases, and bars.
   - Users can click on any part of the grid to play the corresponding audio segment.

7. **Save and Load Annotations**:
   - Annotations and analysis results can be saved to a JSON file.
   - Users can load previously saved annotations and analysis results from a JSON file.

## File Structure

├── backend
│   ├── app
│   │   ├── main.py
│   │   ├── routes.py
│   ├── songs
│   ├── Dockerfile
│   ├── requirements.txt
├── frontend
│   ├── src
│   │   ├── pages
│   │   │   ├── index.js
│   │   │   ├── songs.js
│   │   │   ├── song-details.js
│   │   ├── components
│   │   ├── styles
│   ├── public
│   ├── package.json
│   ├── next.config.js
│   ├── .eslintrc.json
│   ├── .prettierrc
├── .gitignore
├── README.md
