# Panduan Menjalankan Project MLflow Training

Dokumen ini berisi langkah-langkah untuk menjalankan project training
model dengan MLflow.

## 1. Persiapan Lingkungan

Pastikan telah meng-install dependensi berikut:

``` bash
pip install -r requirements.txt
```

## 2. Struktur Project

    project/
    │── train.py
    │── requirements.txt
    │── datset.csv(disesuaikan)
    

## 3. Cara Menjalankan Training

Jalankan perintah berikut:

``` bash
python train.py
```

## 4. Hasil Training

MLflow akan otomatis membuat folder:

    mlruns/

Semua: - Parameter - Metric - Artifact - Model

akan tersimpan di dalam folder tersebut.

## 5. Menjalankan MLflow UI

Gunakan:

``` bash
mlflow ui
```

Akses dashboard melalui:

    http://127.0.0.1:5000

## 6. Mengubah File Dataset Secara Manual

Edit pada `config.py`:

``` python
DATA_PATH = "path_ke_dataset.csv"
```

## 7. Catatan

Jika menjalankan eksperimen baru, ubah nama experiment di file:

``` python
mlflow.set_experiment("nama_experiment_baru")
```
