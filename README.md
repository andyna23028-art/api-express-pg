# 🎓 RESTful API Mahasiswa dengan Express & PostgreSQL

Project ini merupakan implementasi CRUD API menggunakan Node.js, Express, dan PostgreSQL. Data yang dikelola berupa informasi mahasiswa, dan project ini mengikuti arsitektur MVC.

---

## 🚀 Fitur Utama

- Menampilkan semua data mahasiswa
- Menampilkan data mahasiswa berdasarkan ID
- Menambahkan data mahasiswa baru
- Memperbarui data mahasiswa
- Menghapus data mahasiswa
- Error handling untuk setiap operasi
- Koneksi database menggunakan environment variable (`.env`)

---

## 📦 Instalasi

```bash
npm install
npx nodemon index.js

## 🗂️ Struktur Folder

api_express_pg/
├── index.js
├── .env
├── package.json
├── src/
│   ├── config/
│   │   └── db.js
│   ├── models/
│   │   └── studentsModel.js
│   ├── controllers/
│   │   └── studentsController.js
│   └── routes/
│       └── studentsRoutes.js
└── README.md

## 🧾 Struktur Tabel

CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  major VARCHAR(50),
  age INT
);

## 📮 Endpoint API

GET     /api/students           → Ambil semua data mahasiswa
GET     /api/students/:id       → Ambil data mahasiswa berdasarkan ID
POST    /api/students           → Tambah data mahasiswa baru
PUT     /api/students/:id       → Update data mahasiswa berdasarkan ID
DELETE  /api/students/:id       → Hapus data mahasiswa berdasarkan ID

## 📌 Catatan

- Gunakan Postman untuk menguji semua endpoint
- Pastikan format body JSON saat menggunakan POST dan PUT
- Koneksi database diatur melalui file .env dan digunakan di db.js
- Tabel students harus sudah dibuat di PostgreSQL sebelum testing
- Semua query SQL menggunakan parameterized query untuk keamanan
- Struktur project mengikuti pola MVC: Model, Controller, Router

## 👩‍💻 Author

Mahasiswa Sistem Informasi – Universitas Negeri Surabaya
Backend Developer | PostgreSQL | RESTful API | GitHub
