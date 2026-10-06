# Handover screens

Template HTML mandiri untuk dokumentasi screen handover ke developer.

## Mengisi dokumentasi

1. Di Pen.dev, pilih frame lalu klik **Export HTML**. Salin file HTML hasil export ke `assets/screens/`.
2. Buka `index.html`, lalu isi objek `handover` di bagian bawah file.
3. Tambahkan modul untuk setiap produk/flow dan screen untuk setiap tampilan.
4. Buka `index.html` langsung di browser untuk mengecek hasilnya.

Contoh screen:

```js
{ id: "GML-01", title: "Inbox", state: "Default", document: "assets/screens/gmail-01-inbox.html", notes: "Catatan implementasi." }
```

## Publish ke GitHub Pages

1. Buat repository baru di GitHub, lalu unggah folder ini ke repository tersebut.
2. Buka **Settings → Pages** pada repository.
3. Pada **Build and deployment**, pilih **GitHub Actions** sebagai source.
4. Push ke branch `main`. Workflow di `.github/workflows/deploy-pages.yml` akan menerbitkan situs.
5. URL akan tersedia di halaman **Actions** atau **Settings → Pages**, biasanya `https://USERNAME.github.io/NAMA-REPOSITORY/`.

Jika repository memakai branch selain `main`, ubah nilai `branches` dalam file workflow.
