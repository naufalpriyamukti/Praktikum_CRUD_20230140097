# 🌐 WEB VIEW
<img width="1918" height="1197" alt="Image" src="https://github.com/user-attachments/assets/14b4e802-bfcd-4697-8a76-8d25f5aa119b" />

1. ➕ Tambah User Baru (Create)
Menambahkan data pengguna baru. ID akan otomatis di-generate dalam format UUID.

Method	Endpoint	Headers
POST	/api/users	Content-Type: application/json
Request Body:

json
{
    "name": "Wowo",
    "age": 20
}
Success Response (201 Created):

json
{
    "status": "success",
    "data": {
        "id": "123e4567-e89b-12d3-a456-426614174000",
        "name": "Naufal Priyamukti Wibowo",
        "age": 20
    }
}
2. 📋 Ambil Semua Data User (Read All)
Menampilkan daftar seluruh pengguna yang ada di database.

Method	Endpoint	Headers
GET	/api/users	Accept: application/json
Success Response (200 OK):

json
{
    "status": "success",
    "data": [
        {
            "id": "123e4567-e89b-12d3-a456-426614174000",
            "name": "Wowo",
            "age": 20
        }
    ]
}
3. 🔍 Cari User Berdasarkan ID (Read By ID)
Mengambil detail data satu pengguna secara spesifik.

Method	Endpoint	Headers
GET	/api/users/{id}	Accept: application/json
Success Response (200 OK):

json
{
    "status": "success",
    "data": {
        "id": "123e4567-e89b-12d3-a456-426614174000",
        "name": "Wowo",
        "age": 20
    }
}
4. ✏️ Edit Data User (Update)
Memperbarui informasi nama atau umur pengguna yang sudah ada.

Method	Endpoint	Headers
PUT	/api/users/{id}	Content-Type: application/json
Request Body:

json
{
    "name": "Wowo",
    "age": 21
}
Success Response (200 OK):

json
{
    "status": "success",
    "data": {
        "id": "123e4567-e89b-12d3-a456-426614174000",
        "name": "Naufal P. Wibowo",
        "age": 21
    }
}
5. 🗑️ Hapus User (Delete)
Menghapus data pengguna dari database secara permanen.

Method	Endpoint
DELETE	/api/users/{id}
Success Response (200 OK):

json
{
    "status": "success delete user with id 123e4567-e89b-12d3-a456-426614174000"
}
📊 Ringkasan Endpoint
Method	Endpoint	Fungsi
POST	/api/users	Menambah user baru
GET	/api/users	Mengambil semua data user
GET	/api/users/{id}	Mengambil data user by ID
PUT	/api/users/{id}	Mengupdate data user by ID
DELETE	/api/users/{id}	Menghapus data user by ID

