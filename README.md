# Weather Classification MLOps Project 🌤️

โปรเจค Machine Learning Operations (MLOps) สำหรับการจำแนกสภาพอากาศจากภาพถ่าย พัฒนาสำหรับรายวิชา CP413008

## 📋 รายละเอียดโปรเจค

โปรเจคนี้เป็นระบบ MLOps แบบครบวงจรสำหรับการจำแนกสภาพอากาศ 4 ประเภท:
- ☀️ **Sunny** (แสงแดด)
- ☁️ **Cloudy** (มีเมฆ)
- 🌧️ **Rainy** (ฝนตก)
- 🌫️ **Foggy** (หมอก)

## 🚀 คุณสมบัติหลัก

- **MLflow Tracking**: ติดตามการทดลองและผลลัพธ์โมเดล
- **CI/CD Pipeline**: อัตโนมัติการทดสอบและ deployment
- **Data Validation**: ตรวจสอบคุณภาพข้อมูลอัตโนมัติ
- **Model Registry**: จัดการเวอร์ชันโมเดลและ deployment
- **Comprehensive Testing**: ทดสอบระบบครบถ้วน

## 📁 โครงสร้างโปรเจค

```
weather_classification_mlops/
├── .github/workflows/          # CI/CD pipeline
├── artifacts/                  # ผลลัพธ์และรายงาน
├── scripts/                    # สคริปต์ Python หลัก
│   ├── 01_data_validation.py   # ตรวจสอบข้อมูล
│   ├── 03_train_evaluate_register.py  # ฝึกและประเมินโมเดล
│   ├── 04_load_and_predict.py  # โหลดโมเดลและทำนาย
│   └── test_*.py              # สคริปต์ทดสอบ
├── DEMO_SCRIPT.md             # สคริปต์การนำเสนอ
├── PRESENTATION_SLIDES.md     # สไลด์นำเสนอ
├── PROJECT_REPORT.md          # รายงานโปรเจค
└── requirements.txt           # Dependencies
```

## 🛠️ การติดตั้งและใช้งาน

### 1. Clone Repository
```bash
git clone https://github.com/Orimsaa/ml_projectV1.git
cd weather_classification_mlops
```

### 2. ติดตั้ง Dependencies
```bash
pip install -r requirements.txt
```

### 3. เตรียมข้อมูล
วางไฟล์ภาพในโฟลเดอร์ตามโครงสร้าง:
```
data/
├── sunny/
├── cloudy/
├── rainy/
└── foggy/
```

### 4. รันการตรวจสอบข้อมูล
```bash
python scripts/01_data_validation.py
```

### 5. ฝึกโมเดล
```bash
python scripts/03_train_evaluate_register.py
```

### 6. ทดสอบการทำนาย
```bash
python scripts/04_load_and_predict.py
```

## 📊 MLflow Tracking

เปิด MLflow UI เพื่อดูผลการทดลอง:
```bash
mlflow ui
```
จากนั้นเปิดเบราว์เซอร์ไปที่ `http://localhost:5000`

## 🧪 การทดสอบ

รันการทดสอบทั้งหมด:
```bash
python scripts/test_complete_api.py
python scripts/test_model_loading.py
```

## 📈 ผลลัพธ์

โปรเจคนี้ได้รับผลลัพธ์:
- **Accuracy**: ~85-90% บนชุดข้อมูลทดสอบ
- **MLflow Integration**: ติดตามการทดลอง 100+ runs
- **Automated Pipeline**: CI/CD ทำงานอัตโนมัติ
- **Model Registry**: จัดการโมเดลหลายเวอร์ชัน

## 🔧 เทคโนโลยีที่ใช้

- **Python 3.8+**
- **TensorFlow/Keras**: สำหรับ Deep Learning
- **MLflow**: สำหรับ ML Lifecycle Management
- **GitHub Actions**: สำหรับ CI/CD
- **NumPy, Pandas**: สำหรับจัดการข้อมูล
- **Matplotlib, Seaborn**: สำหรับ Visualization

## 📝 เอกสารเพิ่มเติม

- [📋 Demo Script](DEMO_SCRIPT.md) - สคริปต์การนำเสนอ 15 นาที
- [📊 Presentation Slides](PRESENTATION_SLIDES.md) - สไลด์นำเสนอ
- [📖 Project Report](PROJECT_REPORT.md) - รายงานโปรเจคฉบับสมบูรณ์

## 👥 ทีมพัฒนา

โปรเจคนี้พัฒนาโดยนักศึกษารายวิชา CP413008 - Machine Learning Operations

## 📄 License

โปรเจคนี้เป็น Open Source ภายใต้ MIT License

---

⭐ **หากโปรเจคนี้มีประโยชน์ อย่าลืม Star ให้ด้วยนะครับ!** ⭐