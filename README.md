# UKE-project

#  Task 2
## Implementation

We need to find if each page of the file is 
            0: machine-readable
            1: non-machine readable but OCR-able
            2: non-machine readable and not OCR-able

In order to find that, input file path is provided in `input_pdf`. Next I cropped the each page to extract the middle part to remove the page number in the pages. This is because the page number can be considered as machine-readable. Next I parsed each page of the cropped document to `classify_page` function which will classify the pages. 

### Logic

First I extracted the text from the page to confirm if it is a machine-readable page. If not, I tried to convert it to image and then extracted the ocr text to confirm non-machine readable but OCR-able page. If it is doesn't match any of the above cases or if it is not able to convert to image, then we can confirm it is non-machine readable and not OCR-able page.
