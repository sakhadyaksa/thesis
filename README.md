#MaskerRCNN_Video

Dalam proyek ini kita akan membahas segmentasi semantik menggunakan MaskRCNN dalam gambar dan video. Repositori dasar untuk proyek ini adalah sebagai berikut. Yang pertama adalah implementasi untuk Tensorflow 1, dan repositori kedua memiliki pembaruan untuk Tensorflow 2.
Modifikasi dilakukan untuk menjalankan deteksi menggunakan webcam.

    https://github.com/matterport/Mask_RCNN
    https://github.com/akTwelve/Mask_RCNN

## Persiapan lingkungan

Kami akan menyiapkan lingkungan dengan python 3.7.7, Tensorflow 2.1.0 dan keras 2.3.1

    $ conda create -n MaskRCNN anaconda python = 3.7.7
    $ conda aktifkan MaskRCNN
    $ conda install ipykernel
    $ python -m ipykernel install --user --name MaskRCNN --display-name "MaskRCNN"
    $ conda install tensorflow-gpu == 2.1.0 cudatoolkit = 10.1
    $ pip instal tensorflow == 2.1.0
    $pip instal jupyter
    $pip install keras
    $ pip install numpy scipy Bantal cython matplotlib scikit-image opencv-python h5py imgaug IPython [all]
    
## Instal MaskRCNN

    $ python setup.py install
    $ pip install git + https: //github.com/philferriere/cocoapi.git#subdirectory=PythonAPI
    
## Uji di notebook Jupyter

    $cd sampel
    $buku catatan jupyter
    
## Tes konsol dengan gambar dan video

### Dengan Gambar

    $cd sampel
    $ python imagemask.py
    
### Dalam video

    $cd sampel
    $ python videomask.py
    
# Pelatihan dengan kumpulan data khusus
- Beri label kumpulan data dengan alat [VIAv1.0] (http://www.robots.ox.ac.uk/~vgg/software/via/via-1.0.0.html) (Lakukan dengan versi 1.0. 0)
- Simpan data validasi dan pelatihan di folder bernama train and val
- Simpan anotasi dari dua grup data dengan nama: via_region_data.json
- Jalankan di google collab file Casco.ipynb.

## Uji model terlatih dengan kumpulan data khusus

- UNTUK PENGUJIAN SISTEM DENGAN GAMBAR :
    
    Ubah parameter
    
    - model_filename = "mask_rcnn_casco_0050.h5" # Di sini Anda harus memuat model terlatih dengan dataset Anda
    - class_names = ['BG', 'casco'] # Kelas yang terkait dengan model BG Anda + kelas khusus
    - min_confidence = 0,6 # Tingkat kepercayaan minimum untuk menerima temuan sebagai positif
    
    $ python helm.py
        
- UNTUK PENGUJIAN SISTEM DI VIDEO:

    Ubah parameter
    
    - model_filename = "mask_rcnn_casco_0050.h5" # Di sini Anda harus memuat model terlatih dengan dataset Anda
    - class_names = ['BG', 'casco'] # Kelas yang terkait dengan model BG Anda + kelas khusus
    - min_confidence = 0,6 # Tingkat kepercayaan minimum untuk menerima temuan sebagai positif
    - kamera = cv2.VideoCapture (0) # Jika Anda ingin menjalankan webcam
    - camera = cv2.VideoCapture ("video.mp4") # Jika Anda ingin menjalankan video yang memuatnya dari PC Anda
    
    $ python cascoVideo.py
    

 
## Pelatihan kumpulan data khusus multikelas

 - Kelas Kustom.ipynb
 
## Persimpangan IoU di atas Union

- IoUTest.ipynb
 
# Terima kasih

    Matterport, Inc
    https://github.com/matterport

    Adam Kelly
    https://github.com/akTwelve
