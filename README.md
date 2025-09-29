React WebOS - Super Extreme

A browser-based desktop environment built with React. React WebOS Super Extreme mimics a modern operating system experience with draggable/resizable windows, file management, terminal, text editor, paint app, notifications, and more — all inside your browser.

Features

Multi-window environment

Drag, resize, minimize, maximize windows

Animated window opening/closing

Apps included

Text Editor: Edit and save text files (supports Ctrl+S)

Paint: Draw and save images to the file system

Terminal: Simulated CLI with basic commands (ls, cat, touch, rm, import-list, save)

Files App: Manage, create, import, export, rename, delete files

Settings: Change theme (dark/light) and wallpaper

Persistent storage

All files, settings, and windows are saved in localStorage

Drag & Drop

Import files directly by dragging onto the desktop

Notifications

Custom notifications for file operations and app events

Keyboard Shortcuts

Ctrl+N: Open a new file window

Ctrl+K: Open file search

Ctrl+S: Save text files in editor

Esc: Close top-most window

Responsive design

Works on small screens, adapting dock and windows

Installation / Usage

Clone or download this repository.

Open index.html in any modern browser (Chrome, Edge, Firefox).

Start using the OS directly — no build steps required.

Optional: For development with live reloading, you can serve it via VS Code Live Server or any local HTTP server.

File Types Supported

Text (.txt)

Image (.png, .jpg, .jpeg, .gif)

Audio (.mp3, .wav)

Video (.mp4, .webm)

App Commands (Terminal)

help – Show available commands

ls – List all files

cat <filename> – Display file content

touch <filename> – Create new text file

rm <filename> – Delete a file

import-list – Show imported files

save <filename> <text> – Save content to file

Technologies Used

React 18 (CDN build)

Babel Standalone (for JSX in browser)

Vanilla JS + CSS (no bundler needed)

LocalStorage for state persistence
