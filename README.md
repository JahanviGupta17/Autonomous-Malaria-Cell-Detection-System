# Autonomous-Malaria-Cell-Detection-System

---

## 📊 Cell Categories Detected

- Red Blood Cell
- Leukocyte
- Gametocyte
- Ring
- Trophozoite
- Schizont
- Difficult

---

## 🧪 Technical Highlights

### ✅ Data Preparation
- Converted complex, nested JSON annotations into **COCO format**
- Verified annotation consistency, image metadata, and bounding box quality
- Registered datasets using `register_coco_instances` in Detectron2

### 📊 Exploratory Data Analysis (EDA)
- **Class distribution** bar plots
- **Bounding box** size and aspect ratio histograms
- Image size consistency check
- Insights used to rebalance samples and tune hyperparameters

### 🧠 Model Training (Faster R-CNN)
- Base config: `faster_rcnn_R_50_FPN_3x.yaml`
- Training on 7 cell types with Detectron2’s `DefaultTrainer`
- Loss functions monitored: `loss_cls`, `loss_box_reg`, `loss_rpn_cls`, `loss_rpn_loc`
- **Checkpointing every 1000 iterations**
- Custom visualization using Detectron2’s `Visualizer`

### 📈 Evaluation Metrics
- `fast_rcnn/cls_accuracy`: **94.3%**
- `fast_rcnn/fg_cls_accuracy`: **85.2%**
- False negatives reduced to **14.1%**
- **AUC-ROC Score**: 0.92
- **F2-Score**: 0.87
- **RMSE**: 0.31
- Real-time loss/accuracy plotted over 3,000 iterations


