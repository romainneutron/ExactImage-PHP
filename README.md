#ExactImage PHP documentation

As ExactImage bindings for PHP are not well documented, here's an attempt to
share an API doc.

##Functions

```php
<?php
newImage();

newImageWithTypeAndSize($samplesPerPixel, $bitsPerSample, $width, $height, $fill = 0);

deleteImage($image);

copyImage($image);

copyImageCropRotate($image, $x, $y, $w, $h, $angle);

decodeImage($image, $data);

decodeImageFile($image, $filename);

encodeImage($image, $codec, $quality = 75, $compression = "");

encodeImageFile($image, $filename, $quality = 75, $compression = "");

imageChannels($image);

imageChannelDepth($image);

imageWidth($image);

imageHeight($image);

imageColorspace($image);

imageXres($image);

imageYres($image);

imageSetXres($image, $xres);

imageSetYres($image, $yres);

get($image, $x, $y);

set($image, $x, $y, $r_, $g, $b, $a = 1.0);

imageConvertColorspace($image, $target_colorspace, $threshold = 127);

imageResize($image, $x, $y);

imageRotate($image, $angle);

imageFlipX($image);

imageFlipY($image);

imageScale($image, $factor, $yfactor = .0);

imageNearestScale($image, $factor, $yfactor = .0);

imageBoxScale($image, $factor, $yfactor = .0);

imageBilinearScale($image, $factor, $yfactor = .0);

imageThumbnailScale($image, $factor, $yfactor = .0);

imageCrop($image, $x, $y, $w, $h);

imageFastAutoCrop($image);

// throws a fatal error if you pass an integer instead of float
setForegroundColor(float $r, float $g, float $b, float $a = 1.0);

// throws a fatal error if you pass an integer instead of float
setBackgroundColor(float $r, float $g, float $b, float $a = 1.0);

imageNormalize($image);

imageInvert($image);

imageBrightnessContrastGamma($image, $brightness, $contrast, $gamma);

imageHueSaturationLightness($image, $hue, $saturation, $lightness);

setLineWidth($width);

imageDrawLine($image, $x, $y, $x2, $y2);

imageDrawRectangle($image, $x, $y, $x2, $y2);

newPath();

deletePath($path);

pathClear($path);

pathMoveTo($path, $x, $y);

pathLineTo($path, $x, $y);

pathCurveTo($path, $x, $y, $x2, $y2);

pathQuadCurveTo($path, $x, $y, $x2, $y2, $x3, $y3);

pathClose($path);

pathStroke($path, $image);

pathFill($path, $image);

imageDrawText($image, $x, $y, $text, $height, $fontfile = null);

imageDrawTextOnPath($image, $path, $text, $height, $fontfile = null);

imageOptimize2BW($image, $low = 0, $high = 255, $threshold = 170, $radius = 3, $standard_deviation = 2.3, $target_dpi = 0);

imageIsEmpty($image, $percent, $margin);

imageDecodeBarcodes($image, $codes, $min_length = 0, $max_length = 0, $multiple = 0, $line_skip = 8, $directions = 0xf);

newContours($image, $low = 0, $high = 0, $threshold = 0, $radius = 3, $standard_deviation = 2.1);

deleteContours($contours);

newRepresentation($logo_contours, $max_feature_no = 10, $max_avg_tolerance = 20, $reduction_shift = 3, $maximum_angle = 0.0, $angle_step = 0.0);

deleteRepresentation($representation);

matchingScore($representation, $image_contours);

logoAngle($representation);

logoTranslationX($representation);

logoTranslationY($representation);

inverseLogoTranslationX($representation, $image);

inverseLogoTranslationY($representation, $image);

drawMatchedContours($representation, $image);
```

##License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">
    <img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/3.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">Creative Commons Attribution-ShareAlike 3.0 Unported License
</a>.

