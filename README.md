# colorpalette-master
Scripts for generating a color palette out of an image, based on median cut algorithm. Used in my college project PixPalette.
## The tasks I had were: 
- To generate a palette out of a given picture.
- To write a wrapper for my script, which will compose my palette with the given picture into a single image.

## For that I've created a module called "colorpalette-master":

### Install it via pip:
```python
pip install colorpalette-master
```
### Install it manually:
- Copy the folder `cpmaster` into Lib\side-packages of your python enviroment.
- Install additional packages with:
```python
pip install scikit-image==0.19.3
```
```python
pip install numpy==1.21.6
```
```python
pip install pillow==9.4.0
```
```python
pip install image-decoding-algorithms
```
### After, import it into the script using `import cpmaster *`.

## Compiling requirements:
- Scikit-image (version '0.19.3' or newer)
- Numpy (version '1.21.6' or newer)
- Pillow (version '9.4.0' or newer)

## Running requirements:
- Python 3.7.7 or newer (code actually uses some deprecated syntax in newer versions of Python, so not sure about the last part)

## Using the package:
- Check the `____MiniDocumentation.md` or `___main___.py` files for my brief documentation on methods
- Write me an email, if there are any questions left - superavb222@gmail.com
