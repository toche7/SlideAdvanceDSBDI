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


ปรับการสอนตาม  module 12-13

LLM
Demo ChatGPT create SQL
Demo ChatGPT do EDA
Groq
Chat with LLM (Groq)
Data Extraction with LLM (Groq)
	- sentiment analysis
	- entity recognition
Data Validation with LLM (Groq)
	- anomaly detection
	- causality analysis (ความเป็นเหตุเป็นผล)
Data Generation with LLM (Groq)
	- สร้างข้อมูลจำลอง (synthetic data)
Data Summarization with LLM (Groq)
	- สรุปข้อมูลเชิงสถิติ
	- สรุปข้อมูลเชิง narrative
Chatbot
## หัวข้อที่ควรรู้เพิ่มเติม (สำหรับ Module 12-13)
RAG (Retrieval-Augmented Generation)
Vector Database

## Lesson Plan (สำหรับคาบ 3 ชั่วโมง: Module 12-13)

### เป้าหมายของคาบ
- ให้ผู้เรียนเห็นว่า LLM ช่วยงาน Data Science ได้หลายช่วงของ workflow ไม่ใช่แค่ chat
- ให้ผู้เรียนทดลองใช้ LLM กับงาน SQL, EDA, extraction, validation, generation, summarization
- ให้ผู้เรียนเข้าใจภาพรวมของ chatbot, RAG และ vector database ในระดับใช้งาน

### โครงสอน 3 ชั่วโมง (ภาคบ่าย)

#### 1) Opening: LLM for Data Work (00:00-00:10)
- ปูภาพรวมว่า LLM ช่วยงานข้อมูลได้อะไรบ้าง: SQL, EDA, extraction, validation, summarization, chatbot
- ตั้งหลักคิดว่า AI เป็น data assistant ไม่ใช่ตัวแทนการคิด
- เป้าหมาย: ให้ผู้เรียนเห็นภาพรวมก่อนเข้าสู่ demo

#### 2) Demo ChatGPT Create SQL (00:10-00:30)
- ใช้โจทย์ business question ง่าย ๆ แล้วให้ LLM ช่วยสร้าง SQL
- สอนวิธีให้ schema, กำหนด output, และตรวจคำตอบที่ได้กลับมา
- เป้าหมาย: แปลงคำถามธุรกิจเป็น query ที่ใช้ได้จริง

#### 3) Demo ChatGPT Do EDA (00:30-00:50)
- ให้ LLM ช่วยอ่านผลจาก head(), info(), describe(), missing value summary
- ใช้ LLM ช่วยตั้ง hypothesis และช่วยสรุป insight เบื้องต้น
- เป้าหมาย: ให้ผู้เรียนเห็นว่า LLM ช่วยคิดต่อจากสถิติพื้นฐานได้

#### 4) Mini Theory: LLMs, Embeddings, Context (00:50-01:05)
- อธิบาย LLM แบบสั้น: token, context window, prompt, limitation
- เชื่อมไปสู่ embeddings ว่าใช้แทนข้อความเป็นเวกเตอร์เพื่อค้นหาเนื้อหาที่ใกล้กัน
- เป้าหมาย: ให้มี mental model พอสำหรับเข้าใจ RAG ช่วงท้าย

#### 5) Break (01:05-01:15)

#### 6) Chat with LLM (Groq) (01:15-01:30)
- สาธิตการใช้งาน LLM ผ่าน Groq เพื่อให้เห็นอีก workflow หนึ่งนอกเหนือจาก ChatGPT
- เน้นความเร็วในการตอบและการใช้ prompt เดียวกันกับหลายงาน
- เป้าหมาย: ให้เห็นความต่างระหว่าง web chat กับ platform/API-style usage

#### 7) Data Extraction with LLM (Groq) (01:30-01:50)
- งานที่สาธิต:
	- sentiment analysis
	- entity recognition
