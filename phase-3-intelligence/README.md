# 🧠 Phase 3 – AI + IoT Integration

This phase connects AI recommendation logic and IoT-based item pickup detection to enable a fully automated cashierless experience.

---

## 🤖 Azure ML – Product Recommendations

Trains a model to suggest items based on previous customer feedback.

- **Tool:** Azure Machine Learning  
- **Input Table:** `Feedback`  
- **Output Table:** `AIRecommendations`  
- **Logic:**  
  - Group feedback by user  
  - Identify top-rated categories  
  - Suggest new products within those categories  

---

## 📦 IoT – Product Shelf Tracking

Simulates Raspberry Pi sensors detecting item pickup events from shelves.

- **Platform:** Azure IoT Hub  
- **Simulator:** Python script or Azure Device Simulator  
- **Behavior:**  
  - Sends shelf item movement events (picked/returned)  
  - Maps product to shelf ID  
  - Triggers item detection logic in app  

---

✅ **Next Step**  
Create `ml-setup.md` to define model training, inputs/outputs, and deployment in Azure ML.
