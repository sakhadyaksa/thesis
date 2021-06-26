# Deteksi Imunoreaktivitas Ki-67 pada Glioma dengan Pendekatan Deep Learning Berbasis Mask Region-Based Convolutional Neural Network (Mask R-CNN) - Dewa Datara Nyoman Murti Adyaksa - m32
![image](https://user-images.githubusercontent.com/83645352/123502805-3ac04c80-d679-11eb-90b5-bda295f920e8.png)
The code is an implementation of modified Mask R-CNN algorithm to perform object detection, localization, classification and instance segmentation of glioma tumor cells stained with Ki-67 immunohistochemistry. Several experiment were conducted and the model best performed with 512x512 spatial dimension training data, 0.001 learning rate, 10 epochs, small RPN anchors, 512 px slider with ResNet 101 + FPN backbone harnesing 13 GB K80 nVidia Tesla GPU. High resolution image for training purpose is not recommended. Transfer learning performed utilizing pre-trained weight with MS COCO dataset. Model accuracy is not yet generalized and or externally validated with inter-institution dataset. Pixel-perfect accuracy were achieved with average IoU of 0.75. The code is ideal for pathology images application. Primary image data were retrieved from single-field image sensor and manually annotated by a training pathologist. There were no pre-processing deployed in the pipeline except to extract 512x512 hotspot region from the given high resolution images data.

  # Pembimbing:
    Ir. Hanung Adi Nugroho, Ph.D, IPM - Departemen Teknik Elektro dan Teknologi Informasi Fakultas Teknik Universitas Gadjah Mada
    dr. Ery Kus Dwianingsih, Ph.D, Sp.PA(K)
  # Penguji:
    Dr. dr. Ahmad Ghozali, Sp.PA(K)
    dr. Rusdy Ghazali Malueka, Ph.D, Sp.N(K)
Tesis ini telah dipertahankan dalam ujian akhir yang dilaksanakan pada 25 Juni 2021 di ruang virtual Fakultas Kedokteran, Kesehatan Masyarakat dan Keperawatan (FK-KMK) Universitas Gadjah Mada.

Terima kasih yang tidak terhingga teruntuk pada pembimbing (dr. Ery Kus Dwianingsih, Ph.D, Sp.PA(K), Ir. Hanung Adi Nugroho, S.T, M.E, Ph.D, IPM) dan penguji (Dr. dr. A. Ghozali, Sp.PA(K), dr. Rusdy G. Malueka, Ph.D, Sp.S(K)) yang telah dengan sabar menuntun penelitian ini.
# Credit:
Many thanks to David Revelo Luna, Adam Kelly, Waleed Abdulla and Matterport, Inc. for providing the source code I have adapted and modified to suit my research objectives:

    Matterport, Inc
    https://github.com/matterport

    Adam Kelly
    https://github.com/akTwelve
    
    David Revelo Luna
    https://github.com/DavidReveloLuna
