# SAR Aircraft Detection Dataset
## Data Description
Since there is no publicly available aircraft detection dataset in SAR images, we collect and construct an aircraft slice dataset to investigate the detection performance of our method. We name the SAR aircraft detection dataset SADD and make it public to facilitate the research of other scholars. The SADD is collected from the German TerraSAR-X satellite, which working in x-band and HH polarization mode with image resolutions ranging from 0.5m to 3m. The ground truth of aircraft are manually annotated by SAR ATR experts according to the priori knowledge and corresponding optical images. After cropping the large images, 2966 nonoverlapped 224×224 slices are collected with 7835 aircraft targets, of which structures, outlines and main components are clear. The distributions of bounding boxes’ sizes in pixels and aspect ratios are shown in  (a), (b), respectively. Aircraft targets in SADD have various sizes, and there are a large number of small-size targets.
![image](https://user-images.githubusercontent.com/100459825/155867948-96e7b34b-9e59-4941-8b88-6f4d4935212a.png)
## Example
The target background of SADD is relatively complex, including various scenes such as airport runway, airport apron, and civil aviation airport. The negative samples are mostly around the airport, including open space and forest, etc. The picture shows the sample images in SADD.

<div align=center>
<img src="https://user-images.githubusercontent.com/100459825/155868013-55f34875-0e2d-4508-bd97-8f982775c40a.png">
</div>

## Label format
We use yolo-format for our labels, as shown bellow:

`<object-class> <x_center> <y_center> <width> <height>`

 Where:

- `<object-class>` - integer object number from `0` to `(classes-1)`
- `<x_center> <y_center> <width> <height>` - float values **relative** to width and height of image, it can be equal from `(0.0 to 1.0]`
- for example: `<x> = <absolute_x> / <image_width>` or `<height> = <absolute_height> / <image_height>`
- attention: `<x_center> <y_center>` - are center of rectangle (are not top-left corner)

  For example for `img1.jpg` you will be created `img1.txt` containing:

  ```csv
  0 0.716797 0.395833 0.216406 0.147222
  0 0.687109 0.379167 0.255469 0.158333
  0 0.420312 0.395833 0.140625 0.166667
  ```
## Data download
BaiduYun:

        https://pan.baidu.com/s/1ALH9lWP0XtGAA5rhdXoKtA 
        Extraction Code: 

