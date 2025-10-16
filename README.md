# P-th Prime Finder

## Summary

This is a minimal, working application designed to find the *p*-th prime number. It consists of two main components:
1.  A Python command-line script (`main.py`) for server-side or local execution.
2.  An interactive HTML file (`index.html`) with embedded JavaScript for a client-side, in-browser experience.

The program takes a positive integer `p` as input and outputs the prime number at that position in the sequence of primes (e.g., for p=1, the output is 2; for p=2, the output is 3).

## Setup

No external libraries or complex installation are required.

### Prerequisites

*   **For the command-line script:** Python 3.x
*   **For the web interface:** A modern web browser (e.g., Chrome, Firefox, Safari).

### Installation

1.  Clone or download the files to your local machine.
2.  No further installation steps are necessary.

## Usage

You can use either the command-line script or the web interface.

### Command Line (`main.py`)

1.  Open your terminal or command prompt.
2.  Navigate to the directory where you saved the files.
3.  Run the script by providing the position `p` as a command-line argument.

**Example:**
To find the 10th prime number:
```bash
python main.py 10
```

**Output:**
```
The 10-th prime number is: 29
```

### Web Interface (`index.html`)

1.  Locate the `index.html` file on your computer.
2.  Open it directly in your web browser (e.g., by double-clicking it).
3.  Enter a positive integer into the input field.
4.  Click the "Find Prime" button.
5.  The result will be displayed on the page below the button.

**Note:** Calculating primes for very large numbers (e.g., p > 10,000) can be computationally intensive and may cause your browser to become unresponsive for a moment.

## Code Explanation

### `main.py`

This Python script implements the core logic for finding the p-th prime.

*   `is_prime(n)`: A function that efficiently checks if a given number `n` is prime. It uses an optimized trial division method that skips multiples of 2 and 3.
*   `get_pth_prime(p)`: This function iterates through numbers (starting from 2 and then odd numbers) and uses `is_prime()` to count them until it finds the prime at the desired position `p`.
*   The main execution block (`if __name__ == "__main__":`) handles parsing command-line arguments, validating the input, calling the main logic, and printing the result.

### `index.html`

This single file provides a complete, self-contained web interface.

*   **HTML**: Defines the structure of the page, including a title, an input form for the number `p`, a submit button, and a `div` to display the result.
*   **CSS**: Embedded within a `<style>` tag, it provides a clean and modern design for the user interface, making it responsive and easy to use.
*   **JavaScript**: Embedded within a `<script>` tag, it replicates the prime-finding logic from the Python script.
    *   It adds an event listener to the form to capture user submissions.
    *   It includes client-side input validation.
    *   The `isPrime` and `getPthPrime` functions are implemented in JavaScript to perform the calculation directly in the browser, eliminating the need for a server backend.
    *   A `setTimeout` is used to ensure the UI updates with a "Calculating..." message before a potentially long computation begins.

## License

This project is licensed under the MIT License.
