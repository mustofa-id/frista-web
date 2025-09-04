# Frista Web

<p align="center">
 <img src="https://github.com/user-attachments/assets/c82422f6-836d-460e-90fd-fbb3107cbdbe" width="500" alt="Demo app" />
</p> 

Frista Web merupakan port aplikasi berbasis web dari Frista Desktop milik BPJS Kesehatan. Aplikasi ini dikembangkan sebagai bagian dari inisiatif untuk meningkatkan aksesibilitas dan efisiensi operasional. Dengan porting web ini, Frista kini dapat diakses melalui berbagai jenis perangkat tanpa perlu instalasi khusus, sehingga memudahkan pengguna dalam berbagai situasi dan lokasi.

Aplikasi ini dirancang agar **bekerja sepenuhnya di sisi klien (client-side) melalui browser**, tanpa menyimpan atau mengumpulkan data pribadi pengguna. Seluruh proses dan komunikasi data dilakukan secara langsung dari browser ke API resmi Frista BPJS Kesehatan. Dengan pendekatan ini, Frista Web tidak hanya memberikan kemudahan akses, tetapi juga menjamin keamanan dan privasi pengguna.

## Integrasi

### 📃 iframe

Frista Web dapat disematkan di `<iframe />` dengan dukungan pengisian NIK atau Nomor Kartu BPJS otomatis melalui `URLSearchParams` dengan key `member_id` dan nilai 13 atau 16 digit angka. Contoh:

```html
<iframe src="<link-aplikasi>?member_id=160207XXXXXX000X" />
```

> ℹ️ Penggunaan `iframe` mewajibkan aplikasi utama berjalan di *[secure context](https://developer.mozilla.org/en-US/docs/Web/Security/Secure_Contexts)*.

### 📃 windowed

Alternatif, Frista Web dapat dijalankan di *[popup window](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#popup)* dengan kode JavaScript:

```js
const url = new URL('<link-aplikasi>');
url.searchParams.set('member_id', '160207XXXXXX000X');
window.open(url, 'FRISTA', 'popup');
```

> ℹ️ Dengan cara ini, aplikasi utama tidak harus berjalan di *secure context*.

### 📃 autentikasi

Terdapat dua metode autentikasi:
* Menyimpan informasi akun di browser
* Menggunakan Web Hook

Klik icon ![passkey_24dp](https://github.com/user-attachments/assets/1ee2cf48-8c4b-4ef0-87f7-a1d5b9cea76a) pada Frista Web untuk informasi selengkapnya.

## Link Aplikasi

* Link Frista Web dapat dilihat di bidang *About/Tentang* 🔝 di repository ini.

## Izin Khusus Terbuka
Memberikan izin terbuka (non-exclusive, perpetual) kepada BPJS Kesehatan untuk:
* Menggunakan, menyalin, memodifikasi, dan/atau mengadopsi aplikasi ini secara penuh maupun sebagian;
* Mendistribusikan kepada pihak terkait (misalnya fasilitas kesehatan mitra) untuk tujuan pelayanan JKN.

## Lainnya
* [Syarat & Ketentuan Penggunaan](./TERMS-OF-USE.md)
* [Kebijakan Privasi](./PRIVACY-POLICY.md)
* Inspirasi: https://github.com/banguncode/PHP-Frista

> Code akan di-publish segera! Jangan lupa berikan star ke repository ini :)
