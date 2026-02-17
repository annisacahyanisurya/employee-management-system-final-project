Dokumentasi ini menyajikan penjelasan mendalam mengenai komponen teknis database, mencakup Technical Requirements, Stored Procedures, Functions, Views, dan Triggers. Selain itu, dokumen ini berfungsi sebagai panduan utama untuk memahami Flowchart Pendukung yang memvisualisasikan alur logika dari setiap kebutuhan sistem (_requirement_).

## 1) Actors
Berikut merupakan user yang akan menggunakan aplikasi Employee Management System:
| Id | Actor | Description |
| :--- | :--- | :--- | 
| ACT01 | Super Admin | Pengguna dengan hak akses tertinggi yang memiliki kontrol penuh atas semua fitur dan pengaturan dalam sistem. | 
| ACT02 | Admin | Pengguna dengan hak akses tinggi yang bertanggung jawab mengelola pengguna lain dan fitur dalam sistem | 
| ACT03 | Manager | Pengguna yang memiliki tanggung jawab atas pengelolaan Employee dan departemen tertentu. | 
| ACT04 | Employee | Pengguna standar yang menggunakan aplikasi untuk menjalankan tugas-tugas mereka sehari-hari dalam organisasi. | 

## 2) Features
### A. Management Employee 
Modul ini digunakan untuk melakukan pengelolaan Employee yang ingin dibuat dan yang sudah ada dari perubahan data diri employee serta pengelolaan akun yang dimiliki employee.

### B. Loan Management 
Modul ini digunakan untuk melakukan pengelolaan terhadap data peminjaman uang (loan) yang dilakukan Employee di suatu perusahaan

## 3) Technical Requirements
- Purpose : Menjelaskan hak akses dari setiap aktor. 
- SP -> Stored Procedure

### 3.1 General
| Id | Requirement | Trigger | Function | Document |
| :--- | :--- | :--- | :--- | :--- | 
| GR001 | SP untuk melakukan login  | - | - | SD-001 |
| GR002 | SP untuk melakukan forgot password | - | F-01, F-02 | SD-002 |
| GR003 | SP untuk melakukan generate kode Otp | - | - | SD-003 |

