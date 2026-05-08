
### معلمات التدريب

| المعامل | القيمة | الشرح |
|---------|--------|-------|
| **Optimizer** | Adam | Adaptive Moment Estimation |
| **Learning Rate** | 0.001 | حجم الخطوة في التحديث |
| **Loss Function** | Sparse Categorical Crossentropy | مناسبة للتصنيف المتعدد |
| **Batch Size** | 32 | عدد العينات في كل تحديث |
| **Max Iterations** | 1500 | الحد الأقصى للتكرارات |
| **Early Stopping** | Enabled | يوقف التدريب عند plateau |
| **Patience** | 30 | عدد التكرارات بدون تحسن |
| **Validation Fraction** | 0.1 | 10% من التدريب للتحقق |
| **L2 Alpha** | 0.001 | قوة الـ Regularization |

---

## 📋 Knowledge Base (القواعد الخبيرة)

### القواعد الكاملة (22 قاعدة)

#### مجموعة 1: ضغط الدم (5 قواعد)

| القاعدة | الشرط | النقاط |
|---------|-------|--------|
| R01 | Hypertension Stage 2 | +4 |
| R02 | Hypertension Stage 1 | +3 |
| R03 | Elevated BP | +2 |
| R04 | Systolic BP ≥ 160 | +3 |
| R05 | Systolic BP ≥ 140 | +2 |

#### مجموعة 2: الكوليسترول (4 قواعد)

| القاعدة | الشرط | النقاط |
|---------|-------|--------|
| R06 | Total Cholesterol ≥ 240 | +2 |
| R07 | Total Cholesterol ≥ 200 | +1 |
| R08 | HDL < 40 | +2 |
| R09 | HDL < 60 | +1 |

#### مجموعة 3: سكر الدم (2 قاعدتين)

| القاعدة | الشرط | النقاط |
|---------|-------|--------|
| R10 | Fasting Blood Sugar ≥ 126 | +3 |
| R11 | Fasting Blood Sugar ≥ 100 | +1 |

#### مجموعة 4: تاريخ المريض (3 قواعد)

| القاعدة | الشرط | النقاط |
|---------|-------|--------|
| R12 | Diabetes = YES | +3 |
| R13 | Smoking = YES | +2 |
| R14 | Family History = YES | +2 |

#### مجموعة 5: BMI والعمر (5 قواعد)

| القاعدة | الشرط | النقاط |
|---------|-------|--------|
| R15 | BMI ≥ 35 | +2 |
| R16 | BMI ≥ 30 | +1 |
| R17 | Age ≥ 65 | +3 |
| R18 | Age ≥ 55 | +2 |
| R19 | Age ≥ 45 | +1 |

#### مجموعة 6: نمط الحياة (1 قاعدة)

| القاعدة | الشرط | النقاط |
|---------|-------|--------|
| R20 | Physical Activity = Low | +1 |

#### مجموعة 7: القواعد المركبة (2 قاعدتين)

| القاعدة | الشرط | النقاط |
|---------|-------|--------|
| COMBO1 | BP ≥ 160 AND Diabetes | +2 |
| COMBO2 | Cholesterol ≥ 240 AND Smoking | +2 |

---

## 📈 نتائج المشروع

### مقارنة النماذج

| النموذج | Test Accuracy | Precision | Recall | F1-Score |
|---------|---------------|-----------|--------|----------|
| **Expert Rules (Knowledge Base)** | 82.4% | 0.82 | 0.81 | 0.81 |
| **Neural Network (بدون Regularization)** | 88.7% | 0.88 | 0.87 | 0.87 |
| **Neural Network (مع Regularization)** | **94.2%** | **0.94** | **0.93** | **0.93** |
