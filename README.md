# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju

## Business Understanding

Jaya Jaya Maju merupakan perusahaan multinasional yang telah berdiri sejak tahun 2000 dan saat ini mempekerjakan lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. Sebagai perusahaan besar dengan cakupan nasional, keberhasilan Jaya Jaya Maju sangat bergantung pada stabilitas dan produktivitas tenaga kerjanya. Meskipun demikian, perusahaan kini menghadapi tantangan signifikan dalam mengelola karyawan, terutama berkaitan dengan tingginya tingkat pergantian karyawan (attrition rate). Saat ini attrition rate tercatat mencapai 17%. Kondisi ini dapat berdampak negatif terhadap kinerja operasional, efektivitas tim, dan biaya rekrutmen yang semakin meningkat.

Untuk mengatasi hal ini, departemen Human Resources (HR) berinisiatif memanfaatkan pendekatan berbasis data untuk memahami faktor-faktor yang menyebabkan tingginya attrition rate. Dengan mengidentifikasi akar penyebabnya, diharapkan perusahaan dapat merumuskan strategi intervensi yang lebih tepat demi mempertahankan dan meningkatkan kepuasan kerja karyawan.

### Permasalahan Bisnis
Permasalahan bisnis yang akan diselesaikan dalam proyek ini adalah sebagai berikut.
1. Tingginya attrition rate yang menunjukkan ketidakstabilan tenaga kerja dan berdampak pada efisiensi operasional.
2. Ketidakmampuan perusahaan dalam mengidentifikasi faktor-faktor utama yang memicu keputusan karyawan untuk mengundurkan diri.
3. Kurangnya alat bantu analitik berupa dashboard yang dapat digunakan oleh manajer HR untuk melakukan pemantauan secara terhadap kondisi tenaga kerja dan indikator yang berhubungan dengan attrition.
4. Keterbatasan dalam pengambilan keputusan berbasis data, khususnya dalam menyusun kebijakan retensi karyawan yang efektif.

### Cakupan Proyek

Proyek ini mencakup beberapa tahap utama yaitu sebagai berikut.

1. Data Understanding dan Preprocessing: Memahami struktur dan kualitas data attrition perusahaan Jaya Jaya Maju. Setelah memahami dan mengidentifikasi kecacatan dalam data selanjutnya dilakukan pembersihan data, transformasi fitur, penyeimbangan data dan penanganan nilai hilang.
2. Modeling: Mengembangkan model prediktif untuk mengidentifikasi faktor-faktor utama yang mempengaruhi keputusan karyawan untuk keluar.
3. Pembuatan Business Dashboard: Mendesain dan membangun dashboard interaktif yang dapat menampilkan indikator attrition secara visual, serta mendukung pengambilan keputusan HR berdasarkan data yang ada.
4. Insight dan Rekomendasi: Memperoleh insight berbasis data dan memberikan rekomendasi konkret (recommendation action item) untuk menurunkan tingkat attrition.

### Persiapan

Sumber data: Dataset yang digunakan pada proyek ini merupakan data karyawan perusahaan Jaya Jaya Maju yang dapat diakses melalui [Data Employee Jaya Jaya Maju]("https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/refs/heads/main/employee/employee_data.csv"). 

