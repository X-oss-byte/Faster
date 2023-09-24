fast-colors

Classes​

Class	Description
ColorHSL	This uses Hue values in "degree" format. So expect a range of [0,360]. Some other implementations instead uses radians or a normalized Hue with range [0,1]. Be aware of this when checking values or using other libraries.
ColorHSV	This uses Hue values in "degree" format. So expect a range of [0,360]. Some other implementations instead uses radians or a normalized Hue with range [0,1]. Be aware of this when checking values or using other libraries.
ColorLAB	CIELAB color space This implementation uses the D65 constants for 2 degrees. That determines the constants used for the pure white point of the XYZ space of 0.95047, 1.0, 1.08883. https://en.wikipedia.org/wiki/Illuminant_D65 These constants determine how the XYZ, LCH and LAB colors convert to/from RGB.
ColorLCH	CIELCH color spaceThis is a cylindrical representation of the CIELAB space useful for saturation operations This uses Hue values in "degree" format. So expect a range of [0,360]. Some other implementations instead uses radians or a normalized Hue with range [0,1]. Be aware of this when checking values or using other libraries. This implementation uses the D65 constants for 2 degrees. That determines the constants used for the pure white point of the XYZ space of 0.95047, 1.0, 1.08883. https://en.wikipedia.org/wiki/Illuminant_D65 These constants determine how the XYZ, LCH and LAB colors convert to/from RGB.
ColorPalette	Generates a color palette
ColorRGBA64	A RGBA color with 64 bit channels.
ColorScale	A color scale created from linear stops
ColorXYZ	XYZ color spaceThis implementation uses the D65 constants for 2 degrees. That determines the constants used for the pure white point of the XYZ space of 0.95047, 1.0, 1.08883. https://en.wikipedia.org/wiki/Illuminant_D65 These constants determine how the XYZ, LCH and LAB colors convert to/from RGB.
ComponentStateColorPalette	Creates a color palette for UI components
Histogram	For each possible color, this counts how many pixels in the source image match that color. If signifigantBits is less than 8, each channel (eg: red, green, blue) in each color is reduced to fit in significantBits. So for the default value of 5 significantBits colors are reduced from 8 bits per channel (0-255) to 5 (0-31). Colors that were previously distinct get combined together. If the image source has more than 2^32 pixels (eg: a square image 65536x65536 in size) of the same color this code will break.
ImageDataPixelBlob	A PixelBlob implementation from an ImageData object.
PixelBox	Represents a range of colors in RGB color space.
Enumerations​

Enumeration	Description
ColorBlendMode	Color blend modes.
ColorInterpolationSpace	Color interpolation spaces
Functions​

