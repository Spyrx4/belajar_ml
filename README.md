# Panduan Instalasi Virtual Environment

Repository ini berisi environment configuration untuk project belajar machine learning. Ikuti langkah-langkah berikut untuk setup environment.

## Prerequisites

Pastikan Anda sudah menginstall:

- Anaconda atau Miniconda ([Download di sini](https://www.anaconda.com/download))
- Git

## Step-by-Step Instalasi

### 1. Clone Repository

```bash
git clone https://github.com/belajar_ml/belajar_ml.git
cd belajar_ml
```

### 2. Buat Virtual Environment dari File `mlenv.yml`

```bash
conda env create -f mlenv.yml
```

Perintah ini akan:

- Membaca konfigurasi dari file `mlenv.yml`
- Membuat environment baru dengan nama yang sudah ditentukan di file
- Menginstall semua dependencies yang tercantum

### 3. Aktivasi Virtual Environment

**Windows:**

```bash
conda activate mlenv
```

**macOS/Linux:**

```bash
conda activate mlenv
```

_Note: Nama environment `mlenv` disesuaikan dengan nama yang ada di file `mlenv.yml`. Jika berbeda, sesuaikan dengan nama yang tertera._

### 4. Verifikasi Instalasi

Untuk memastikan environment sudah terinstall dengan benar:

```bash
conda env list
```

Atau cek package yang terinstall:

```bash
conda list
```

## Deaktivasi Virtual Environment

Jika sudah selesai bekerja dan ingin keluar dari environment:

```bash
conda deactivate
```

## Update Environment

Jika ada perubahan pada file `mlenv.yml`, update environment dengan:

```bash
conda env update -f mlenv.yml --prune
```

## Hapus Environment

Jika perlu menghapus environment:

```bash
conda env remove -n mlenv
```

## Troubleshooting

### Error: "CondaValueError: prefix already exists"

Environment sudah ada. Hapus dulu environment lama:

```bash
conda env remove -n mlenv
conda env create -f mlenv.yml
```

### Error: "PackagesNotFoundError"

Update conda terlebih dahulu:

```bash
conda update conda
conda env create -f mlenv.yml
```

### Conda command not found

Pastikan Anaconda/Miniconda sudah terinstall dan PATH sudah dikonfigurasi dengan benar.

## Export Environment (Opsional)

Jika Anda menambah package baru dan ingin update file `mlenv.yml`:

```bash
conda env export > mlenv.yml
```

Atau export tanpa build specifications:

```bash
conda env export --no-builds > mlenv.yml
```

## Catatan

- Selalu aktivasi environment sebelum menjalankan program
- Jangan install package di base environment, gunakan environment khusus
- Backup file `mlenv.yml` jika melakukan perubahan

## Kontak

Jika ada pertanyaan atau masalah, silakan buat issue di repository ini.
