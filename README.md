<div align="center">

# Image Compressor

**Reduce the number of colors in an image with k-means clustering, in Haskell.**

<img alt="Haskell" src="https://img.shields.io/badge/Haskell-5D4F85?style=flat-square&logo=haskell&logoColor=white"/> <img alt="Stack" src="https://img.shields.io/badge/Stack-4B4B4B?style=flat-square&logo=&logoColor=white"/>

<sub>Team of 2 · March 2024</sub>

</div>




## About the project

An image is read as a list of pixels (position and RGB color). The program groups the colors into *k* clusters with the **k-means** algorithm, repeating until the clusters move less than a given limit, and prints each cluster with its pixels. It is written in pure functional style, with errors handled explicitly.

## Build and run

```bash
make                                   # uses Stack
./imageCompressor -n 4 -l 0.8 -f pixels.txt
```

| Flag | Meaning |
|---|---|
| `-n` | Number of colors (clusters) to keep |
| `-l` | Convergence limit: stop when clusters move less than this |
| `-f` | Path to the file of pixels |

The input is one pixel per line, as `(x,y) (r,g,b)`.

## My contribution

10 of the project's 22 commits, shared with Yanis Harkouk.

- **Parsing**: reading the file and turning every line into a pixel in a typed data structure
- **Error handling**: invalid files, unreadable files, and malformed lines exit cleanly with the expected error code
- **Structure**: refactoring `main` into small, readable functions

## Team

Yanis Harkouk and Eva Legrand.
