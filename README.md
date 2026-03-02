# 🌐 WEB VIEW
<img width="1918" height="1197" alt="Image" src="https://github.com/user-attachments/assets/14b4e802-bfcd-4697-8a76-8d25f5aa119b" />


1. TAMBAH USER BARU (CREATE)
Method: POST
Endpoint: /api/users
Headers:
Content-Type: application/json

Request Body:
{
"name": "Wowo",
"age": 20
}

Response (201 Created):
{
"status": "success",
"data": {
"id": "123e4567-e89b-12d3-a456-426614174000",
"name": "Naufal Priyamukti Wibowo",
"age": 20
}
}

2. AMBIL SEMUA DATA USER (READ ALL)
Method: GET
Endpoint: /api/users
Headers:
Accept: application/json

Response (200 OK):
{
"status": "success",
"data": [
{
"id": "123e4567-e89b-12d3-a456-426614174000",
"name": "Naufal Priyamukti Wibowo",
"age": 20
}
]
}

3. AMBIL DATA USER BERDASARKAN ID (READ BY ID)
Method: GET
Endpoint: /api/users/{id}
Headers:
Accept: application/json

Response (200 OK):
{
"status": "success",
"data": {
"id": "123e4567-e89b-12d3-a456-426614174000",
"name": "Naufal Priyamukti Wibowo",
"age": 20
}
}

4. EDIT DATA USER (UPDATE)
Method: PUT
Endpoint: /api/users/{id}
Headers:
Content-Type: application/json

Request Body:
{
"name": "Naufal P. Wibowo",
"age": 21
}

Response (200 OK):
{
"status": "success",
"data": {
"id": "123e4567-e89b-12d3-a456-426614174000",
"name": "Naufal P. Wibowo",
"age": 21
}
}

5. HAPUS USER (DELETE)
Method: DELETE
Endpoint: /api/users/{id}

Response (200 OK):
{
"status": "success delete user with id 123e4567-e89b-12d3-a456-426614174000"
}

RINGKASAN ENDPOINT

POST /api/users -> Menambah user
GET /api/users -> Ambil semua user
GET /api/users/{id} -> Ambil user by ID
PUT /api/users/{id} -> Update user
DELETE /api/users/{id} -> Hapus user

