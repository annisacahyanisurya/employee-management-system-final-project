# Data Dictionary 

## 1.) Employee

| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Int | NNNNNN | 6 | Angka unik untuk identifikasi employee | 118633 |
| `first_name` | Varchar | - | 25 | Nama depan untuk employee | John |
| `last_name` | Varchar | - | 25 | Nama belakang untuk employee | Doe |
| `gender` | Varchar | "Male" or "Female" | 10 | Jenis kelamin untuk employee | Male |
| `email` | Varchar | - | 25 | Email untuk employee | john@mail.com |
| `phone` | Varchar | NNNNNN | 20 | Phone number untuk employee | 82663821399 |
| `hire_date` | Date | DD/MM/YYYY | - | Hire date didapatkan dari pertama kali gabung | 8/18/2001 |
| `salary` | Int | - | - | Salary untuk dari employee | 50000 |
| `manager` | Int | NNNNNN | 6 | Manager diambil dari id employee | 117798 |
| `job` | Varchar | - | 10 | Job diambil dari id di table Job | IT_PROG |
| `department` | Int | - | - | Department diambil dari id di table department | 1 |

## 2.) Jobs

| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Varchar | - | 10 | Angka unik untuk identifikasi job | IT_PROG |
| `title` | Varchar | - | 35 | Nama pekerjaan atau jabatan dari employee | Programmer |
| `min_salary` | Int | - | - | Minimal salary dari employee | 5500000 |
| `max_salary` | Int | - | - | Maksimal salary dari employee | 7500000 |

## 3.) Departement

| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Varchar | NNN | 3 | Angka unik untuk identifikasi departement | 105 |
| `name` | Varchar | - | 40 | Nama departement dari employee | Human Resource |
| `location` | Int | - | 4 | Location diambil dari id di table locations | 2700 |

## 4.) Locations 
| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Int | NNNN | 4 | Angka unik untuk identifikasi location | 2700 |
| `street_address` | Varchar | - | 40 | Alamat jalan location dari departement | 2014 Jabberwocky Rd |
| `postal_code` | Varchar | - | 12 | Kode pos untuk location | 26192 |
| `city` | Varchar | - | 30 | Kota untuk locations | Southlake |
| `state_province` | Varchar | - | 25 | Bagian/Provinsi dari location | Texas |
| `country` | Char | - | 3 | Country yang diambil dari id di tabel countries | US |

## 5.) Countries
| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Char | NNN | 3 | Angka unik untuk identifikasi country | IDN |
| `name` | Varchar | - | 40 | Nama country dari locations | Indonesia |
| `regions` | Int | - | 3 | Region yang diambil dari id di tabel regions | Asia |

## 6.) Regions
| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Int | - | - | Angka atau Id untuk mengidentifikasi region | 1 |
| `name` | Varchar | - | 25 | Nama untuk region | Asia |

## 7.) Roles
| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Int | - | - | Angka atau Id untuk mengidentifikasi role | 2 |
| `name` | Varchar | - | 50 | Nama yang digunakan untuk role | Manager |

## 8.) Permissions
| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Int | - | 6 | Angka atau Id untuk mengidentifikasi permission | 1 |
| `name` | Varchar | - | 25 | Nama untuk permission | Add Employee |

## 9.) Loan
| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Int | NNNNNNNN | 8 | Angka unik untuk identifikasi Loan | 10624 |
| `employee_id` | Int | NNNNNN | 6 | Angka unik untuk identifikasi employee | 118633 |
| `total_loan` | Int | - | - | Jumlah uang yang dipinjam | 2500000 |
| `loan_date` | Date | DD/MM/YYYY | - | Tanggal uang dipinjam | 19/06/2024 |
| `payment_date` | Date | DD/MM/YYYY | - | Tanggal uang dibayar | 30/06/2024 |
| `due_date` | Date | DD/MM/YYYY | - | Tenggat waktu pembayaran | 05/07/2024 |
| `status` | Varchar | - | 30 | Status peminjaman | Belum bayar |
| `days_late` | Int | - | - | Total telat bayar (dalam hari) | 12 |

## 10.) Penalty 
| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Int | NNNNNNNN | 8 | Angka unik untuk identifikasi id loan | 29005 |
| `penalty_amount`| Decimal | - | - | Total denda yang harus dibayarkan | 120000 |

## 11.) Accounts
| Field Name | Data Type | Data Format | Length | Description | Example |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `id` | Int | NNNNNNNN | 8 | ID employee dalam Tabel Employees | 123 |
| `username` | Varchar | - | 25 | Username akun (seringkali dari last name) | john_snow |
| `password` | Varchar | - | 225 | Password account dari employee | Passw0rd123! |
| `otp` | Int | - | - | Kode yang digunakan untuk forgot password | 1089 |
| `is_expired` | Date | - | - | Waktu masa berlaku atau tenggat kode OTP | 2024-06-13 19:40:03 |
| `is_used` | Bit | - | - | Status apakah kode OTP telah digunakan | 0 |
