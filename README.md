# TV Canlı Yayın Uygulaması

## Overview

**TV Canlı Yayın Uygulaması** is a web-based live TV streaming application built with HTML, CSS, and JavaScript. It uses the [HLS.js](https://github.com/video-dev/hls.js/) library to stream HLS video content and provides a TV-like user interface optimized for use with a remote control (or keyboard). The application fetches an M3U IPTV playlist, parses the channels, and displays them in an interactive, navigable menu.

## Features

- **Live Streaming:**  
  Stream live TV channels using HLS (HTTP Live Streaming).

- **Remote Control Navigation:**  
  Navigate through channels using only directional keys, Enter, and numeric keys.

- **Channel List & Search:**  
  - The channel panel displays channels from an M3U playlist.
  - A native search input lets you filter channels in real time.
  - You can toggle between the default playlist order and alphabetical order.

- **Channel Info Overlay:**  
  When you select a channel, a visually appealing overlay appears in the top-left corner displaying the channel number, title, logo, and group (if available).

- **Direct Channel Selection:**  
  Use numeric keys to jump directly to a channel.

- **Quality Selection (Optional):**  
  Press the **Q** key to bring up a quality selection menu (for streams with multiple quality levels).

- **PWA Support:**  
  The project includes a manifest and service worker registration to support Progressive Web App features.

## How It Works

1. **Loading Channels:**  
   On startup, the app fetches an M3U IPTV playlist from a remote URL, parses it to extract channel details (title, logo, URL, group, etc.), and stores the original order. The filtered channel list is updated based on user input in the search field.

2. **User Interface:**  
   - **Video Area:** Displays the live stream.
   - **Channel Panel:**  
     - Slides in from the left.
     - Contains a sort toggle button, a search input, and the channel list.
     - Navigation is controlled via remote/keyboard:
       - **Sort Button:** Toggle between the default order (as provided) and alphabetical order.
       - **Search Input:** When focused, you can type to filter the channel list using the device’s native keyboard.
       - **Channel List:** Use the arrow keys to move through the list. If you try to move above the first channel, focus automatically returns to the search field.
   - **Channel Info Overlay:**  
     Displays channel details (number, title, logo, and group) briefly at the top-left when a channel is selected.

3. **Remote Control Integration:**  
   The application is designed for TV use:
   - **Arrow Keys** to navigate between channels and menu items.
   - **Enter** to select items.
   - **Numeric Keys** for direct channel selection.
   - **Q Key** to bring up the quality selection menu.
   - **C/Left Arrow** to open/close the channel panel.

## Installation & Usage

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/xertxetin/LiveTV.git
   cd LiveTV
   run index.hmtl
   ```

2. **Open the Application:**
   - Simply open `index.html` in a modern browser that supports HLS.js (Chrome, Firefox, etc.).
   - For the best experience on a TV, load the app on a compatible web browser on your TV device.

3. **Controls:**
   - Use the remote (or keyboard) to navigate:
     - **Arrow Keys:** Move between menu items and channels.
     - **Enter:** Select a channel or toggle options.
     - **Numeric Keys:** Directly select channels.
     - **Q:** Open the quality selection menu (if available).
     - **C or Left Arrow:** Open/close the channel panel.
   - Use the search field to type channel names and filter the list (native keyboard input).

## Disclaimer

**This project is for educational purposes only.**  
The IPTV playlist (.m3u file) used in this project is provided solely as an example. Its legality and authorization for use are not guaranteed. **Please do not use this project for unauthorized or illegal streaming activities.**  
If you encounter any issues or have suggestions for improvement, please report them.

## Contributing

Contributions, suggestions, and improvements are welcome! Feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

---

*Note: This project is experimental and provided "as is" without warranty of any kind. Use it responsibly and only for learning purposes.*
