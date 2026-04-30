# Datathon2026_TheGridbreakers_Ecoconut
<div align="center">
  <img src="https://vinuni.edu.vn/wp-content/uploads/2021/04/Logo-VinUni-1.png" width="200" alt="VinUni Logo" />

  <h1>🏆 DATATHON 2026: THE GRIDBREAKER</h1>
  <h3>📊 Nowcasting Doanh thu cho TMĐT Thời trang</h3>

  <p>
    <img src="https://img.shields.io/badge/Team-ECOCONUT-blue?style=for-the-badge" />
    <img src="https://img.shields.io/badge/Python-3.8+-yellow?style=for-the-badge&logo=python" />
    <img src="https://img.shields.io/badge/Model-LightGBM-green?style=for-the-badge" />
    <img src="https://img.shields.io/badge/R²-0.9106-success?style=for-the-badge" />
  </p>

  <p>
    <b>Giải pháp dự báo doanh thu & giá vốn theo thời gian thực cho doanh nghiệp thương mại điện tử tại Việt Nam</b>
  </p>
</div>

---

## 📖 Tổng quan dự án

Dự án xây dựng hệ thống **Nowcasting (dự báo tức thời)** nhằm dự đoán:

* 📈 **Revenue (Doanh thu)**
* 📉 **COGS (Giá vốn)**

ở mức **daily level**, phục vụ:

* lập kế hoạch tài chính
* quản lý tồn kho
* tối ưu vận hành TMĐT

💡 **Điểm mạnh nổi bật:**

* Kết hợp **historical transactions + external signals**
* Xử lý tốt **seasonality & volatility**
* Có **Explainable AI (SHAP)** giúp giải thích mô hình

---

## 📂 Cấu trúc dự án

| Thành phần             | Mô tả                            |
| ---------------------- | -------------------------------- |
| `viz_all/`             | 12 biểu đồ (EDA, Forecast, SHAP) |
| `DATATHON_Model.ipynb` | Pipeline hoàn chỉnh từ A → Z     |
| `submission.csv`       | Kết quả dự báo                   |
| `Report_Ecoconut.pdf`  | Báo cáo chuẩn NeurIPS            |

---

## 🧠 Phương pháp tiếp cận

### 🔹 1. Feature Engineering (100+ features)

**Time-based features**

* Ngày, tháng, tuần, mùa

**Fourier Seasonality**

* Sử dụng sin/cos để capture chu kỳ

**Time-series dynamics**

* Lag features
* Rolling mean
* Exponentially Weighted Mean (EWM)

**External signals**

* 🌐 Web traffic (Bounce Rate)
* 📦 Inventory (Fill Rate)

---

### 🔹 2. Mô hình dự báo

* **Model:** LightGBM Regressor
* **Target transformation:** Log-transform
* **Validation:** TimeSeriesSplit (3 folds)

📊 **Kết quả:**

* **MAE:** 347,014
* **R²:** 0.9106

➡️ Mô hình đạt độ chính xác cao và ổn định theo thời gian.

---

### 🔹 3. Explainable AI

Áp dụng **SHAP values** để:

* Xác định feature quan trọng
* Giải thích biến động doanh thu
* Hỗ trợ ra quyết định kinh doanh

---

## 🚀 Hướng dẫn chạy lại

### 1. Cài đặt thư viện

```bash
pip install pandas numpy matplotlib lightgbm shap scikit-learn kagglehub
```

### 2. Cấu hình Kaggle API

* Đặt file `kaggle.json` tại:

```
~/.kaggle/kaggle.json
```

### 3. Chạy pipeline

* Mở:

```
DATATHON_Model.ipynb
```

* Chọn:

```
Run All
```

Pipeline sẽ tự động:

* Load dữ liệu
* Feature engineering
* Train model
* Xuất file submission

---

## 📊 Highlights

* ✔️ 100+ engineered features
* ✔️ Time-series validation chuẩn
* ✔️ High interpretability (SHAP)
* ✔️ Pipeline fully reproducible

---

## 👥 Team ECOCONUT

| Thành viên                | Vai trò                      |
| ------------------------- | ---------------------------- |
| **Nguyễn Đức Huy**        | 🧠 Team Leader               |
| **Tạ Nguyễn Nghi Phương** | 📊 Data Analyst              |
| **Phan Thanh Trúc**       | ⚙️ Machine Learning Engineer |

---

## 🏁 Kết luận

Giải pháp không chỉ đạt hiệu suất cao trong bài toán dự báo mà còn đảm bảo:

* 🔍 **Minh bạch (Explainable)**
* ⚡ **Realtime-ready (Nowcasting)**
* 📦 **Ứng dụng thực tế cho doanh nghiệp TMĐT**

---

<div align="center">
  <h3>🔥 "Break the Grid – Forecast the Future"</h3>
</div>
