# MapAutocorrelationAnalyzer

MapAutocorrelationAnalyzer is a Python program for analyzing spatial autocorrelation in maps. It can calculate Moran's I and Geary's C indices and test their significance.

## Features

* Generate vector grid from RGB image
* Calculate Moran's I and Geary's C indices
* Test the significance of Moran's I and Geary's C indices
* Save results to a text file

## Usage

1. **Prepare the image**: Prepare an RGB regular-girdded image and save it as a .jpg file.
2. **Modify parameters**: (1) Modify the `img_path` variable to point to your image file path. (2)Change the variable N, which represents the length of the side of the image in pixels. (3) Change the palette variable, which represents the colormap for the image.
3. **Run the program**: Run the program. It will generate a vector grid, calculate the autocorrelation indices, perform significance tests, and save the results to a text file.

## Output

The program will output the following information:

* **Moran's I**: An index measuring spatial autocorrelation, with values ranging from -1 to 1. Positive values indicate positive autocorrelation, negative values indicate negative autocorrelation, and 0 indicates random distribution.
* **Geary's C**: An index measuring spatial autocorrelation, with values ranging from 0 to 2. Smaller values indicate stronger positive autocorrelation, while larger values indicate stronger negative autocorrelation.
* **Significance test**: Perform significance tests for Moran's I and Geary's C indices and provide p-values. Smaller p-values indicate more significant results.

## Notes

* The program uses the `libpysal` library for spatial weight matrix generation and ground truth test.
* The program uses a default black and white color scheme. You can modify the `palette` variable to use other color schemes.

## Examples

Suppose you have an image file named `example.jpg`, you can analyze it as follows:

1. Modify the `img_path` variable to `r"example.jpg"`.
2. Change the parameter settings.
3. Run the program.
4. The program will generate a text file named `example.txt` containing Moran's I, Geary's C indices, and significance test results.

## License

MapAutocorrelationAnalyzer is licensed under the MIT License.