Function	Description
blend(mode, bottom, top)	Blend two colors.
blendBurn(bottom, top)	Blends two colors with the burn mode
blendBurnChannel(bottom, top)	
blendColor(bottom, top)	Blends two colors
blendDarken(bottom, top)	Blends two colors with the darken mode
blendDarkenChannel(bottom, top)	
blendDodge(bottom, top)	Blends two colors with the dodge mode
blendDodgeChannel(bottom, top)	
blendLighten(bottom, top)	Blends two colors with the lighten mode
blendLightenChannel(bottom, top)	
blendMultiply(bottom, top)	Blends two colors with the multiply mode
blendMultiplyChannel(bottom, top)	
blendOverlay(bottom, top)	Blends two colors with the overlay mode
blendOverlayChannel(bottom, top)	
blendScreen(bottom, top)	Blends two colors with the screen mode
blendScreenChannel(bottom, top)	
calculateOverlayColor(rgbMatch, rgbBackground, rgbOverlay)	Calculate an overlay color that uses rgba (rgb + alpha) that matches the appearance of a given solid color when placed on the same background
centeredRescale(input, config)	Takes an input array of colors and extrapolates them to a larger palette. The mapping first takes the input array and extrapolates between each color so that they are separated by spacing-1 slots. Then it adds to either end enough new colors to make up the desired targetSize. All output color slots between the defined stops are interpolated.
clamp(i, min, max)	Ensures that an input number does not exceed a max value and is not less than a min value.
computeAlphaBlend(bottom, top)	Alpha channel of bottom is ignored The returned color always has an alpha channel of 1 Different programs (eg: paint.net, photoshop) will give different answers than this occasionally but within +/- 1/255 in each channel. Just depends on the details of how they round off decimals
contrastRatio(a, b)	Calculate the contrast ratio between two colors. Uses the formula described by WCAG 2.0.
darkenViaLAB(input, amount, darkenConstant)	Darken a color using LAB color space
degreesToRadians(i)	Converts degrees to radians.
denormalize(i, min, max)	Scales a number between 0 and 1
desaturateViaLCH(input, saturation, saturationConstant)	De-saturate a color using LCH color space
extractPalette(colors, config)	Extracts a palette.
generateOffCenterPalette(input, outputSteps, greyscaleConfig, colorConfig)	Generates a greyscale palette using greyscaleConfig. The Lightness (in HSL) of the input color is then compared to the greyscale palette to determine how far off center the input color should be placed. The output palette is then generated with outputSteps number of steps using colorConfig.
generateScaledPalettes(input, shortPaletteLength, config)	Generates two palettes of length shortPaletteLength and longPaletteLength from a base color. The base color is compared to the default greyscale palette to determine where it should be placed. The short palette is then fed into centeredRescale to create the long palette. The colors in the short palette are always contained within the long.
getHexStringForByte(i)	Converts a number between 0 and 255 to a hex string.
hslToRGB(hsl, alpha)	Converts a ColorHSL to a ColorRGBA64
hsvToRGB(hsv, alpha)	Converts a ColorHSV to a ColorRGBA64
insertIntoSortedList(list, newItem, sortPriority)	Adds a newItem to an already sorted list without needing to do a full re-sort. Higher sort priority puts the newItem closer to the start (index 0) of the list.
interpolateByColorSpace(position, space, left, right)	Interpolate by color space
interpolateHSL(position, left, right)	Interpolate by HSL color space
interpolateHSV(position, left, right)	Interpolate by HSV color space
interpolateLAB(position, left, right)	Interpolate by LAB color space
interpolateLCH(position, left, right)	Interpolate by LCH color space
interpolateRGB(position, left, right)	Interpolate by RGB color space
interpolateXYZ(position, left, right)	Interpolate by XYZ color space
isColorNamed(raw)	Tests whether a color is in NamedColors.
isColorStringHexARGB(raw)	Test if a color matches #AARRGGBB or #ARGB
isColorStringHexRGB(raw)	Test if a color matches #RRGGBB or #RGB
isColorStringHexRGBA(raw)	Test if a color matches #RRGGBBAA or #RGBA
isColorStringWebRGB(raw)	Test if a color matches rgb(rr, gg, bb)
isColorStringWebRGBA(raw)	Test if a color matches rgba(rr, gg, bb, aa)
labToLCH(lab)	Converts a ColorLAB to a ColorLCH
labToRGB(lab, alpha)	Converts a ColorLAB to a ColorRGBA64
labToXYZ(lab)	Converts a ColorLAB to a ColorXYZ
lchToLAB(lch)	Converts a ColorLCH to a ColorLAB
lchToRGB(lch, alpha)	Convert a ColorLCH to a ColorRGBA64
lerp(i, min, max)	Linearly interpolate
lerpAnglesInDegrees(i, min, max)	Linearly interpolate angles in degrees
lerpAnglesInRadians(i, min, max)	Linearly interpolate angles in radians
lightenViaLAB(input, amount, darkenConstant)	Lighten a color using LAB color space
loadImageData(source)	Creates an HTMLImageElement and loads the source argument as its src. Then an HTMLCanvasElement is created and the image is copied into the canvas. The pixel data is then returned from the CanvasRenderingContext2D for that canvas.
matchLightnessIndex(input, reference)	Takes the input color and compares it to each color in the reference array to find the index with the closest Lightness value in HSL color space
normalize(i, min, max)	Scales an input to a number between 0 and 1
parseColor(raw)	Expects any of the following and attempts to determine which is being used #RRGGBB, #AARRGGBB, rgb(RR,GG,BB) rgba(RR,GG,BB,a), or any of the CSS color names.
parseColorHexARGB(raw)	Converts a hexadecimal color string to a ColorRGBA64.
parseColorHexRGB(raw)	Converts a hexadecimal color string to a ColorRGBA64.
parseColorHexRGBA(raw)	Converts a hexadecimal color string to a ColorRGBA64.
parseColorNamed(raw)	Converts a named color to a ColorRGBA64.
parseColorWebRGB(raw)	Converts a rgb color string to a ColorRGBA64.
parseColorWebRGBA(raw)	Converts a rgba color string to a ColorRGBA64.
quantize(source, config)	The image stored in the source PixelBlob is reduced down to a small set of colors. Based on the Modified Median Cut Quantization implementation from https://github.com/DanBloomberg/leptonica/blob/master/src/colorquant2.c
quantizeHistogram(histogram, config)	The data in the color histogram is reduced down to a small set of colors. It can be useful to create the Histogram manually in cases where one wants to remove or alter the colors in it or to re-use it in order to quantize multiple times with different config settings. Based on the Modified Median Cut Quantization implementation from https://github.com/DanBloomberg/leptonica/blob/master/src/colorquant2.c
radiansToDegrees(i)	Converts radians to degrees.
rescale(input, targetSize, preserveInputColors)	Take the input array of colors and extrapolates them to a larger palette of size targetSize. If preserveInputColors is false the input colors are evenly distributed into the output. Otherwise, the positions of the input colors are adjusted from a perfectly even distribution in order to ensure that the exact color values appearing in the input array also appear in the output array. The larger targetSize is compared to input.length the smaller those adjustments will be.
rgbToHSL(rgb)	Converts a ColorRGBA64 to a ColorHSL
rgbToHSV(rgb)	Converts a ColorRGBA64 to a ColorHSV
rgbToLAB(rgb)	Converts a ColorRGBA64 to a ColorLAB
rgbToLCH(rgb)	Convert a ColorRGBA64 to a ColorLCH
rgbToLinearLuminance(rgb)	Get the luminance of a color in the linear RGB space. This is not the same as the relative luminance in the sRGB space for WCAG contrast calculations. Use rgbToRelativeLuminance instead.
rgbToRelativeLuminance(rgb)	Get the relative luminance of a color. Adjusts the color to sRGB space, which is necessary for the WCAG contrast spec. The alpha channel of the input is ignored.
rgbToTemperature(rgb)	Convert a rgb color to a color temperature
rgbToXYZ(rgb)	Converts a ColorRGBA64 to a ColorXYZ
roundToPrecisionSmall(i, precision)	Will return infinity if i*10^(precision) overflows number note that floating point rounding rules come into play here so values that end up rounding on a .5 round to the nearest even not always up so 2.5 rounds to 2
saturateViaLCH(input, saturation, saturationConstant)	Saturate a color using LCH color space
temperatureToRGB(tempKelvin, alpha)	Converts a color temperature to a ColorRGBA64
xyzToLAB(xyz)	Converts a ColorXYZ to a ColorLAB
xyzToRGB(xyz, alpha)	Converts a ColorXYZ to a ColorRGBA64
Interfaces​

Interface	Description
CenteredRescaleConfig	
ColorPaletteConfig	
ColorRGBA64Config	Configuration object for ColorRGBA64
ColorScaleStop	
ComponentStateColorPaletteConfig	Configuration for ComponentStateColorPalette
PaletteEntry	
PaletteEntryConstraint	
PaletteExtractionConfig	Configuration structure for palette extraction.
PixelBlob	Represents a blob of pixel data.
QuantizeConfig	A quantize configuration object.
QuantizedColor	A quantized color
Variables​

Variable	Description
defaultCenteredRescaleConfig	
defaultPaletteExtractionConfig	The default configuration for palette extraction.
defaultQuantizeConfig	The default quantize configuration.
Type Aliases​

Type Alias	Description
NamedColors	Browser named colors.
