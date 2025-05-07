# 📧 Intelligent Email Writer for Students

Proyek ini merupakan aplikasi berbasis Web yang memungkinkan mahasiswa membuat email secara otomatis dan profesional dengan bantuan teknologi Large Language Model (LLM) dari **Gemini API**. Aplikasi ini dirancang khusus untuk membantu mahasiswa dalam menyusun email profesional untuk berbagai keperluan akademik.

## 📋 Daftar Isi
- [📦 Fitur Utama](#-fitur-utama)
- [🖥️ Demo Aplikasi](#-demo-aplikasi)
- [📁 Struktur Proyek](#-struktur-proyek)
- [⚙️ Instalasi dan Menjalankan Proyek](#-instalasi-dan-menjalankan-proyek)
- [🔐 Konfigurasi API Key Gemini](#-konfigurasi-api-key-gemini)
- [📬 Panduan Penggunaan](#-panduan-penggunaan)
- [🛠️ Teknologi yang Digunakan](#-teknologi-yang-digunakan)
- [📝 Lisensi](#-lisensi)

## 📦 Fitur Utama

- **Kategori Email yang Beragam**: Akademik, Skripsi, Magang/MBKM, Beasiswa, Organisasi, Karier, dan lainnya.
- **Fleksibilitas Gaya Penulisan**: Formal, netral, atau santai sesuai kebutuhan.
- **Dukungan Multibahasa**: Mendukung Bahasa Indonesia dan Inggris.
- **Penyesuaian Konten**: Menentukan poin-poin utama yang ingin disampaikan dalam email.
- **Tingkat Urgensi**: Opsi untuk menentukan prioritas email.
- **Referensi**: Dapat menggunakan contoh email sebelumnya sebagai acuan.
- **Hasil yang Profesional**: Menghasilkan email yang terstruktur, jelas, dan sesuai konteks.

## 🖥️ Demo Aplikasi

Berikut adalah **detail pengisian form** yang bisa kamu masukkan ke dalam `README.md` sebelum menampilkan screenshot antarmuka aplikasi:

---

### Tampilan Utama
![image](https://github.com/user-attachments/assets/729b82f6-fd4b-4588-90e7-c3f945a07a8a)

### Contoh Penggunaan untuk Email Beasiswa/Exchange
### 📄 Contoh Pengisian Form: Intelligent Email Writer for Students
* **Kategori Email:**
  `Beasiswa / Exchange`
* **Kepada:**
  `Yth. Bapak/Ibu Dosen Pembimbing Akademik`
* **Subjek Email:**
  `Permohonan Surat Rekomendasi untuk Program Exchange ke Thailand`
* **Gaya/Tone Penulisan:**
  `Formal dan Sopan`
* **Bahasa:**
  `Bahasa Indonesia`
* **Tingkat Urgensi:**
  `Segera`
* **Poin-poin Utama Isi Email:**
  ```
  - Nama saya Pryta Rosela dengan NPM 2208107010046
  - Saya ingin mendaftar program pertukaran pelajar ke Jepang yang diselenggarakan oleh universitas chula
  - Dibutuhkan surat rekomendasi dari dosen pembimbing
  - Batas pengumpulan dokumen adalah tanggal 15 Mei 2025
  - Saya telah menyiapkan draft dokumen pendukung dan CV
  - Mohon kesediaan Bapak/Ibu untuk memberikan surat rekomendasi
  ```
* **Contoh Email Sebelumnya (Opsional):**
  *(Tidak diisi)*
  
![image](https://github.com/user-attachments/assets/0579bede-02f7-4bda-90f5-d01a66dc22f0)

### Hasil Generate Email Beasiswa/Exchange
![image](https://github.com/user-attachments/assets/432dd003-adb0-4e1f-bffb-88fba33456bd)


## 📁 Struktur Proyek

```
intelligent_email_writer/
├── .env                    # Berisi API Key Gemini
├── app.py                  # Frontend dengan Streamlit
├── backend/
│   └── main.py             # Backend API menggunakan FastAPI
├── requirements.txt        # Dependensi backend
└── README.md               # Dokumentasi proyek
```

## ⚙️ Instalasi dan Menjalankan Proyek

### 1. Kloning repository

```bash
git clone https://github.com/prytarosela/UAS_PrytaRosela_2208107010046.git
cd UAS_PrytaRosela_2208107010046
```

### 2. Setup dan jalankan Backend (FastAPI)

```bash
# Buat dan aktifkan environment
python3 -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows

# Install dependencies
pip install -r requirements.txt

# Jalankan server
uvicorn backend.main:app --reload --host 0.0.0.0 --port 8000
```

### 3. Setup dan jalankan Frontend (Streamlit)

Buka terminal baru:

```bash
# Pastikan sudah berada di direktori project dan environment aktif
streamlit run app.py
```

## 🔐 Konfigurasi API Key Gemini

1. Buka [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Klik **Create API Key**.
3. Copy API key dan simpan ke dalam file `.env` di root project dengan format:

```env
GEMINI_API_KEY=your_api_key_here
```

### Troubleshooting Konfigurasi API Key

Jika mengalami error terkait API key:

- Pastikan file `.env` berada di direktori yang sama dengan file `main.py`
- Periksa bahwa API key sudah valid dan aktif
- Pastikan variabel environment diangkat dengan benar menggunakan `load_dotenv()`
- Jika menggunakan model selain `gemini-2.0-flash`, sesuaikan konfigurasi di `main.py`

## 📬 Panduan Penggunaan

### Langkah-langkah Membuat Email

1. **Pilih Kategori Email** yang sesuai dengan kebutuhan Anda.
2. **Tentukan Penerima** email (contoh: Dosen Pembimbing, Koordinator Magang).
3. **Tulis Subjek** email yang jelas dan informatif.
4. **Pilih Gaya Penulisan** yang sesuai dengan konteks dan hubungan Anda dengan penerima.
5. **Pilih Bahasa** yang akan digunakan.
6. **Tentukan Tingkat Urgensi** jika diperlukan.
7. **Tulis Poin-poin Utama** yang ingin disampaikan (satu poin per baris).
8. **Tambahkan Contoh Email** sebelumnya jika ada (opsional).
9. **Klik tombol "Buat Email"** untuk menghasilkan email.
10. **Salin hasil** dan sesuaikan seperlunya.

### Tips Penggunaan

- Semakin detail poin-poin yang dimasukkan, semakin sesuai hasil yang akan dihasilkan.
- Gunakan tingkat urgensi "Tinggi" hanya untuk email yang benar-benar mendesak.
- Selalu periksa kembali hasil generate sebelum mengirimkannya.

## 🛠️ Teknologi yang Digunakan

- **Frontend**: Streamlit
- **Backend**: FastAPI
- **LLM API**: Google Gemini 2.0 Flash
- **Environment Management**: python-dotenv
- **HTTP Client**: Requests

## 📝 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).

---

**Dibuat untuk UAS Praktikum Pembelajaran Mesin**
