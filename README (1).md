# Animated ASCII Ocean 🌊

A tiny Python program (about 20 lines) that draws a moving ocean in your terminal by combining two sine waves and showing their height as ASCII characters.

## Aim
To simulate an animated ocean in the terminal using the superposition of two sine waves.

## Prerequisites
- Python 3.x
- Built-in modules only: `math`, `time`, `shutil` (no installation needed)
- A terminal that supports ANSI escape codes (Linux, macOS, Windows Terminal, VS Code terminal)

## Usage
1. Save the program as `ocean.py`.
2. Run it:
   ```bash
   python ocean.py
   ```
3. Press `Ctrl+C` to stop.

## Procedure
1. Create `ocean.py` and import `math`, `time`, and `shutil`.
2. Get the terminal width and define the wave characters (`" ._-~=*#"`).
3. For each row and column, add two sine waves to get the height.
4. Map the height to a character, then clear the screen and print the frame.
5. Increase `t`, pause briefly, and repeat.

## How It Works
- Each cell's height is the sum of two sine waves moving in opposite directions.
- The height (range -2 to 2) is scaled to an index in the character string, from a blank space up to `#` for the tallest crests.
- `\033[H\033[J` clears the screen every frame, which creates the animation.

## Customization
- Try `chars = " ░▒▓█"` for a smoother look.
- Change the divisors `6` and `11` to alter the wave shape.
- Change `range(8)` to make the ocean taller or shorter.
- Adjust `time.sleep(0.06)` to change the speed.

## Result
A continuously moving ocean appears in the terminal. Crests show as dense symbols like `#` and `*`, and troughs show as blanks or dots. On `Ctrl+C`, it prints "Calm seas."

## Conclusion
Simple mathematics can produce a dynamic visual effect. The program demonstrates nested loops, string indexing, ANSI escape codes, and exception handling in about 20 lines.
