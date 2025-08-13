# 🏆 Script Cek Address Menang (CREATOR by XBOOT)

Script ini digunakan untuk mengecek apakah alamat wallet kamu termasuk di daftar pemenang (winner list).  
Menggunakan **masking address** untuk mencocokkan, serta menampilkan hasil dalam tabel berwarna yang rapi.

## ✨ Fitur
- Banner **CREATOR by XBOOT** menggunakan `pyfiglet`
- Membaca **winner list** dan **daftar alamat kamu** dari file `.txt`
- Cocokkan berdasarkan 6 karakter awal dan 5 karakter akhir address
- Tabel hasil berwarna dengan `rich`
- Menampilkan jumlah address yang cocok

## 📦 Instalasi
Pastikan Python 3 sudah terinstall.  
Lalu install dependency:
```bash
pip install rich pyfiglet
```

## 📂 Struktur File
```
📁 cek-winner
 ├── cek_winner_xboot.py     # Script utama
 ├── winner_list.txt         # Daftar pemenang (masking)
 ├── my_addresses.txt        # Daftar address kamu
```

## 📝 Format File
**winner_list.txt** (alamat dengan masking, satu per baris):
```
0x4881****b2f0b
0x2beb****45e2fb
0x9bcc****8be598
```

**my_addresses.txt** (alamat full, satu per baris):
```
0x48811234567890abcdef1234567890b2f0b
0x9363abcdef9876543210abcdef96201964
```

## 🚀 Cara Menjalankan
1. Pastikan file `winner_list.txt` dan `my_addresses.txt` sudah ada di folder yang sama dengan script.
2. Jalankan di terminal:
```bash
python cek_winner_xboot.py
```

## 📊 Contoh Output
```
  ____ ____  _____  ____   ___   ___  _____ 
 / ___| __ )| ____|| __ ) / _ \ / _ \|_   _|
| |   |  _ \|  _|  |  _ \| | | | | | | | |  
| |___| |_) | |___ | |_) | |_| | |_| | | |  
 \____|____/|_____||____/ \___/ \___/  |_|  

 ✅ 1 address kamu ADA di daftar pemenang

┏━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ No┃ Address                               ┃
┣━━━╋━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┫
┃ 1 ┃ 0x48811234567890abcdef1234567890b2f0b  ┃
┗━━━┻━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛
```

## ⚠️ Catatan
- Format pencocokan hanya melihat 6 karakter awal & 5 karakter akhir address
- Pastikan tidak ada spasi atau karakter aneh di file `.txt`
- Script ini **tidak memeriksa blockchain langsung**, hanya membandingkan data dari file

---
💻 **CREATOR by XBOOT**