Dataset ini berisi data karyawan di perusahaan Jaya Jaya Maju. Dataset ini terdiri dari 35 fitur dan 1470 entry data. Berikut fitur yang terdapat dalam dataset: 
1. `EmployeeId`: Nomor identifikasi unik karyawan
2. `Age`: Usia karyawan
3. `Attrition`: Data ini menyatakan apakah karyawan melakukan attrition (resign atau diberhentikan).
Attrition = 0 → Karyawan masih bekerja
Attrition = 1 → Karyawan sudah keluar (attrisi terjadi)
4. `BusinessTravel`: Kolom ini berisi data seberapa sering karyawan melakukan perjalanan bisnis untuk pekerjaannya
5. `DailyRate`: Data berupa gaji harian karyawan
6. `Department`: Data rupa nama departemen tempat karyawan bekerja
7. `DistanceFromHome`: Jarak dari rumah karyawan ke kantor dalam satuan kilometer (km)
8. `Education`: Data ini menunjukkan tingkat pendidikan karyawan
9. `EducationField`: Data berupa jurusan dalam pendidikan karyawan
10. `EmployeeCount`: Menyatakan jumlah dari karyawan
11. `EnvironmentSatisfaction`: Tingkat kepuasan karyawan terhadap lingkungan pekerjaan
12. `Gender`: Jenis kelamin karyawan
13. `HourlyRate`: Gaji per jam
14. `JobInvolvement`: Tingkat keterlibatan atau komitmen karyawan
15. `JobLevel`: Tingkatan atau level jabatan karyawan dalam organisasi
16. `JobRole`: Peran atau jabatan dalam pekerjaan
17. `JobSatisfaction`: Tingkat kepuasan kerja karyawan terhadap pekerjaannya
18. `MaritalStatus`: Status pernikahan
19. `MonthlyIncome`: Total penghasilan bulanan aktual (termasuk tunjangan, bonus, dsb)
20. `MonthlyRate`: Gaji per bulan
21. `NumCompaniesWorked`: Jumlah perusahaan tempat karyawan bekerja
22. `Over18`: Menyatakan apakah karyawan diatas 18 tahun.
23. `OverTime`: Menunjukkan apakah seorang karyawan sering bekerja lembur atau tidak
24. `PercentSalaryHike`: Persentase kenaikan gaji dari tahun sebelumnya
25. `PerformanceRating`: Tingkat kinerja karyawan
26. `RelationshipSatisfaction`: Tingkat kepuasan karyawan terdapat relasi dengan karyawan lainnya
27. `StandardHours`: Jam kerja standar bulanan
28. `StockOptionLevel`: Menunjukkan tingkatan opsi saham yang diberikan kepada karyawan oleh perusahaan
29. `TotalWorkingYears`: Total pengalaman kerja karyawan dalam satuan tahun
30. `TrainingTimesLastYear`: Jumlah pelatihan yang diikuti pada tahun sebelumnya
31. `WorkLifeBalance`: Tingkat keseimbangan antara pekerjaan dan kehidupan pribadi
32. `YearsAtCompany`: Jumlah total tahun karyawan telah bekerja di perusahaan Jaya jaya maju
33. `YearsInCurrentRole`: Jumlah tahun karyawan berada di posisi/jabatan saat ini
34. `YearsSinceLastPromotion`: Jumlah tahun sejak karyawan terakhir kali mendapatkan promosi
35. `YearsWithCurrManager`: Jumlah tahun karyawan bekerja di bawah manajer yang sekarang

**Setup environment:**
Berikut langkah-langkah untuk mempersiapkan environment:
1. Menjalankan Notebook
- Jika menggunakan Anaconda, jalankan perintah berikut:
    ```
    conda create --name main-ds python=3.9
    conda activate main-ds
    pip install -r requirements.txt
    ```
- Jika menggunakan Shell/Terminal, jalankan perintah berikut:
    ```
    pip install pipenv
    pipenv install
    pipenv shell
    pip install -r requirements.txt
    ```
    
-  Jalankan file `notebook.ipynb` untuk melihat seluruh hasil analisis data beserta insight yang diperoleh dari data. Anda dapat menggunakan Jupyter notebook atau IDE lokal lainnya, atau anda dapat memanfaatkan IDE lain seperti Google Collab jika ingin menjalanakan proyek secara online.

2. Menjalankan Dashboard
- Jalankan perintah berikut pada Terminal/Command Prompt/PowerShell guna memanggil (pull) Docker image untuk menjalankan Metabase.
    ```
    docker pull metabase/metabase:v0.46.4
    ```

- Apabila proses pembuatan docker image telah selesai, Anda dapat menjalankan image tersebut menggunakan perintah berikut.
    ```
    docker run -p 3000:3000 --name metabase metabase/metabase
    ```

- Login ke metabase menggunakan email dan password berikut
    ```
    email: root@mail.com
    password: root123
    ```
## Business Dashboard

Employee Attrition Risk Dashboard dirancang untuk membantu departemen HR dalam melakukan analisis dan monitoring attrition karyawan di perusahaan Jaya Jaya Maju.
Dashboard ini menampilkan:
1. Ringkasan jumlah karyawan, dengan total 1059 karyawan, 179 di antaranya telah keluar (attrition), dan 9 karyawan diprediksi memiliki risiko tinggi untuk attrition.
2. Pie chart perbandingan persentase karyawan yang keluar dan bertahan.
3. Diagram batang yang menampilkan 10 fitur paling berpengaruh terhadap risiko attrition, dengan faktor utama seperti lembur (overtime) dan penghasilan bulanan (monthly income).
4. Distribusi attrition berdasarkan kategori seperti gender, status pernikahan, usia, penghasilan, overtime, job role, dan departemen.

Pada dashboard diperoleh hasil analisis sebagai berikut.
1. Karyawan laki-laki dan berstatus single lebih sering mengalami attrition.
2. Attrition lebih tinggi pada karyawan dengan gaji rendah hingga menengah (2.000–8.000 dolar) dan usia di bawah 37 tahun.
3. Karyawan yang lembur cenderung lebih banyak keluar.
4. Job role seperti Laboratory Technician, Research Scientist, dan Sales Executive memiliki attrition tinggi.
5. Departemen Research & Development serta Sales mencatat attrition terbanyak.
6. Tren risiko attrition menunjukkan kecenderungan tinggi pada karyawan dengan pengalaman kerja <5 tahun dan penghasilan rendah.

