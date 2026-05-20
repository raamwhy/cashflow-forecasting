# Cashflow Forecasting 13 Weeks

Project ini berisi notebook, dataset, output, dan laporan forecasting cashflow 13 minggu ke depan menggunakan pendekatan:

- External dataset training
- Internal company inference
- Internal trend calibration
- Scenario analysis

## Main Notebook

- `cashflow_forecasting_13_weeks_final.ipynb`

Notebook ini adalah versi full yang berisi alur lengkap mulai dari data understanding, preprocessing, feature engineering, model training, direct forecast, internal trend calibration, scenario analysis, visualisasi, export output, sampai business summary.

## Repository Structure

- `dataset/` berisi data internal dan dataset external yang digunakan untuk training.
- `outputs/` berisi hasil forecast, model evaluation metrics, grafik, Excel output, dan Word report.
- `Cashflow Forecast Dashboard.pdf` dan `Cashflow Forecast Report.pdf` berisi hasil laporan dalam format PDF.
- `requirements.txt` berisi daftar library Python utama yang digunakan.

Folder `website/` tidak disertakan dalam push repository ini.

## Method Overview

1. Dataset external distandardisasi menjadi weekly cashflow.
2. Feature engineering dibuat menggunakan lag 4 minggu, rolling mean, dan week number.
3. Model regression dilatih untuk memprediksi next week inflow dan next week outflow.
4. Direct forecast dibuat secara recursive selama 13 minggu.
5. Forecast dikalibrasi menggunakan rata-rata netflow data aktual internal 4 minggu terakhir.
6. Hasil akhir disajikan dalam Base Case, Optimistic, dan Pessimistic Scenario.

## Notes

Forecast ini adalah estimasi berbasis model dan skenario, bukan angka pasti. Hasil tetap perlu divalidasi dengan informasi bisnis aktual seperti jadwal collection, pembayaran vendor, OPEX/O&M, dan kebutuhan working capital.
