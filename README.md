 This C++ program is a Number Base Converter that allows a user to convert numbers between decimal, binary, and hexadecimal formats. It's designed with a menu-driven command-line interface, meaning the user interacts by typing numbers to select options from a displayed menu.
Here's a breakdown of its key components and functionality:
Core Conversion Functions:
decimalToBinary(int decimalNum): Takes a decimal integer and returns its binary representation as a std::string. It uses repeated division by 2 and collects the remainders.
binaryToDecimal(const std::string& binaryStr): Takes a binary string and converts it to its decimal integer equivalent. It processes each binary digit, multiplying it by the corresponding power of 2. Includes basic validation for non-binary characters.
decimalToHexadecimal(int decimalNum): Converts a decimal integer to its hexadecimal string representation. Similar to binary conversion, it uses repeated division by 16 and maps remainders (0-15) to hexadecimal digits (0-9, A-F).
hexadecimalToDecimal(const std::string& hexStr): Converts a hexadecimal string to its decimal integer. It processes each hex digit, converts it to its decimal value (e.g., 'A' becomes 10), and multiplies by the corresponding power of 16. Also includes validation for invalid hex characters.
User Interface and Control:
displayMenu(): Prints a list of options to the console, guiding the user on available conversions.
main() function (the program's entry point):
Contains a do-while loop that continuously displays the menu and prompts the user for a choice until the "Exit" option is selected.
Uses a switch statement to execute the specific conversion function based on the user's input.
Input Handling (Crucial in C++): It includes robust error handling for user input:
Checks if std::cin failed (e.g., if the user typed text when an integer was expected).
std::cin.clear() and std::cin.ignore() are used to reset the input stream's error state and discard invalid input, preventing an infinite loop.
std::getline() is used for reading string inputs (binary, hexadecimal) to handle entire lines, including potential spaces.
Demo Functionality:
demoRandomConversion(): Generates a random integer between 0 and 99.
It then converts this random number to binary using decimalToBinary() and displays both the original number and its binary form.
It also performs a verification step by converting the generated binary back to decimal to confirm the conversion works correctly.
It utilizes the modern C++ <random> library for generating high-quality random numbers.
In essence, this program demonstrates:
Modular Programming: Breaking down the problem into smaller, manageable functions (e.g., one function per conversion type).
Command-Line Interface (CLI) Design: Creating an interactive, text-based user experience.
Number Base Conversion Algorithms: The fundamental logic behind converting numbers between different bases.
Robust Input Handling in C++: Essential techniques for gracefully dealing with incorrect or unexpected user input, making the program more user-friendly and stable.
Use of Standard C++ Libraries: iostream, string, cmath, iomanip, random, and limits.