### 3.2 Super Admin Requirements
| Id | Requirement | Trigger | Function | Document |
| :--- | :--- | :--- | :--- | :--- |
| **Employee** | | | | |
| `SAR001` | SP untuk menambahkan Data Employee baru/ Registrasi Employee | TR-01 | F-01, F-02, F-03, F-04, F-05, F-06 | SD-004 |
| `SAR002` | View untuk melihat detail employee | - | - | VW-001 |
| `SAR003` | SP untuk mengedit Data Employee | TR-02 | - | SD-005 |
| `SAR004` | SP untuk menghapus Data Employee | TR-03 | - | SD-006 |
| **Job** | | | | |
| `SAR005` | SP untuk menambahkan Data Job baru | - | F-07, F-08, F-09 | SD-007 |
| `SAR006` | View untuk melihat data pada Tabel Job | - | - | VW-002 |
| `SAR007` | SP untuk mengedit Data Job | - | - | SD-008 |
| `SAR008` | SP untuk menghapus Data Job | - | - | SD-009 |
| **Department** | | | | |
| `SAR009` | SP untuk menambahkan Data Departement baru | - | F-10 | SD-010 |
| `SAR010` | View untuk melihat detail Departemen | - | - | VW-003 |
| `SAR011` | View melihat data dalam Tabel Department | - | - | VW-004 |
| `SAR012` | SP untuk mengedit data Department | - | - | SD-011 |
| `SAR013` | SP untuk menghapus data Department | - | - | SD-012 |
| **Locations** | | | | |
| `SAR014` | SP untuk menambahkan Data Locations baru | - | F-11, F-12, F-13 | SD-013 |
| `SAR015` | View melihat data dalam Tabel Locations | - | - | VW-005 |
| `SAR016` | SP untuk mengedit data locations | - | - | SD-014 |
| `SAR017` | SP untuk menghapus data locations | - | - | SD-015 |
| **Country** | | | | |
| `SAR018` | SP untuk menambahkan data country baru | - | F-14 | SD-016 |
| `SAR019` | View melihat data dalam Tabel country | - | - | VW-006 |
| `SAR020` | SP untuk mengedit data country | - | - | SD-017 |
| `SAR021` | SP untuk menghapus data country | - | - | SD-018 |
| **Region** | | | | |
| `SAR022` | SP untuk menambahkan Data Region | - | - | SD-019 |
| `SAR023` | View melihat data dalam Tabel region | - | - | VW-007 |
| `SAR024` | SP untuk mengedit Data Region | - | - | SD-020 |
| `SAR025` | SP untuk menghapus Data Region | - | - | SD-021 |
| **Role** | | | | |
| `SAR026` | SP untuk menambahkan Data Role | - | - | SD-022 |
| `SAR027` | View melihat data dalam Tabel Role | - | - | VW-008 |
| `SAR028` | SP untuk mengedit Data Role | - | - | SD-023 |
| `SAR029` | SP untuk menghapus Data Role | - | - | SD-024 |
| **Permission** | | | | |
| `SAR030` | SP untuk menambahkan Data Permission | - | - | SD-025 |
| `SAR031` | View melihat data dalam Tabel Permission | - | - | VW-009 |
| `SAR032` | SP untuk mengedit Data Permission | - | - | SD-026 |
| `SAR033` | SP untuk menghapus Data Permission | - | - | SD-027 |
| **Loan** | | | | |
| `SAR034` | SP untuk menambahkan Data Loan | - | F-15, F-16 | SD-028 |
| `SAR035` | View melihat data dalam Tabel Loan | - | - | VW-010 |
| `SAR036` | SP untuk mengedit Data Loan | - | - | SD-029 |
| `SAR037` | SP untuk menghapus Data Loan | - | - | SD-030 |
| **Penalty** | | | | |
| `SAR038` | View melihat data dalam Tabel Penalty | - | - | VW-011 |

### 3.3 Admin Requirement
| Id | Requirement | Trigger | Function | Document |
| :--- | :--- | :--- | :--- | :--- |
| **Employee** | | | | |
| `AR001` | View untuk melihat detail employee | - | - | VW-001 |
| `AR002` | SP untuk menambahkan Data Employee baru/ Registrasi Employee | TR-01 | F-01, F-02, F-03, F-04, F-05, F-06 | SD-004 |
| `AR003` | SP untuk mengedit Data Employee | TR-02 | - | SD-005 |
| `AR004` | SP untuk menghapus Data Employee | TR-03 | - | SD-006 |
| **Job** | | | | |
| `AR005` | SP untuk menambahkan Data Job baru | - | F-07, F-08, F-09 | SD-007 |
| `AR006` | View untuk melihat data pada Tabel Job | - | - | VW-002 |
| `AR007` | SP untuk mengedit Data Job | - | - | SD-008 |
| `AR008` | SP untuk menghapus Data Job | - | - | SD-009 |
| **Department** | | | | |
| `AR009` | SP untuk menambahkan Data Departement baru | - | F-10 | SD-010 |
| `AR010` | View untuk melihat detail Departemen | - | - | VW-003 |
| `AR011` | View melihat data dalam Tabel Department | - | - | VW-004 |
| `AR012` | SP untuk mengedit data Department | - | - | SD-011 |
| `AR013` | SP untuk menghapus data Department | - | - | SD-012 |
| **Locations** | | | | |
| `AR014` | SP untuk menambahkan Data Locations baru | - | F-11, F-12, F-13 | SD-013 |
| `AR015` | View melihat data dalam Tabel Locations | - | - | VW-005 |
| `AR016` | SP untuk mengedit data locations | - | - | SD-014 |
| `AR017` | SP untuk menghapus data locations | - | - | SD-015 |
| **Country** | | | | |
| `AR018` | SP untuk menambahkan data country baru | - | F-14 | SD-016 |
| `AR019` | View melihat data dalam Tabel country | - | - | VW-006 |
| `AR020` | SP untuk mengedit data country | - | - | SD-017 |
| **Region** | | | | |
| `AR021` | SP untuk menambahkan Data Region | - | - | SD-019 |
| `AR022` | View melihat data dalam Tabel region | - | - | VW-007 |
| `AR023` | SP untuk mengedit Data Region | - | - | SD-020 |
| **Role** | | | | |
| `AR024` | SP untuk menambahkan Data Role | - | - | SD-022 |
| `AR025` | View melihat data dalam Tabel Role | - | - | VW-008 |
| `AR026` | SP untuk mengedit Data Role | - | - | SD-023 |
| **Loan** | | | | |
| `AR027` | SP untuk menambahkan Data Loan | - | F-15, F-16 | SD-028 |
| `AR028` | View melihat data dalam Tabel Loan | - | - | VW-010 |
| `AR029` | SP untuk mengedit Data Loan | - | - | SD-029 |
| **Penalty** | | | | |
| `AR030` | View melihat data dalam Tabel Penalty | - | - | VW-011 |

