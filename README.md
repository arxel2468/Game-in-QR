# Game-in-QR

This project demonstrates how to embed a simple snake game directly inside a QR code using a Base64-encoded HTML file. The QR code contains all the necessary code for the game to be played directly in a browser after scanning the QR code.

## Project Structure

The repository contains the following important files:

- **qr.svg**: The generated QR code in SVG format, which can be scanned to play the game.
- **index.html**: The minimized HTML file that contains the snake game code.
- **encodedfile.txt**: A file containing the Base64-encoded version of the `index.html` file, which was used to generate the QR code.

## How It Works

1. **Snake Game**: A simple implementation of the snake game using HTML, CSS, and JavaScript.
    - The snake moves automatically, and you control it using the arrow keys.
    - The game ends if the snake collides with the walls or itself.
    - The score increases as the snake eats food, which randomly appears on the game grid.

2. **Base64 Encoding**: The game HTML file is encoded to Base64 and prefixed with the `data:text/html;base64,` scheme. This allows the entire game to be stored within the QR code as a self-contained web page.

3. **QR Code Generation**: The Base64-encoded game was embedded inside a QR code, allowing anyone to scan it with a QR code reader and instantly play the game in their browser.

## Usage

1. **Scan the QR Code**:
    - The QR code is available in the `qr.svg` file.
    - You can scan it using any QR code reader (Google Lens or other compatible apps).

2. **Play the Game**:
    - Once the QR code is scanned, a data URL containing the HTML will be opened in your browser, and the snake game will load.

3. **Controls**:
    - Use the arrow keys to move the snake.
    - Collect the food to increase your score.
    - Avoid colliding with the walls or yourself!

## Repository Files

- `qr.svg`: The QR code image containing the encoded snake game.
- `index.html`: The minified HTML code for the snake game.
- `encodedfile.txt`: The Base64-encoded HTML file.

## How to Recreate the Project

If you'd like to recreate this project or modify the snake game:

1. Clone the repository:
    ```bash
    git clone https://github.com/arxel2468/snake-game-qr-code.git
    ```

2. Modify the `index.html` file with any changes you want for the game.

3. Minify the HTML code (optional, but recommended for smaller QR codes).

4. Use an online tool or a script to encode the modified `index.html` file into Base64.

5. Generate a QR code from the Base64-encoded string using any online QR code generator that supports `data:` URLs.

## Future Improvements

- Add touch controls for better mobile experience.
- Host the game online as an alternative way to access it directly from a URL.
- Customize the snake game further (speed control, difficulty levels, etc.).

## License

This project is open-source and can be freely modified or distributed under the [MIT License](LICENSE).
