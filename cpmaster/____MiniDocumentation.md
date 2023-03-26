# MiniDocumentation on colorpalette-master module

## def output_palette(filepath: str, colors: int = 8, sort_by_lightness: bool = False, pix_limit: int = 200000) -> List[List[int]]:
***Reads an image, reformats it and generates a palette out of it.***
Input:
:param filepath: *a path to the image, which you want to get the palette out of*
:param colors: *amount of colors in palette*
:param sort_by_lightness: *whether to sort palette by lightness of it's components or not*
:param pix_limit: *a maximum amount of pixels in the formatted image*
Output:
Will output a standard python list of lists of RGB colors in uint8 format ([[5,5,5],[6,6,6],...] for example)



## def output_image_with_palette(filepath: str, colors: int = 8, sort_by_lightness: bool = False, pix_limit: int = 200000) -> np.ndarray:
***Reads an image, reformats it, generates a palette out of it and then comps it with the image.***
Input:
:param filepath: *a path to the image, which you want to get the palette out of*
:param colors: *amount of colors in palette*
:param sort_by_lightness: *whether to sort palette by lightness of it's components or not*
:param pix_limit: *a maximum amount of pixels in the formatted image*
Output:
Will output an image, which will contain given image and it's palette in numpy array form
Intended for saving on hard drive via skimage.io.imsave method



## def output_palette_img(filepath: str, colors: int = 8, sort_by_lightness: bool = False, pix_limit: int = 200000) -> List[List[int]]:
***Reads an image, reformats it, generates a palette out of it and then draws it.***
Input:
:param filepath: *a path to the image, which you want to get the palette out of*
:param colors: *amount of colors in palette*
:param sort_by_lightness: *whether to sort palette by lightness of it's components or not*
:param pix_limit: *a maximum amount of pixels in the formatted image*
Output:
Will output an picture, which will contain palette of a given image in numpy array form
Intended for saving on hard drive via skimage.io.imsave method



## def DEV_formatting(img: np.ndarray, pix_limit: int, img_w: int, img_h: int, img_c: int, img_d: str) -> np.ndarray:
**USED FOR DEVELOPMENT NEEDS: IF YOU DON'T KNOW WHAT YOU'RE DOING, DON'T TOUCH IT.
NOT ACCESIBLE THROUGH THE STANDARD IMPORT STATEMENT**
***Formatting algorithm for a image, will resize it to fit the pix limit, delete/convert data.***
Input:
:param img: *input image (numpy array) to reformat*
:param pix_limit: *limit of pixels for the reformatted image*
:param img_w: *width of the image*
:param img_h: *height of the image*
:param img_c: *amount of channels of the image (usually 3 for R, G, B)*
:param img_d: *dtype of the image (uint8, int16 for example)*
Output:
A image in numpy array form
Intended for faster processing in MMCQ algorithm, also converting data to one standard (RGB uint8)



## def DEV_draw_palette(RGB_pal: List[List[int]], cube_side: int = 2, cube_interval: int = 1, bg_col: List[int] = [255, 255, 255], scale_size: int = 50) -> np.ndarray:
**USED FOR DEVELOPMENT NEEDS: IF YOU DON'T KNOW WHAT YOU'RE DOING, DON'T TOUCH IT.
NOT ACCESIBLE THROUGH THE STANDARD IMPORT STATEMENT**
***Palette preview algorithm.***
:param RGB_pal: *list of lists of colors in RGB uint8 format ([[5,5,5],[6,6,6],[7,7,7]] for example)*
:param cube_side: *defines cube's side*
:param cube_interval: *defines interval between cubes and surroundings*
:param bg_col: *color of a background of the image [255, 255, 255] means white*
:param scale_size: *a parameter, on which the drawing will be scaled after creating palette with nearest neighbourhood interpolation*
Output:
An image of the palette in numpy array form
Intended for saving on hard drive via skimage.io.imsave method



## def DEV_comp_palette_with_picture(img: np.ndarray, RGB_palette: List[List[int]]) -> np.ndarray:
**USED FOR DEVELOPMENT NEEDS: IF YOU DON'T KNOW WHAT YOU'RE DOING, DON'T TOUCH IT.
NOT ACCESIBLE THROUGH THE STANDARD IMPORT STATEMENT**
***Composes given image with palette.***
Input:
:param img: *a image in numpy array form*
:param RGB_palette: *list of lists of colors in RGB uint8 format ([[5,5,5],[6,6,6],[7,7,7]] for example)*
Output:
Will output an image, which will contain given image and palette in numpy array form
Intended for saving on hard drive via skimage.io.imsave method