### 3.4 Manager Requirement
| Id | Requirement | Trigger | Function | Document |
| :--- | :--- | :--- | :--- | :--- |
| **Employee** | | | | |
| `MR001` | View untuk melihat detail employee | - | - | VW-001 |
| `MR002` | SP untuk mengedit Data Employee | TR-02 | - | SD-005 |
| **Profile** | | | | |
| `MR003` | SP untuk mengedit Data Profile | - | - | SD-034 |
| `MR004` | SP untuk mengubah Password | - | - | SD-035 |

### 3.5 Employee Requirement
| Id | Requirement | Trigger | Function | Document |
| :--- | :--- | :--- | :--- | :--- |
| **Profile** | | | | |
| `ER001` | SP untuk mengedit Data Profile | - | - | SD-034 |
| `ER002` | SP untuk mengubah Password | - | - | SD-035 |

## 4. Functions
| Id | Name | Description | Parameter | Data Type | Length | Return |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `F-01` | `func_email_format` | value input harus sesuai format email | Email | Varchar | 50 | 1 (True) |
| `F-02` | `func_password_policy` | value input harus memiliki minimal 8 karakter | Password | Varchar | 255 | 1 (True) |
| `F-03` | `func_gender` | value input harus memiliki "Male" atau "Female" | Gender | Varchar | 10 | 1 (True) |
| `F-04` | `func_phone_number` | value input tidak boleh memiliki karakter | Phone | Varchar | 20 | 1 (True) |
| `F-05` | `func_title_length` | value input tidak boleh lebih dari yang sudah ditentukan | Title | Varchar | 35 | 1 (True) |
| `F-06` | `func_title_format` | value input tidak boleh memiliki karakter spesial | Title | Varchar | 35 | 1 (True) / 0 (False) |
| `F-07` | `func_salary_positive` | value input tidak boleh bernilai negatif | Min Salary, Max Salary | Int | - | 1 (True) / 0 (False) |
| `F-08` | `func_department_format`| value input tidak boleh memiliki karakter spesial AND panjangnya sesuai | Department name | Varchar | 30 | 1 (True) / 0 (False) |
| `F-09` | `func_street_address_length`| value input tidak boleh lebih dari yang sudah ditentukan | Street address | Varchar | 40 | 1 (True) |
| `F-10` | `func_city_format` | value input tidak boleh memiliki karakter spesial | City | Varchar | 30 | 1 (True) |
| `F-11` | `func_state_province_format`| value input tidak boleh memiliki karakter spesial | State Province | Varchar | 25 | 1 (True) |
| `F-12` | `func_country_format` | value input tidak boleh memiliki karakter spesial | Country name | Varchar | 40 | 1 (True) |
| `F-13` | `func_username_format` | value input tidak boleh memiliki karakter spesial | username | Varchar | 50 | 1 (True) |

