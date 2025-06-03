# Sistem Prediksi Penyakit Kardiovaskular

Sistem machine learning yang memprediksi risiko penyakit kardiovaskular menggunakan neural network. Proyek ini mengimplementasikan model deep learning untuk menganalisis data kesehatan pasien dan memberikan penilaian risiko penyakit kardiovaskular.

## Gambaran Proyek
Sistem ini menggunakan neural network untuk memprediksi risiko penyakit kardiovaskular berdasarkan berbagai parameter kesehatan termasuk usia, jenis kelamin, pengukuran fisik, tekanan darah, kadar kolesterol, dan faktor gaya hidup.

## Informasi Dataset

| Kategori Data              | Fitur       | Deskripsi                        | Tipe Data      | Cara Input / Keterangan                                                |
| -------------------------- | ----------- | -------------------------------- | -------------- | ---------------------------------------------------------------------- |
| Mudah Diketahui          | age         | Usia dalam tahun                 | Integer        | Input langsung                                                         |
|                            | gender      | Jenis kelamin                    | Integer | Pilihan (0: Perempuan, 1: Laki-laki)                                   |
|                            | height      | Tinggi badan (cm)                | Integer        | Bisa diukur sendiri                                                    |
|                            | weight      | Berat badan (kg)                 | Float/Integer  | Bisa ditimbang sendiri                                                 |
| Perlu Pemeriksaan Medis | ap\_hi      | Tekanan darah sistolik           | Integer        | Perlu tensimeter                                                       |
|                            | ap\_lo      | Tekanan darah diastolik          | Integer        | Perlu tensimeter                                                       |
|                            | cholesterol | Kadar kolesterol                 | Integer | Perlu tes darah                                                        |
|                            | gluc        | Kadar gula darah                 | Integer | Perlu tes gula                                                         |
| Gaya Hidup              | smoke       | Status merokok                   | Integer | Input: Ya/Tidak (0: Tidak, 1: Ya)                                      |
|                            | alco        | Konsumsi alkohol                 | Integer | Input: Ya/Tidak (0: Tidak, 1: Ya)                                      |
|                            | active      | Aktivitas fisik rutin            | Integer | Input: Ya/Tidak (0: Tidak aktif, 1: Aktif); olahraga ≥150 menit/minggu |
| Target Variable         | cardio      | Prediksi penyakit kardiovaskular | Integer        | 0: Risiko Rendah, 1: Risiko Tinggi                                     |

## Penjelasan Output Prediksi

1. Probability (Probabilitas)

Tingkat kepercayaan model bahwa pasien memiliki risiko penyakit kardiovaskular (persen).

2. Prediction (Prediksi)

  - Low Risk: Probabilitas ≤ 50%
  - High Risk: Probabilitas > 50%

3. Risk Level (Tingkat Risiko)

  - Low: Probabilitas < 30% - Risiko minimal
  - Medium: Probabilitas 30-70% - Perlu pemantauan
  - High: Probabilitas > 70% - Perlu tindakan segera

## Proses
