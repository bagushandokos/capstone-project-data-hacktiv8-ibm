# Capstone Project - Data Hacktiv8 x IBM

## Project Title
Analisis Kesenjangan Guru dan Akses Internet di Indonesia Menggunakan AI (IBM Granite Models)

## Project Overview
Pendidikan di Indonesia menghadapi dua tantangan besar:  
1. Kesenjangan rasio murid-guru yang masih timpang di beberapa provinsi.  
2. Kesenjangan digital dalam akses internet rumah tangga dan sekolah.  

Tujuan proyek ini adalah memetakan kondisi provinsi di Indonesia berdasarkan dua indikator tersebut, serta menggali insight menggunakan AI (IBM Granite Models) untuk memberikan rekomendasi kebijakan pendidikan digital.

## Dataset
Sumber data publik resmi (BPS & Data.go.id):

### Akses Internet Sekolah
- [Proporsi sekolah dengan akses ke internet untuk tujuan pembelajaran pada jenjang SD - SD/MI/Sederajat - 2023 - Indonesia](https://data.go.id/dataset/dataset/proporsi-sekolah-dengan-akses-ke-internet-untuk-tujuan-pembelajaran-pada-jenjang-sd-sd-mi-seder)  
- [Proporsi sekolah dengan akses ke internet untuk tujuan pembelajaran pada jenjang SMP - SMP/MTs/Sederajat - 2023 - Indonesia](https://data.go.id/dataset/dataset/proporsi-sekolah-dengan-akses-ke-internet-untuk-tujuan-pembelajaran-pada-jenjang-smp-smp-mts-se)  
- [Proporsi sekolah dengan akses ke internet untuk tujuan pembelajaran pada jenjang SMA - SMA/MA/Sederajat - 2023 - Indonesia](https://data.go.id/dataset/dataset/proporsi-sekolah-dengan-akses-ke-internet-untuk-tujuan-pembelajaran-pada-jenjang-sma-sma-ma-sed)  
- [Proporsi sekolah dengan akses ke internet untuk tujuan pembelajaran pada jenjang SMK - SMK/MAK/Sederajat - 2023 - Indonesia](https://data.go.id/dataset/dataset/proporsi-sekolah-dengan-akses-ke-internet-untuk-tujuan-pembelajaran-pada-jenjang-smk-smk-mak-se)  

### Rasio Murid per Guru
- [Rasio Murid-Guru SD - SD/MI/Sederajat - 2023 - Indonesia](https://data.go.id/dataset/dataset/rasio-murid-guru-sd-sd-mi-sederajat-2023-indonesia)  
- [Rasio Murid-Guru SMP - SMP/MTs/Sederajat - 2023 - Indonesia](https://data.go.id/dataset/dataset/rasio-murid-guru-smp-smp-mts-sederajat-2023-indonesia)  
- [Rasio Murid-Guru SMA - SMA/MA/Sederajat - 2023 - Indonesia](https://data.go.id/dataset/dataset/rasio-murid-guru-sma-sma-ma-sederajat-2023-indonesia)  
- [Rasio Murid-Guru SMK - SMK/MAK/Sederajat - 2023 - Indonesia](https://data.go.id/dataset/dataset/rasio-murid-guru-smk-smk-mak-sederajat-2023-indonesia)  

### Akses Internet Rumah Tangga
- [Persentase Rumah Tangga yang Pernah Mengakses Internet dalam 3 Bulan Terakhir Menurut Provinsi dan Klasifikasi Daerah 2023](https://www.bps.go.id/id/statistics-table/2/Mzk4IzI=/persentase-rumah-tangga-yang-pernah-mengakses-internet-dalam-3-bulan-terakhir-menurut-provinsi-dan-klasifikasi-daerah.html)

## Analysis Process
1. Data Cleaning 
   - Standardisasi nama provinsi  
   - Konversi data numerik (mengganti koma → titik)  
   - Pembuangan entri non-provinsi (Indonesia total, luar negeri)  

2. Data Aggregation  
   - Hitung rata-rata rasio murid/guru per provinsi  
   - Hitung rata-rata persentase akses internet sekolah & rumah tangga  

3. Clustering (AI - KMeans)
   - Fitur: Persen_Internet_RT, Rasio Murid per Guru  
   - Jumlah cluster: 3  

4. AI Support (Granite)
   - Gunakan model
   - Prompt: menganalisis tiap cluster → nama cluster, insight utama, rekomendasi  

## Insight & Findings
- Cluster 0: Internet tinggi, kesenjangan guru timpang  
- Cluster 1: Internet rendah, guru timpang
- Cluster 2: Internet tinggi, guru seimbang  

## Recommendations
- Cluster 0: Optimalkan distribusi guru + pelatihan e-learning.  
- Cluster 1: Prioritaskan pembangunan infrastruktur digital.  
- Cluster 2: Perluas program pelatihan digital guru (PDGD).  

## AI Support Explanation
- IBM Granite digunakan untuk interpretasi cluster → memberi insight yang lebih kaya daripada sekadar angka.  
- Model membantu memberi nama cluster, menarik insight utama, serta menghasilkan rekomendasi kebijakan.  

## Conclusion
Dengan kombinasi analisis data + dukungan AI, proyek ini menemukan pola jelas antara kesenjangan guru dan kesiapan digital provinsi di Indonesia.  
Rekomendasi berbasis AI ini dapat menjadi dasar kebijakan yang lebih tepat sasaran untuk memperbaiki kualitas pendidikan.  