- ใช้ข้อความลูกค้าหรือ feedback จริงเป็นตัวอย่าง
- เป้าหมาย: เปลี่ยนข้อความอิสระให้เป็น structured output ที่ใช้วิเคราะห์ต่อได้

#### 8) Data Validation with LLM (Groq) (01:50-02:10)
- งานที่สาธิต:
	- anomaly detection
	- causality analysis (ความเป็นเหตุเป็นผล)
- ให้ LLM ช่วยตรวจ record ที่ผิดปกติและช่วยตั้งคำถามต่อว่าควรตรวจอะไรเพิ่ม
- เป้าหมาย: ใช้ LLM เป็นผู้ช่วยในงาน data quality และ reasoning เบื้องต้น

#### 9) Data Generation with LLM (Groq) (02:10-02:25)
- สาธิตการสร้างข้อมูลจำลอง (synthetic data) สำหรับ prototype หรือการทดลอง pipeline
- อธิบายข้อควรระวังเรื่อง realism, bias, privacy และการใช้แทนข้อมูลจริง
- เป้าหมาย: ให้ผู้เรียนรู้ว่า LLM ช่วยเร่งการทดลองได้ แต่ต้องใช้อย่างระวัง

#### 10) Data Summarization with LLM (Groq) (02:25-02:40)
- งานที่สาธิต:
	- สรุปข้อมูลเชิงสถิติ
	- สรุปข้อมูลเชิง narrative
- ใช้ผลลัพธ์จาก EDA หรือ model summary แล้วให้ LLM สรุปเป็นภาษาที่ผู้บริหารอ่านเข้าใจ
- เป้าหมาย: เปลี่ยน output เชิงเทคนิคให้เป็น insight ที่สื่อสารได้

#### 11) Chatbot Mini Demo (02:40-02:50)
- สาธิต chatbot แบบง่ายเพื่อให้เห็นปลายทางของการประกอบ LLM เป็นแอปพลิเคชัน
- เน้นว่า chatbot เป็นการรวมหลายองค์ประกอบ ไม่ใช่แค่ถาม-ตอบลอย ๆ
- เป้าหมาย: ให้ผู้เรียนเห็น end-to-end application view

#### 12) Wrap-up: RAG และ Vector Database (02:50-03:00)
- ปิดคาบด้วยภาพรวม RAG: Document -> Embedding -> Retrieve -> Generate
- อธิบายบทบาทของ vector database ในการเก็บ embeddings และค้นหาบริบทที่เกี่ยวข้อง
- เป้าหมาย: ให้ผู้เรียนรู้ next step ถ้าจะสร้าง chatbot จากเอกสารขององค์กร

### Workflow ที่ต้องการให้ผู้เรียนเห็น
- SQL -> EDA -> Extraction -> Validation -> Generation -> Summarization -> Chatbot
- ปิดท้ายด้วย RAG/Vector Database เป็นแนวทางต่อยอด

### Deliverable ที่เหมาะกับคาบนี้
- แต่ละกลุ่มออกแบบ prompt สำหรับ 1 งานจริงใน data workflow
- แต่ละกลุ่มสรุปว่า LLM ควรช่วยตรงไหนและต้องมี human verification ตรงไหน

### ข้อความหลักที่ต้องสื่อทั้งคาบ
- LLM ช่วยเร่งงานได้ แต่ต้องตรวจความถูกต้องเสมอ
- Prompt ที่ดีช่วยลดความคลุมเครือและเพิ่มคุณภาพ output
- งาน data จริงต้องคิดทั้ง accuracy, privacy, bias และ explainability

### หัวข้อเสริม ถ้ามีเวลาเพิ่ม
- RAG (Retrieval-Augmented Generation)
- Vector Database
- Deploy chatbot prototype แทนการ deploy ML model แบบทั่วไป เพื่อให้ theme ของคาบต่อเนื่องมากขึ้น






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


g