## 5. Triggers
| Id | Name | Description | On Table | Action |
| :--- | :--- | :--- | :--- | :--- |
| `TR-01` | `tr_insert_employee` | Menambahkan data ke table job histories | `tbl_employees` | After Insert |
| `TR-02` | `tr_update_employee_job`| Menambahkan data ke table job histories dengan status "Hand Over" ketika ada perubahan pada kolom job | `tbl_employees` | After Update |
| `TR-03` | `tr_delete_employee` | Menambahkan data ke table job histories | `tbl_employees` | After Delete |

## 6. Views
| Id | Name | Description | Property | Note |
| :--- | :--- | :--- | :--- | :--- |
| `VW-001` | `vw_employee_details` | Untuk melihat list employee secara detail | `id`<br>`username`<br>`full_name`<br>`gender`<br>`email`<br>`hire_date`<br>`salary`<br>`manager_id`<br>`manager_name`<br>`job`<br>`department`<br>`role`<br>`location`<br>`status` | Employee id<br>Account username<br>Employee first_name and last_name<br>Employee gender<br>Employee email<br>Employee hire date<br>Employee salary<br>Employee manager id<br>Employee manager first_name and last_name<br>Employee job name dari table job<br>Employee department name dari table<br>Diambil dari role yang paling tinggi<br>Diambil dari city di table location<br>Diambil dari status paling terakhir |
| `VW-002` | `vw_job` | Untuk melihat data-data yang ada dalam tabel Job | `id`<br>`title`<br>`min_salary`<br>`max_salary` | Job id<br>Nama pekerjaan atau jabatan<br>Minimal salary<br>Maksimal salary |
| `VW-003` | `vw_department_details` | Untuk melihat department secara detail | `id`<br>`name`<br>`locations`<br>`country` | Department id<br>Department name<br>Gabungan department location street_address<br>Nama country dari tabel countries |
| `VW-004` | `vw_department` | Untuk melihat data-data yang ada dalam tabel departments | `id`<br>`name`<br>`locations` | Department id<br>Department name<br>Department location id |
| `VW-005` | `vw_locations` | Untuk melihat data-data yang ada dalam tabel locations | `id`<br>`street_address`<br>`postal_code`<br>`city`<br>`state_province`<br>`country` | Location id<br>Location street address<br>Location postal code<br>Location city name<br>Location state province<br>Location country id |
| `VW-006` | `vw_countries` | Untuk melihat data-data yang ada dalam tabel countries | `id`<br>`country`<br>`regions` | Country Id<br>Country name<br>Country region id |
| `VW-007` | `vw_regions` | Untuk melihat data-data yang ada dalam tabel region | `id`<br>`name` | Region Id<br>Region Name |
| `VW-008` | `vw_roles` | Untuk melihat data-data yang ada dalam tabel role | `id`<br>`name` | Role Id<br>Role Name |
| `VW-009` | `vw_permissions` | Untuk melihat data-data yang ada dalam tabel permission | `id`<br>`name` | Permission Id<br>Permission Name |
| `VW-010` | `vw_loan` | Untuk melihat data-data yang ada dalam tabel loan | `id`<br>`employee_id`<br>`total`<br>`loan_date`<br>`payment_date`<br>`due_date`<br>`status`<br>`days_late` | Loan Id<br>Employee Id<br>Total Loan<br>Loan Date (Tanggal Peminjaman)<br>Payment Date (Tanggal Pembayaran)<br>Tenggat Waktu Pembayaran<br>Status Bayar<br>Total Telat Bayar (dalam hari) |
| `VW-011` | `vw_penalty` | Untuk melihat data-data yang ada di dalam tabel penalty | `loan_id`<br>`penalty_amount` | Id dari loan<br>Jumlah denda yang harus di bayar |
| `VW-012` | `vw_accounts` | Untuk melihat data yang ada didalam tabel accounts | `id`<br>`username`<br>`password`<br>`otp`<br>`is_expired`<br>`is_used` | Id Employee dalam tabel<br>username account employee<br>password account employee yang...<br>Kode OTP untuk forgot password<br>Lama waktu kode otp dapat digunakan<br>Status kode OTP, "Used" & "Not Used" |





