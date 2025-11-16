# Magic Square

A responsive single-page web application built with HTML, CSS, and JavaScript that allows users to create dynamic square grids, fill cells sequentially with numbers, calculate row/column/diagonal sums, and undo actions step-by-step. This tool simulates aspects of constructing a magic square, where all rows, columns, and diagonals ideally sum to the same value, providing an educational and interactive experience for mathematics enthusiasts [web:91][web:92].

## Features

- **Dynamic Grid Creation**: Specify grid size (1x1 to 10x10) and starting number to generate a square grid of clickable cells [web:91].
- **Sequential Filling**: Click empty cells to assign the next number in sequence, starting from the user-defined value and incrementing by 1 each time [web:91].
- **Sum Calculations**: Button to compute and display sums for each row, column, and both main/anti-diagonals (cross), treating empty cells as 0 [web:21][web:29].
- **Multi-Step Undo**: Undo button reverses the last fill action (clears cell, decrements current number); repeated clicks undo further steps using a stack-based history [web:53][web:55].
- **Responsive Design**: Grid and controls adapt to screen size using CSS Grid, flexbox, and viewport units for mobile/desktop compatibility [web:65][web:68].
- **User-Friendly Interface**: Aligned form controls with consistent labeling, hover effects, and visual feedback for filled cells [web:74][web:75].

## How to Play

1. Enter the desired grid size (e.g., 3 for a 3x3 square) and starting number (e.g., 1).
2. Click "Create Square" to generate the empty grid.
3. Click on cells to fill them sequentially (e.g., first click fills with starting number, second with +1, etc.).
4. Use "Sum" to view row sums (e.g., Row Sums: 15, 15, 15), column sums, and diagonal sums after filling.
5. Click "Undo" to reverse fills one by one; sums are hidden after undos to reflect changes.
6. Aim to fill the grid such that all sums equal the magic constant: ( n(n^2 + 1)/2 ) for size ( n ) starting from 1 [web:35][web:96].

The game prevents overwriting filled cells and limits grid size to avoid performance issues [web:91].

## Screenshots

- **Controls and Empty Grid**: Aligned inputs and buttons above a responsive 3x3 grid.
- **Filled Grid with Sums**: Example shows a completed 3x3 magic square with Row Sums: 15, 15, 15; Column Sums: 15, 15, 15; Main Diagonal: 15; Anti-Diagonal: 15.
- **Mobile View**: Grid scales down on smaller screens, with wrapped controls for touch interaction [web:91].

## Technologies Used

- **HTML5**: Structure for inputs, buttons, and grid container.
- **CSS3**: Flexbox for alignment, CSS Grid for the responsive square layout, clamp() for scaling, and aspect-ratio for square cells [web:77][web:82].
- **Vanilla JavaScript**: Handles grid creation, event listeners for clicks, stack for undo history, matrix summation for rows/columns/diagonals [web:53][web:21].

No external libraries or frameworks are required, keeping it lightweight and browser-native [web:91].

## Installation and Usage

1. Clone or download the repository (or save the provided `index.html` file).
2. Open `index.html` in any modern web browser (Chrome, Firefox, Safari, Edge).
3. No build tools or server needed; it runs entirely client-side.
4. For development, edit the HTML file directly; changes take effect on refresh.

Tested on desktops and mobiles as of November 2025 [web:91].

## Potential Improvements

- Auto-generate a complete magic square using algorithms like Siamese method for odd orders [web:35].
- Add validation to check if the grid is a true magic square (all sums equal).
- Include save/load grid state via localStorage.
- Support even-order grids or advanced filling rules [web:96].

## License

This project is open-source and free to use/modify under the MIT License. See LICENSE file for details.

## Acknowledgments

Inspired by classic magic square puzzles and web development best practices from MDN and Stack Overflow [web:91][web:2].
