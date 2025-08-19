# Phppolyglot
This Python script creates a polyglot JPEG/PHP file by injecting PHP code into a JPEG image without breaking the image structure. The resulting file remains a valid JPEG while also being executable as a PHP script.
# JPEG Polyglot Injector Tool

## Description

This Python script creates a polyglot JPEG/PHP file by injecting PHP code into a JPEG image without breaking the image structure. The resulting file remains a valid JPEG while also being executable as a PHP script.

## How It Works

1. **Input Validation**: The script requires exactly two arguments - input JPEG file and output file name
2. **Signature Check**: Verifies the input is a valid JPEG by checking for the standard FF D9 end marker
3. **Code Injection**: Removes the end marker, appends PHP code, then restores the marker
4. **Output**: Creates a new file that functions as both an image and a PHP script

## Technical Details

- Preserves original JPEG functionality
- Injects minimal PHP code that enables command execution
- Maintains file structure integrity
- Compatible with most JPEG images

## Usage

```bash
python3 phppolyglot.py input.jpg output.jpg
```

## Legal Notice

This tool is provided for educational and research purposes only. Users are solely responsible for complying with all applicable laws. The copyright for this tool is held by Mr Nightmare.

## Disclaimer

Unauthorized use of this tool against systems without explicit permission is illegal. Always obtain proper authorization before testing any system.
