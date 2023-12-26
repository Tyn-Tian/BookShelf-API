# BookShelf-API

## Deskripsi
Submission dicoding: Belajar Membuat Aplikasi Back-End untuk Pemula dengan Google Cloud.

## Endpoint
Server berjalan di localhost:5000
### 1. Get all book
- **Deskripsi**: Untuk mendapatkan semua data buku
- **Method**: GET
- **Path**: `/books`
- **Parameter**: -

### 2. Get all reading or unreading book
- **Deskripsi**: Untuk mendapatkan semua data buku yang sudah dibaca atau belum dibaca
- **Method**: GET
- **Path**: `/books?reading={reading}`
- **Parameter**: 

   | Parameter  | Value   | Deskripsi                  |
   |------------|---------|----------------------------|
   | reading    | 1 or 0  | 1 = reading, 0 = unreading |

### 3. Get all finished or unfinished book
- **Deskripsi**: Untuk mendapatkan semua data buku yang sudah selesai dibaca atau belum selesai dibaca
- **Method**: GET
- **Path**: `/books?finished={finished}`
- **Parameter**: 

   | Parameter  | Value   | Deskripsi                    |
   |------------|---------|------------------------------|
   | finished   | 1 or 0  | 1 = finished, 0 = unfinished |

### 4. Get all contain {name} Name
- **Deskripsi**: Untuk mendapatkan semua data buku yang difilter
- **Method**: GET
- **Path**: `/books?name={name}`
- **Parameter**: 

   | Parameter  | Tipe    | Deskripsi                    |
   |------------|---------|------------------------------|
   | name       | String  | Nama buku yang ingin dicari  |

### 5. create new book
- **Deskripsi**: Untuk menyimpan data buku
- **Method**: POST
- **Path**: `/books`
- **Body**: 
    ```bash
    {
        "name": "{{newName}}",
        "year": {{newYear}},
        "author": "{{newAuthor}}",
        "summary": "{{newSummary}}",
        "publisher": "{{newPublisher}}",
        "pageCount": {{newPageCount}},
        "readPage": {{newReadPage}},
        "reading": {{newReading}}
    }

### 6. get book
- **Deskripsi**: Untuk mendapatkan data buku 
- **Method**: GET
- **Path**: `/books/{bookID}`
- **Parameter**: 

   | Parameter  | Tipe    | Deskripsi                |
   |------------|---------|--------------------------|
   | bookID     | Integer | ID Buku                  |


### 7. Change book data
- **Deskripsi**: Untuk mengubah data buku
- **Method**: PUT
- **Path**: `/books/{bookID}`
- **Parameter**: 

   | Parameter  | Tipe    | Deskripsi                |
   |------------|---------|--------------------------|
   | bookID     | Integer | ID Buku                  |

- **Body**:
    ```bash
    {
        "name": "{{updateName}}",
        "year": {{updateYear}},
        "author": "{{updateAuthor}}",
        "summary": "{{updateSummary}}",
        "publisher": "{{updatePublisher}}",
        "pageCount": {{updatePageCount}},
        "readPage": {{updateReadPage}},
        "reading": {{updateReading}}
    }

### 8. Delete book
- **Deskripsi**: Untuk menghapus buku
- **Method**: DELETE
- **Path**: `/books/{bookID}`
- **Parameter**: 

   | Parameter  | Tipe    | Deskripsi                |
   |------------|---------|--------------------------|
   | bookID     | Integer | ID Buku                  |