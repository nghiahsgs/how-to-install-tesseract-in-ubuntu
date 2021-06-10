# how-to-install-tesseract-in-ubuntu
how to install tesseract in ubuntu

## STEP 1: Install
```
sudo apt-get install tesseract-ocr
tesseract -v
```

## STEP 2: How to use tesseract
```
tesseract tesseract_inputs/example_01.png stdout
```

## STEP 3: How to use tesseract in python
```
filename = 'cell_publisher.png'
text = pytesseract.image_to_string(Image.open(filename))
os.remove(filename)
print(text)
```

## Tips: Most common tricks use to phrase preprocessing image
tip1: convert to gray scale image
```
filename = 'cell_publisher.png'
# image = cv2.imread(filename)
# gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
tip2: apply threshold to image
```
## apply thresholding to preprocess the image
# gray = cv2.threshold(gray, 0, 255,
# 		cv2.THRESH_BINARY | cv2.THRESH_OTSU)[1]

```
tip3: apply blur
```
# apply blur
# gray = cv2.medianBlur(gray, 3)
```
