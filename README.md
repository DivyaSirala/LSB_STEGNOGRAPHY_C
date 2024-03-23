**README: LSB Steganography using C**

**LSB Image steganography** - Steganography is the art of hiding the fact that communication is taking place, by hiding
information in other information. This project is developed for hiding information in any image file.
The scope of the project is implementation of steganography tools for hiding information includes
any type of information file and image files and the path where the user wants to save Image and
extruded file.

**Overview:**
This project implements LSB (Least Significant Bit) steganography in C programming language. LSB steganography is a technique for hiding data within an image by replacing the least significant bits of the pixels with secret data. This README aims to provide an understanding of the project structure, usage, and implementation details.

**Project Structure:**
- **beautiful.bmp:** Original image file that serves as the carrier for hiding secret data.
- **common.h:** Header file containing common definitions and macros used across the project.
- **encode.c:** Implementation file for functions related to encoding (hiding) secret data into the carrier image.
- **encode.h:** Header file containing function declarations for encoding.
- **secret.txt:** Text file containing the secret data to be hidden in the carrier image.
- **stego_img.bmp:** Image file with hidden secret data, generated after encoding.
- **test_encode.c:** Test file for encoding functionality.
- **types.h:** Header file containing custom type definitions.

**Usage:**
1. **Compilation:**
   ```bash
   gcc encode.c test_encode.c -o encode
   ```
2. **Encoding:**
   ```bash
   ./encode beautiful.bmp secret.txt stego_img.bmp
   ```
   - `beautiful.bmp`: Path to the original image file (carrier).
   - `secret.txt`: Path to the file containing secret data.
   - `stego_img.bmp`: Path to the output stego image file.
3. **Decoding (Not Provided):**
   - Decoding functionality is not explicitly provided in this project. However, it can be implemented using similar techniques by reading LSBs of pixels and extracting the hidden data.

**Implementation Details:**
- **LSB Steganography:**
  - In LSB steganography, the least significant bits of pixel values are replaced with the secret data bits.
  - This project typically replaces the least significant bit of each color channel (RGB) with secret data bits.
- **Encoding Process:**
  1. Open the carrier image and read pixel values.
  2. Read secret data from the file and convert it to binary.
  3. Replace the least significant bits of pixel values with the secret data bits.
  4. Save the modified pixel values to generate the stego image.
- **Decoding Process (Not Provided):**
  - The decoding process typically involves reading the LSBs of pixel values from the stego image to extract the hidden data.

**Security Considerations:**
- LSB steganography provides a basic level of security but is susceptible to detection by sophisticated analysis techniques.
- Strong encryption methods can be used in conjunction with steganography for enhanced security.

**Contributing:**
Contributions to this project are welcome. If you find any bugs or have suggestions for improvements, please feel free to open an issue or submit a pull request.

**Author:**
Divya Sirala - divyasirala@gmail.com
