Module 5: 
เทคนิค Machine Learning ระดับกลาง
 o ทบทวนแนวคิดพื้นฐานของ Supervised และ Unsupervised Learning
o อัลกอริทึมระดับกลาง เช่น
- Tree-based Models (Random Forest, XGBoost, Light GBM)
- Regularization Methods (Lasso, Ridge, Elastic Net)
- Clustering Techniques (K-means, DBSCAN)
- Dimensionality Reduction (PCA, 
t-SNE, UMAP)
Module 6: 
การประเมินแบบจำลองและการเลือกโมเดล
o Cross-validation และวิธีการแบ่งข้อมูล
o การเลือก Evaluation Metrics ให้เหมาะสม
o การจัดการข้อมูลไม่สมดุล (Imbalanced Data)
o การออกแบบ Feature Engineering Workflow

Module 12: 
Generative AI และ
การประยุกต์ใช้ในงานด้านข้อมูล
o ความเข้าใจพื้นฐาน LLMs และ Embeddings
o Vector Database และ Retrieval-Augmented Generation (RAG)
o การใช้ Generative AI ช่วยงาน Data Science เช่น
- การสร้าง SQL
- การทำ Exploratory Data Analysis (EDA)
- การสรุปข้อมูล
- การเสนอแนวคิด Feature Engineering
Module 13: 
กิจกรรมปฏิบัติ (Workshop)
o ทดลอง deploy โมเดล Machine Learning แบบง่าย
o ทดลองใช้ LLM ทำงานร่วมกับกระบวนการวิเคราะห์ข้อมูลจริง

## Section สรุปโมเดล (สำหรับคาบ 3 ชั่วโมง: Module 5-6)

### 1) Baseline Model: Logistic Regression
- เหมาะกับ: งานจำแนกประเภท (Classification) ที่ต้องการเริ่มจากโมเดลเข้าใจง่าย
- จุดเด่น: เทรนเร็ว, อธิบายได้ง่าย, ใช้เป็น baseline เพื่อเทียบโมเดลที่ซับซ้อนกว่า
- ข้อจำกัด: จับความสัมพันธ์ไม่เชิงเส้นได้จำกัด
- Metric ที่ควรดู: Precision, Recall, F1, ROC-AUC (ไม่ดู Accuracy อย่างเดียว)

### 2) Main Model: Random Forest
- เหมาะกับ: ข้อมูล tabular ที่มีความสัมพันธ์ซับซ้อนระดับหนึ่ง
- จุดเด่น: จับ non-linear ได้ดี, ทน noise ได้ดี, ให้ผลลัพธ์เสถียรกว่า tree เดี่ยว
- ข้อจำกัด: แปลผลยากกว่า baseline, ใช้เวลาเทรนมากขึ้น
- Metric ที่ควรดู: F1 และ ROC-AUC เทียบกับ baseline ด้วย cross-validation

### 3) Advanced Mention (แนวทางต่อยอด): XGBoost / LightGBM
- ใช้เมื่อ: ต้องการประสิทธิภาพสูงขึ้นจาก tree-based ensemble
- ในคาบ 3 ชั่วโมง: แนะนำเชิงแนวคิดและกรณีใช้งาน โดยไม่ลงรายละเอียด tuning เชิงลึก

### 4) Model Selection Logic (ที่ต้องสื่อให้ผู้เรียนเข้าใจ)
- ขั้นที่ 1: ตั้ง baseline ก่อนเสมอ
- ขั้นที่ 2: ลองโมเดลที่ซับซ้อนขึ้น (Random Forest)
- ขั้นที่ 3: ประเมินด้วย cross-validation และ metric ที่สอดคล้องโจทย์
- ขั้นที่ 4: ถ้าข้อมูลไม่สมดุล ให้ใช้ class_weight หรือปรับ threshold ก่อนสรุปผล

### 5) สรุปการเลือกโมเดลสำหรับสอนจริง
- ถ้าเวลา 3 ชั่วโมง: Logistic Regression + Random Forest + วิธีคิดเรื่อง XGBoost/LightGBM
- ถ้าเวลามากขึ้น: ค่อยเพิ่ม Hyperparameter Tuning และ Feature Engineering แบบเป็นระบบ

## Section สไลด์เสริม (ไม่สอนในคาบ แต่ควรรู้)

> วัตถุประสงค์: ใช้เป็นสไลด์ประกอบเพื่อให้ผู้เรียนเห็นภาพรวมครบ Module 5-6
> โดยผู้สอนอ้างอิงสั้นๆ ท้ายคาบ หรือให้เป็นเอกสารอ่านเพิ่มหลังเรียน

### A) Unsupervised Learning ที่ควรรู้
- K-means
	- แนวคิด: จัดกลุ่มจาก centroid
	- เหมาะเมื่อ: ต้องการ segmentation ที่ตีความง่าย
	- ข้อจำกัด: ต้องกำหนดจำนวนคลัสเตอร์ล่วงหน้า, ไวต่อ outliers
- DBSCAN
	- แนวคิด: จัดกลุ่มจากความหนาแน่นของข้อมูล
	- เหมาะเมื่อ: คลัสเตอร์รูปร่างไม่เป็นวงกลม, ต้องการแยก noise
	- ข้อจำกัด: ไวต่อการตั้งค่า eps และ min_samples

### B) Dimensionality Reduction (สำหรับเข้าใจภาพรวม)
- PCA: ลดมิติแบบเชิงเส้น เพื่อคงความแปรปรวนหลัก
- t-SNE: เน้น visualization โครงสร้างใกล้เคียงในมิติสูง
- UMAP: visualization เร็วขึ้นและมักรักษาโครงสร้าง global/local ได้ดี
- หมายเหตุสำหรับผู้เรียน: t-SNE/UMAP ใช้เพื่อสำรวจข้อมูล ไม่ใช่ metric หลักตัดสินโมเดล

### C) Regularization Methods (เสริมจาก supervised)
- Ridge (L2): ลดปัญหา overfitting โดย shrink ค่าน้ำหนัก
- Lasso (L1): ช่วยคัดเลือก feature เพราะบางค่าสัมประสิทธิ์อาจกลายเป็น 0
- Elastic Net: ผสม L1 + L2 เมื่อข้อมูลมี feature สัมพันธ์กัน

### D) Feature Engineering Workflow (เสริมแนวคิด)
- ขั้นตอนแนะนำ: Data cleaning -> Encoding/Scaling -> Feature creation -> Validation
- หลักสำคัญ: ทำ preprocessing ภายใน pipeline เพื่อลด data leakage

### E) Evaluation เสริมสำหรับงานไม่สมดุล
- PR Curve และ Average Precision
- แนวคิด cost-sensitive decision (ค่าเสียหายจาก FN/FP ไม่เท่ากัน)

### F) ข้อความกำกับบนสไลด์ (แนะนำใส่ทุกหน้าใน section นี้)
- "เนื้อหาส่วนเสริมเพื่อความครอบคลุม ไม่ใช่เนื้อหาปฏิบัติหลักของคาบ 3 ชั่วโมง"
