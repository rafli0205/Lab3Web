# Praktikum 3: Membuat Form (Dropdown & Listbox Multiple Selection)

**Nama:** Rafli Dhiya Fadhaly  
**NIM:** 312410251  
**Mata Kuliah:** Pemrograman Web 1  
**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom

---

## Tujuan Praktikum
1. Mahasiswa mampu memahami struktur dasar pembuatan **Form** pada HTML.  
2. Mahasiswa mampu menampilkan elemen **Dropdown Menu** dan **Listbox Multiple Selection**.  
3. Mahasiswa mampu menambahkan **CSS** untuk memperindah tampilan form.  

---

## Langkah-langkah Praktikum

### 1. Struktur Dasar HTML
Buat folder baru bernama `Lab3Web`, lalu buat file `lab3_form.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan</title>
</head>
<body>
    <header>
        <h1>Membuat Form</h1>
    </header>
</body>
</html>
```

![Screenshot 1](https://github.com/user-attachments/assets/c332bc25-6199-4e69-974d-7a67e808e5c6)

---

### 2. Membuat Struktur Form
Tambahkan tag `<form>` dan `<fieldset>` untuk membungkus elemen form.

```html
<form action="proses.php" method="post">
  <fieldset>
    <legend>Data Mahasiswa</legend>
    <!-- Elemen form ditulis di sini -->
  </fieldset>
</form>
```

![Screenshot 2](https://github.com/user-attachments/assets/7ae18fa4-0a5a-4e83-9781-fa0f8a74d9b8)

**Penjelasan:**
- `<form>` digunakan untuk mengelompokkan input pengguna.  
- `action="proses.php"` menentukan file tujuan pengiriman data.  
- `<fieldset>` memberi bingkai dan `<legend>` memberi judul pada form.  

---

### 3. Menambahkan Input Nama & Alamat
```html
<p>
  <label for="nama">Nama</label>
  <input type="text" id="nama" name="nama">
</p>

<p>
  <label for="alamat">Alamat</label>
  <textarea id="alamat" name="alamat" cols="20" rows="3"></textarea>
</p>
```

![Screenshot 3](https://github.com/user-attachments/assets/ebc27e93-d5d9-46c0-837b-b6ad3c42f737)

**Penjelasan:**
- `<input type="text">` digunakan untuk mengisi nama singkat.  
- `<textarea>` digunakan untuk teks panjang seperti alamat.  

---

### 4. Menambahkan Dropdown Menu
```html
<p>
  <label for="prodi">Program Studi</label>
  <select id="prodi" name="prodi">
    <option value="">-- Pilih Program Studi --</option>
    <option value="TI">Teknik Informatika</option>
    <option value="SI">Sistem Informasi</option>
    <option value="RPL">Rekayasa Perangkat Lunak</option>
    <option value="MI">Manajemen Informatika</option>
  </select>
</p>
```

![Screenshot 4](https://github.com/user-attachments/assets/0082efdd-2d5e-4250-a6fe-687322f1f637)

**Penjelasan:**
- `<select>` membuat dropdown menu.  
- `<option>` menampilkan setiap pilihan yang bisa dipilih pengguna.  

---

### 5. Menambahkan Listbox Multiple Selection
```html
<p>
  <label for="minat">Bidang Minat</label><br>
  <select id="minat" name="minat[]" multiple size="4">
    <option value="web">Pemrograman Web</option>
    <option value="ai">Kecerdasan Buatan</option>
    <option value="network">Jaringan Komputer</option>
    <option value="database">Basis Data</option>
    <option value="uiux">Desain UI/UX</option>
  </select>
</p>
```

![Screenshot 5](https://github.com/user-attachments/assets/e0820450-3fc6-488f-803a-9695e00ffdda)

**Penjelasan:**
- Atribut `multiple` memungkinkan memilih lebih dari satu pilihan.  
- Atribut `size="4"` menampilkan 4 baris secara vertikal.  
- `name="minat[]"` menggunakan tanda `[]` agar data dikirim sebagai array.  

---

### 6. Menambahkan Tombol Submit
```html
<p><input type="submit" value="Kirim Data"></p>
```

![Screenshot 6](https://github.com/user-attachments/assets/3aae6be2-61c6-4614-bced-d67c58845059)

**Penjelasan:**  
Tombol ini digunakan untuk mengirim seluruh isi form ke file `proses.php`.

---

### 7. Menambahkan CSS
Tambahkan CSS di dalam tag `<style>` agar tampilan lebih rapi dan menarik.

```html
<style>
  form p > label {
    display: inline-block;
    width: 120px;
  }
  form input[type="text"], form textarea, form select {
    border: 1px solid #197a43;
    padding: 3px;
  }
  form input[type="submit"] {
    border: 1px solid #197a43;
    background-color: #197a43;
    color: #ffffff;
    font-weight: bold;
    padding: 5px 15px;
  }
</style>
```

![Screenshot 7](https://github.com/user-attachments/assets/6f64d3c0-cbea-4fca-bf71-2e816da3ef7f)

**Penjelasan:**
- Memberi warna hijau pada border form.  
- Mengatur jarak dan ukuran tombol kirim agar seragam dan profesional.  

---

## Kesimpulan
Pada praktikum ini, telah dibuat form HTML dengan elemen **input text**, **textarea**, **dropdown**, **listbox multiple selection**, serta ditambahkan **CSS** agar tampilannya lebih menarik.  
Praktikum ini membantu memahami bagaimana form dapat digunakan untuk mengumpulkan data pengguna secara efisien dan terstruktur.

---
