# Airbus Ship Detection
## Required: 
Locate ships in images, and put an aligned bounding box segment around the ships you locate. Many images do not contain ships, and those that do may contain multiple ships. Ships within and across images may differ in size (sometimes significantly) and be located in open sea, at docks, marinas, etc.
## Dataset: 
https://www.kaggle.com/c/airbus-ship-detection/data
## Solution:
Library:
+ [tqdm 4.23.0](https://tqdm.github.io/): Hiển thị thanh xử lý quá trình (progress bar) khi chạy command line
+ [pandas 0.22.0](http://pandas.pydata.org/): Là thư viện trong việc xử lý dữ liệu, tính toán
+ [imageio 2.2.0](https://imageio.github.io/): Là thư viện đọc, ghi, chỉnh sửa các vùng hình ảnh, video
+ [pydot_ng 1.0.0](): Viêt, thực thi [DOT language](https://en.wikipedia.org/wiki/DOT_%28graph_description_language%29), là ngôn ngữ mô tả đồ họa biểu đồ của [Graphviz](https://www.graphviz.org)
+ opencv_python 3.4.0.12
+ torch 0.3.1
+ attrdict 2.0.0
+ scipy 1.0.0
+ scikit_image 0.13.1
+ numpy 1.14.0
+ imgaug 0.2.5
+ neptune-cli
+ ipython 6.3.1
+ Pillow 5.1.0
+ PyYAML 3.12
+ Cython 0.28.2
+ pycocotools 2.0.0
+ steppy 0.1.14
+ steppy-toolkit 0.1.12
+ [pretrainedmodels 0.7.0](https://github.com/Cadene/pretrained-models.pytorch): Huấn luyện tiếp tục (pre-train) các mô hình Convolutional Neural Networks 
+ [torchvision 0.2.0](https://pytorch.org/docs/stable/torchvision/index.html): Tập hợp gồm rất nhiều dataset, mô hình kiến trúc, các tập hình ảnh dùng trong thị giác máy tính 

