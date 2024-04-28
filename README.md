<h1 align="center">Numeric Dataset Generator</h1>
This program is designed to generate human-like requests/requests/orders to solve a numeric expression. This is useful for using as a dataset for AI.

The program uses pthread for multithreading.

## Dependencies
This program only needs the [Rave](https://github.com/Ttimofeyka/Rave) compiler.

## Testing
To test, after compilation (using build.sh, build.bat or `rave main.rave -o numdatagen`) write:

for Windows: `numdatagen 2 100000 0 1000`,

for Linux: `./numdatagen 2 100000 0 1000`.

2 - count of threads;

100000 - count of numbers to generate **per thread**;

0 - minimum value of numbers;

1000 - maximum value of numbers.
