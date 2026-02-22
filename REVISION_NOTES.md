# Revisi Requirement Logbook Internship Dokter Indonesia

Dokumen ini merangkum implementasi revisi pada prototype `index.html`.

## 1) Perubahan Aturan UKP/LK/TM

- Target UKP total: **400** kasus.
- Distribusi stase:
  - **Rumah Sakit minimal 300**
  - **Puskesmas minimal 100**
- Diagnosis dapat dicari melalui **kode ICD-10** (bukan deskripsi saja).
- **Kelompok usia dihitung dari DOB** secara otomatis.
- Field **kategori kasus dihapus** karena tidak lagi applicable (khusus COVID).
- Sumber data dibatasi menjadi:
  - Rawat inap
  - Rawat darurat
  - Rawat jalan
- Jenis tindakan/jenis UKP:
  - Kegawatan
  - Medik
  - Bedah
  - Kebidanan-perinatal
  - Kejiwaan
  - Medikolegal
- Penambahan **Nomor Kasus internal sistem** selain No RM.

## 2) Tindakan Medis (TM)

TM harus terhubung dengan UKP melalui referensi nomor kasus.

Target TM:
- Pasang infus: **50**
- Pasang NGT: **2**
- Persalinan: **2**
- Bedah minor: **10**
- Pasang kateter: **5**
- Jahit: **15**

## 3) Target Analytics

### Distribusi usia
- Anak: **25–40%**
- Dewasa: **40–60%**
- Lansia: **15–25%**

### Distribusi jenis UKP
- Bedah: **minimal 20%** dari 400
- Kegawatan: **minimal 20%** dari 400
- Kebidanan-perinatal: **minimal 10%** dari 400
- Jiwa + Medikolegal: **minimal 0%**
- Sisa dapat dipenuhi dari medik rawat jalan

### Gender
- Laki-laki vs perempuan: **50:50**

## 4) Catatan implementasi prototype

- Prototype difokuskan ke validasi requirement dan struktur form utama.
- Perhitungan kelompok usia dilakukan client-side dengan JavaScript berdasarkan DOB.
- Integrasi ke backend/API, validasi server-side, dan migrasi data belum diimplementasikan pada prototype ini.
