# static-analysis-lab

Repository ini berisi hasil analisis terhadap beberapa file Portable Executable (PE) menggunakan metode dasar *static analysis* tanpa mengeksekusi program.

## 🎯 Tujuan
Melakukan identifikasi karakteristik dasar sebuah file PE untuk memahami informasi yang dapat diperoleh melalui proses *static analysis*.

## 🔬 Target Analisis
* **Steam** (`steam.exe`)
* **XAMPP** (`xampp_start.exe`)

## 🛠️ Metode Analisis
Analisis dilakukan menggunakan pendekatan *static analysis*, yaitu menganalisis file tanpa menjalankannya.
* **Tools yang digunakan:** Detect It Easy (DIE)

## 📊 Parameter Analisis
Setiap file akan dianalisis berdasarkan beberapa aspek berikut.

### 1. Hash
Mengidentifikasi nilai *hash* file sebagai *fingerprint* digital. Parameter yang dicatat:
* MD5
* SHA-1
* SHA-256

### 2. Tipe File
Mengidentifikasi karakteristik dasar *executable*. Informasi yang diamati:
* Format PE
* Architecture (x86/x64)
* Compiler
* Linker
* Packer (jika ada)

### 3. Strings
Mengidentifikasi *string* yang tersimpan di dalam *executable*. Contoh informasi yang dicari:
* URL
* Path
* Registry
* Nama DLL
* Pesan Error
* API Name

### 4. Import Table
Mengidentifikasi *library* (DLL) dan Windows API yang digunakan oleh *executable*. Contoh analisis:
* `Kernel32.dll`
* `User32.dll`
* `Advapi32.dll`
* `Ws2_32.dll`
* `Crypt32.dll`

### 5. Kesimpulan
Merangkum hasil analisis berdasarkan seluruh informasi yang diperoleh, seperti:
* Karakteristik *executable*
* Kemungkinan fungsi program
* Indikasi adanya *packer*
* API penting yang digunakan

## 📁 Struktur Repository
```text
static-analysis-lab/
├── docs/
│   ├── steam.md
│   └── xampp.md
├── Screenshots/
│   ├── steam/
│   └── xampp/
└── README.md
