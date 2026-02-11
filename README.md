# Katalog Tawas Spray

Website katalog produk Tawas Spray. Siap di-upload ke Vercel dan mudah diedit (gambar + harga).

## Cara Edit

### Mengganti / menambah gambar produk
1. Letakkan file gambar (JPG/PNG) di folder **`public/images/`**
2. Buka file **`data/products.json`**
3. Di setiap produk, ubah nilai **`"image"`** menjadi path gambar Anda, contoh:
   - `"/images/tawas-spray-1.jpg"`
   - `"/images/foto-produk-saya.png"`

### Mengedit nama, deskripsi, dan harga
1. Buka file **`data/products.json`**
2. Edit:
   - **`name`** — nama produk
   - **`description`** — deskripsi singkat
   - **`price`** — harga (tulis angka saja, tanpa titik), contoh: `"25000"`
3. Simpan file.

### Menambah produk baru
Di **`data/products.json`**, tambahkan objek baru (copy salah satu produk, lalu ubah id, name, description, price, image). Contoh:

```json
{
  "id": "4",
  "name": "Nama Produk Baru",
  "description": "Deskripsi produk.",
  "price": "35000",
  "image": "/images/gambar-baru.jpg"
}
```

Jangan lupa letakkan file **gambar-baru.jpg** di folder **`public/images/`**.

## Menjalankan di komputer

1. Pasang Node.js (LTS) dari https://nodejs.org
2. Di folder project, jalankan:
   ```bash
   npm install
   npm run dev
   ```
3. Buka http://localhost:3000 di browser.

## Deploy ke Vercel

1. Buat akun di [vercel.com](https://vercel.com) (gratis).
2. Upload project ini ke GitHub (buat repo, push code).
3. Di Vercel: **Add New Project** → pilih repo GitHub Anda.
4. Klik **Deploy** (aturan default Next.js sudah cocok).
5. Setelah selesai, situs Anda dapat diakses lewat URL yang diberikan Vercel.

Setiap kali Anda mengubah **`data/products.json`** atau menambah/mengganti file di **`public/images/`**, commit dan push ke GitHub; Vercel akan otomatis build dan update website.
