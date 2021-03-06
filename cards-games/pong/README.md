# Playing Pong

## Printing on A4

![preview first page](preview/pong-a4-deCH-0.png)
![preview second page](preview/pong-a4-deCH-1.png)  

Download this PDF and print it both sides witout any resizing on A4 paper:  

- [A4 pdf Deutsch](https://github.com/CoderDojoZH/resources/raw/master/cards-games/pong/pong-a4-deCH.pdf)
- [A4 pdf English](https://github.com/CoderDojoZH/resources/raw/master/cards-games/pong/pong-a4-en.pdf)

## Preparing the PDF and PNG files

### Producing the A4 PDF and its PNG preview

- producing the PDF from Scribus with the following custom range:  
  `8,1,6,3,2,7,4,5`
  Save it as `pong-a6-reordered-en.pdf`
- use `pdfnup` (from the pdfjam package) to put 4 A6 pages on each A4 side:  
  `pdfnup --nup 2x2 --frame false --no-landscape pong-a6-reordered-deCH.pdf --outfile pong-a4-deCH.pdf`
  `pdfnup --nup 2x2 --frame false --no-landscape pong-a6-reordered-en.pdf --outfile pong-a4-en.pdf`
- for the PNG preview of the A4 version:  
  `convert -background white -alpha remove -resize 300x pong-a4-deCH.pdf pong-a4-deCH.png`  
  to get `pong-a4-deCH-1.png` to `pong-a4-deCH-3.png`
  `convert -background white -alpha remove -resize 300x pong-a4-en.pdf pong-a4-en.png`
