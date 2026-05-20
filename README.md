# Cashflow Forecasting 13 Weeks

Project ini berisi notebook forecasting cashflow 13 minggu ke depan menggunakan pendekatan:

- External dataset training
- Internal company inference
- Internal trend calibration
- Scenario analysis

Data internal perusahaan dan output hasil forecasting tidak disertakan di repository ini karena bersifat lokal/sensitif. Untuk menjalankan notebook, siapkan file data sesuai path yang digunakan di notebook.

## Main Notebook

- `cashflow_forecasting_13_weeks_final_public.ipynb`

Notebook public ini sudah dibersihkan dari output cell agar angka data internal tidak ikut tersimpan di GitHub.

## Method Overview

1. Dataset external distandardisasi menjadi weekly cashflow.
2. Feature engineering dibuat menggunakan lag 4 minggu, rolling mean, dan week number.
3. Model regression dilatih untuk memprediksi next week inflow dan next week outflow.
4. Direct forecast dibuat secara recursive selama 13 minggu.
5. Forecast dikalibrasi menggunakan rata-rata netflow data aktual internal 4 minggu terakhir.
6. Hasil akhir disajikan dalam Base Case, Optimistic, dan Pessimistic Scenario.

## Notes

Forecast ini adalah estimasi berbasis model dan skenario, bukan angka pasti. Hasil tetap perlu divalidasi dengan informasi bisnis aktual seperti jadwal collection, pembayaran vendor, OPEX/O&M, dan kebutuhan working capital.

