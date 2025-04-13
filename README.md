<h1 align="center">Numeric Dataset Generator</h1>
This program is designed to generate human-like requests/orders to solve a numeric expression using provided format. This is useful for using as a dataset for AI.

You can add your own instructions or own format using `instructions.json` file.

Default format is `.jsonl` (`instruction`/`response`).

## Dependencies
This program only needs the [Rave](https://github.com/Ttimofeyka/Rave) compiler.

## Testing
To test, after compilation (using build.sh, build.bat or `rave ./main.rave -o numdatagen`) write:

for Windows: `numdatagen dataset.txt 2 100000 200 500`,

for Linux: `./numdatagen dataset.txt 2 100000 200 500`.

dataset.txt - name of file to write into;

2 - count of threads;

100000 - count of numbers to generate **per thread**;

200, 500 - min and max values of numbers.

## Speed metrics

Tested on Windows 10 (using WSL), i5-12400f and 32 GB RAM (DDR4-3200).

`time ./numdatagen dataset.txt 2 10000 -500 500` - 0.019s, 1.28MB

`time ./numdatagen dataset.txt 6 100000 500 2000` - 0.124s, 38.32MB

`time ./numdatagen dataset.txt 6 10000000 0 1000` - 15.617s, 3.64GB

Due to the measurements of the program speed, it can be concluded that this generation algorithm is very effective.