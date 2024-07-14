# Belajar Database

Tutorial ini akan membantu Anda memulai dengan dasar-dasar pengelolaan database menggunakan MySQL dengan dirver https://github.com/go-sql-driver/mysql/. Berikut adalah langkah-langkah yang perlu Anda ikuti:

### Persiapan Awal

buatlah databse baru beranama golang

### Membuat Tabel `customer`

Pertama, kita akan membuat tabel `customer` dengan perintah berikut:

```sql
CREATE TABLE customer(
  id VARCHAR(100) NOT NULL,
  NAME VARCHAR(100) NOT NULL,
  PRIMARY KEY (id)
) ENGINE = InnoDB;
```

Menambah Kolom ke Tabel customer

### Menambah beberapa kolom ke tabel customer:

```sql
ALTER TABLE customer
ADD COLUMN email VARCHAR(100),
ADD COLUMN balance INTEGER DEFAULT 0,
ADD COLUMN rating DOUBLE DEFAULT 0.0,
ADD COLUMN created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
ADD COLUMN birth_date DATE,
ADD COLUMN married BOOLEAN DEFAULT FALSE;
```

### Melihat Struktur Tabel `customer`

Untuk melihat struktur tabel customer, gunakan perintah berikut:

```sql
DESC customer;
```

### Menambahkan Data ke Tabel `customer`

Berikut adalah contoh bagaimana menambahkan data ke tabel customer:

```sql
INSERT INTO customer(id, name, email, balance, rating, birth_date, married)
VALUES
('john', 'John', 'john@mail.com', 100000, 90.0, '1999-12-12', TRUE),
('doe', 'Doe', 'doe@mail.com', 50000, 70.0, '2000-12-12', TRUE);
```

### Membuat Tabel `user`

Selanjutnya, kita akan membuat tabel user:

```sql
CREATE TABLE user(
  username VARCHAR(100) NOT NULL,
  password VARCHAR(100) NOT NULL,
  PRIMARY KEY (username)
) ENGINE = InnoDB;
```

### Melihat Struktur Tabel `user`

Untuk melihat struktur tabel user, gunakan perintah berikut:

```sql
DESC user;
```

### Menambahkan Data ke Tabel `user`

Berikut adalah contoh bagaimana menambahkan data ke tabel user:

```sql
INSERT INTO user(username, password)
VALUES ('admin', 'admin');
```

### Membuat Tabel `comments`

Terakhir, kita akan membuat tabel comments:

```sql
CREATE TABLE comments(
  id INT NOT NULL AUTO_INCREMENT,
  email VARCHAR(100) NOT NULL,
  comment TEXT,
  PRIMARY KEY (id)
) ENGINE = InnoDB;
```

### Untuk melihat struktur tabel 'user', gunakan perintah berikut:

```sql
DESC user;
```
