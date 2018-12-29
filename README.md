# Airbus Ship Detection
## Required: 
Locate ships in images, and put an aligned bounding box segment around the ships you locate. Many images do not contain ships, and those that do may contain multiple ships. Ships within and across images may differ in size (sometimes significantly) and be located in open sea, at docks, marinas, etc.
## Dataset: 
https://www.kaggle.com/c/airbus-ship-detection/data

<img src="https://lh3.googleusercontent.com/DHTqMHk9SSpbtLPepNTUP4CwNjRB59zgSru7-U4okjqpdfvivph8gvecFB0yge2I9k20OxqAECKuK0EWX36SboByL9NO8tbHVxoVTae0Jfr_qLEmfyhOKy-rptgjdkRVwToXFJzYRd2X2Yoiw2tKUOE-OOMSvy6OPNsIfDEqzkQ5GqU8qumWg6qzVDMYKNAOaVEGnryvMBBQExIHwm5UweJGQhk0yvKHQ26U_2MqWm7IZuTY-zdJ1pXIrm4xiOVQ4I6lJebTYCoxPvJ9fyFOPCQZV7dx9VNhjUMxZurnlLKmmosIOYTrJGUwWr1_dLZ48U4sPinZieVgi17G7p42D5OXJSsMi468r4hOjNBy80GC5Kc_JnovOhf9CLqWv-K_WAcGGk-2FAk4ldXVai79Hs32pclVCv43jkf3R_XhGi-VqrMV_a0AS5bEINPQLMpLb6NfOB7rOiHWsYQyKtA-7NcxEGNrqZkS-AfDYz8lDfXR5R677Tq2pxM-Eeiv19rkPOxLrQmHzxyo78hdUe8IC5TcvToEH3xuiWIRA7nYfVDZsprVCPfer__WRJpJif_n2ZSy1WP7-VU7c3jzQnEisQAsAag6MAiG-A2E-DTQZxF7s3LSuKvWZTt9ykqY10Q9-NPS_A-B_eV9QTwT3f9YpYxRm8dLe4cC1iqDBfxH2pznZcPMorVucng851vUfu18i9NuUJ-V91KCXqEjHg=s691-no" width="200"/> <img src="https://lh3.googleusercontent.com/oBhfWf0H2eI_Nf48MH4IUbVfFnLcqiJsQ8cLeAy00PQb9MqsAsI5uHCziML9rQqWwjLK_0ef_QRxHG-HKecvvxYD58LkINunycD043Hm9J9_iKU-XGWhL3STDRTZeVYzM7MrlYXE45_kS-x-o8oX7guIlOwNv4AheMPLZfBh91bOOUgMB_fl9YtX9m0ddmAv0zhcoQnQmahsu42O2ehiEQHsrd5DMAXuD-LbjCWfczEpyxyJ_QBhFybqfZ0Y7NddR37MREHY0k5AhBApyHYRqdwHZkoLVjfmFhf68jVgWsSKhJIPOIE5SmqxkTIAPPU86-8L8qBF4n6kzo3wVr3y0kVlE9FVQZhsNY6glRsEpdStp57ibpUtk-sGyfW8g3Tja19xGjc6TCJQRHq2teOb_ppRDmZzRVNBv7k55Eyeq55fQA-eWu7P_i587UARTUFLefg56Z7eGM3e7PGVSAfaEHs4cD4RtOq_MuTXW6k9B6gWoCSGk0_sfJvJm1AeBFtc0CKtk3TKq-Ygbbjt61-r3yFaSlLbJAQNuQ6E96m_snyt0JvPIx15dhI_GCBdQaDgOT1HAHcbXAKnObpIA_Xaj9NHeuTgvsKA6d-1A9sdP0B5-xaAElKpNK3sXnPz9UfaftflVYKX7J-F7WLzWmTg9vqbZoadWi7GEy1ZxT0YUuBneQFkfLeT0mCa04s-WtDDSt-o3uzSWCsqlDCniA=s691-no" width="200"/> <img src="https://lh3.googleusercontent.com/LVPMgbLu0Fb9AXpL2YXEtdFrXqh9iWaGpCAaZVCQVVT-I1FmiOqx8ijvkHS_FD14gYdFQyLOlkYe0nor4X72bMHDgaLIDqo9HTw6LYkC9T4rBVpfvMcVDVBrsNKmgLYlZv9yL8cjhtJuGVKRfoZBDX4U6XrQor-y8RCjN2Qo5FxkwRy2gcAW1Xz7wNvDvFAWmvMZ03PgHPPtfbxtvD0wcHdiyLr0l62ujS3K3MFa1XaCUlmtA7PJCXvqYFMsldrxvpZGt-4rVjkt7T9KMZjH98FgGfoFhDLMpHIjLBNb5EVjWTQEaca_7z5UfzG-b_coYadMVvK4K-tcoIgDDLmyM41-qkEFDYspB28fjMbria49k8FmFEzwazb1DZ_hF_YFrnoxtO34FL6dKG9b6rMT_a3bG-sfLqZFspidQ7hiyP_NTMk2BCTV9wen7mQKIlycgOn34Wjso2IBEtQ4-Nmjv6Bz5Z8UKWVAtGv7XykFVJMtxIOizsMOAaeBimbwYVlomY1bjyOcyT7KITRMjn2GRGGz5Bq7s9QNDLpPriBMJB0je2hw59SfNAED2MNinxwLjpuSYQBZoDItw6uO4mmyPEdGM_9YS1D-nMA1My6nkxs5CxfnvRXiMCmHn1UkqD4_9BAHO6huzMnnAAJK-iPRnOEcoGADq8Rm8pZqF568r4ggXySGfksczNnLSXHWybf20s_OP55QCA3i1LYc7w=s691-no" width="200"/> <img src="https://lh3.googleusercontent.com/X7Bo0hwMWU78GS1MN0sCAlSFauXXxpGD3zcHKTaCw1Y-0WPAQO7bE5Sc_FD4diSkZMt7QpiQWvJn7lrj7ugfGoxMBcX-m_84EKWzNfDB8IRlwMff8_7XKpYLYfTyZ4Kbyp50YMLPkPoCXW84V6ErPs7giiV0QY_GZ6nhzSoc8lm9H9r6SkuVBM6RGw9-b61ZOkSq_D8fDrrFbLGU35rkGoZjqf4cPQY-EQ4465suUWVptDY6HY7xv8LuWTs8YvWbWKCzqHOcbIg64IndulPh7J6MpolYRoeepNbC8qa-lbB7apZIjgzzAB6WQYSE6Jiqy9YMGpejsX3F_pg203ZtLpkCVy9xnBQ-NVclZF0yf3YvuPSzkwdulSYIl8PoK2B2WB0JmtndPrhdptUOpxXCXGwjmxpGEISrgYnUK_aNAhnpmTAbsLdsRLUFEfqBYv1c2WS9MS10DJP6YzX30a5xvgAq6kBl7q7Rz05hnZcmCZxuloxiF-VhdbtQd2ZNEdzP8IWsin071OLfU4Lh5oCJsKlg9Bg7WBAH7fpLNwVcTjvrIqSfM6aH8Nl61fmmkYW9oqI2iWr3v-oED1bd5r6ZHyY10p5nJWKZfsxcKrQ09klbs3vkbc1GliWSgh2T80yi3BVHPn8xye58qrMsNn44LY65ES53_-5EMk3c_-Eb2u8ZfT-aVqAtM1EDqz7ncSMLKah70ilaZEi3b9dQ5g=s691-no" width="200" /> <img src="https://lh3.googleusercontent.com/v9ScBTuLDTnGpZ4HzNpQkXuHrUbunOBONglZtid6Ol834WVo2dYwIk9JVn33kxR2XnwQQmoY6YJicU6eg_qKyzCflK3kOSV-YWcalNzJBu74n0D7vQXs_sBWHfCwjPPRttzmb-gMvRB8vZQqBvkAk8xnVzyV9AGt8nuSZScyNcfcKLI0KLZ_L-aZ9_STRrj8-eYij6eOsqtL1tBgyWobDNQmPngC5DLHUh_x9meOgIHdR8CGG8rOzSxKh6EPLB1SXlRtdiqcoH-__h64y14mgVYFAjBEqCmALw-kh4xT4dOxpnFQ8SRf4f7dHxYhf7bbCJjK-yRHJy2bvkowY8G9i5b-DJvMdk6QnpQ0m0gcSOCNX7eJIuYSTnH6QLBM3n8j5pOr8eGAOQu9IPKQQ2IpKbMRm4DmO4G4AtDM8o6_G3l7YeBDTEZW_5yIAizew3NsKtGcHW_gZm44xg6rfICP-9rgFajJ8Pg63G2nuLbfnQp8S4ud0yWaFi9SLgbUf0mJ4BSWP06tcuuJBhu5n_712F3pY3cXL4VPZIJznlG85SK3Qw9V0d8iSZR7UW9nTrHcIxizVg38_tk-2UHQE-3JxGRnRc8O2lPl3RypFFvwyrR7cVGYRlt4gdqFb89-hbqnk-i1ylmhMt_KSQtlx7SyL6_cGiX2QMICxGUTh9pBd8iNKtW4jKuf6NjakNB7sRAzZHwsNRQ_ycx42NKeFA=s691-no" width="200"/> <img src="https://lh3.googleusercontent.com/Ek_ovVa-sBBfPlrpLQNyxxVc_viZy8_RsXuvkEpahVCF0yA-5yVNOp--ICZSCn3n8uuSBfeU0XYqjxsX65kblNb9zXro8VQvpNhB6hRnEMzMYVUa8DFy92MnkTG-C7z4_7-lkX5kGR5Eqch8c5XHTXDn0dJ5k-9YCb-BGfhxz6dFbTlTsli6ZRIhkODFmpXQY3d_r0MwErZQpAogtjvpXZHIrAMKO9w-jN6lOTJ08LAkDhJGDYSj9_zonkAdCX5sdffuW6V2Z5tz45XLShjr7ayi0-OYyAsLc1wppXe8Xbm88gShDTH8Ovg7a-k7BU3g6N_-V587vCsqr4TFAQav4_9rR0kTNp9_-CsiZqvmOCV8RBujjSARsrsaTZ5B62DVy4RJmNxL8VFGRGiakBzRG3SrqOtDFtx8oz_61lNq_fD_nN3GB3vAURi_MXiYdoYxX00M-oiA7OS7LChfwXlMePph5I5Gl7DM1NnSIO5DUp-JpPv11lsehZz-CCTZiWPz5_jQ1YDaXmPYESkJFt1McgHyu9nwThMABThIfm5M71FUL187RZU7qivGvox4XBMEechRdspxfOjDS_fmOT211aIpak0HSD3MjKYCI7Jesm7u5I0--8y_Zr6GhStTay-sRIc92D8mobjufDwD1ru2VvxHLmaLj2WDcLLIybMXEmI1ZoCpUMrD8_r6FRMbJm6Z2BNzKll4gjATkaidRg=s691-no" width="200" />

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
+ [PyYAML 3.12](https://pyyaml.org/wiki/PyYAML): Sử dụng cú pháp của [YAML](https://yaml.org/) trong Python 
+ [Cython 0.28.2](https://cython.org/): Là một thư viện mở rộng cú pháp và kiểu dữ liệu C trong Python
+ pycocotools 2.0.0
+ [steppy 0.1.14](https://github.com/neptune-ml/steppy): Tập trung vào tính toán khoa học dữ liệu, [steppy xamples](https://github.com/neptune-ml/steppy-examples)
+ [steppy-toolkit 0.1.12](https://github.com/neptune-ml/steppy-toolkit): Cải tiến bổ sung của steppy
+ [pretrainedmodels 0.7.0](https://github.com/Cadene/pretrained-models.pytorch): Huấn luyện tiếp tục (pre-train) các mô hình Convolutional Neural Networks 
+ [torchvision 0.2.0](https://pytorch.org/docs/stable/torchvision/index.html): Tập hợp gồm rất nhiều dataset, mô hình kiến trúc, các tập hình ảnh dùng trong thị giác máy tính 