Dashboard juga dilengkapi dengan tabel data karyawan aktif beserta prediksi risiko attrition masing-masing karyawan.

Untuk mengakses dashboard menggunakan metabase dengan terlebih dahulu menjalankannya melalui Docker. Kemudian Login dengan Username:root@mail.com dan Password: root123

## Conclusion

Pada proyek ini telah dilakukan analisis data untuk menentukan faktor-faktor apa saja yang mempengaruhi angka Attrition (keluar atau resign) karyawan pada perusahaan Jaya Jaya Maju/ Selain itu, dilakukan pelatihan model untuk prediksi kemungkinan karyawan melakukan attrition.

#### 1. Faktor-faktor yang Mempengaruhi Attrition
A.   Overtime

  Karyawan yang sering bekerja lembur menunjukkan kecenderungan lebih tinggi untuk meninggalkan perusahaan.

B.   JobRole

  Beberapa posisi atau departemen tertentu menunjukkan tingkat attrition yang lebih tinggi dibandingkan yang lain.


C.  MaritalStatus

  Status pernikahan karyawan turut berkontribusi, meskipun tidak sekuat faktor lain. Data menunjukkan karyawan dengan status menikah adalah yang memiliki frekuensi attrition tertinggi.

D.   Total Working Year

  Pengalaman kerja total secara keseluruhan berkorelasi negatif terhadap attrition. Karyawan dengan pengalaman kerja yang panjang cenderung lebih stabil, memiliki loyalitas lebih tinggi, dan telah melewati fase pencarian kerja awal. Mereka biasanya juga lebih beradaptasi dalam lingkungan organisasi.

E.   Age

  Karyawan yang lebih tua cenderung lebih stabil dan jarang mengundurkan diri dibandingkan yang lebih muda.

F.  JobLevel, MonthlyIncome, StockOptionLevel

Faktor jabatan, pendapatan bulanan, dan opsi saham menunjukkan hubungan kuat terhadap kemungkinan bertahannya seorang karyawan. Karyawan dengan jabatan tinggi, penghasilan besar, serta kepemilikan saham memiliki insentif finansial dan emosional yang kuat untuk tetap tinggal.

#### 2. Pelatihan Model Prediksi
Model terbaik yang digunakan dalam proyek ini adalah XGBoost, dengan hasil evaluasi berikut:

-   Accuracy: 0.820755
-   Precision: 0.466667
-   Recall: 0.388889
-   F1-Score: 0.424242

Model XGBoost merupakan model terbaik dengan akurasi tertinggi dibandingkan dengan model lain seperti Logistic Regression dan Random Forest. Meskipun model XGBoost menunjukkan akurasi yang tinggi (82.07%), yang berarti sebagian besar prediksi sudah tepat secara keseluruhan, terdapat kekurangan pada nilai recall (38.88%). Hal ini menunjukkan bahwa model masih cukup hati-hati dalam mendeteksi karyawan yang benar-benar resign, sehingga beberapa kasus pengunduran diri mungkin terlewatkan.

### Rekomendasi Action Items (Optional)

Berikut beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.

1.   Karyawan yang sering lembur (OverTime=Yes) cenderung lebih tinggi resiko Attrition (Resign), sehingga perlu melakukan evaluasi kebijakan lembur dan pastikan beban kerja tetap dalam batas wajar. Selain itu Perusahaan perlu mempertimbangkan untuk memberikan kompensasi, istirahat, atau fleksibilitas bagi karyawan yang bekerja lembur.
2.   Beberapa JobRole seperti LaboratoryTechnician, ResearchScientist dan SalesExecutive memiliki tingkat attrition yang tinggi. Perusahaan perlu melakukan tinjauan mengenai alasan karyawan pada divisi tersebut secara lebih intens mungkin melalui wawancara internal. Perusahaan memberikan dukungan lebih, pelatihan, atau jalur promosi untuk role tersebut.
3. karyawan dengan usia muda dan Total Working Years yang sedikit memiliki tingkat attrition tinggi, kemungkinan karena karyawan merasa kurang berkembang pada perusahaan saat ini. Perlu dibuat program mentoring dan pengembangan karier untuk karyawan muda dan baru.
4. Perusahaan dapat mempertimbangkan penggunaan AI untuk monitoring prediksi attrition karyawan. Untuk mempertimbangkan solusi pengurangan jumlah attrition dengan pendekatan proaktif terhadap karyawan yang diprediksi berisiko keluar, misalnya diskusi 1-on-1, survei kepuasan, atau program retensi.
