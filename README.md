# **Wireless Breathing Rate Tracking**  

## **Purpose**  
The goal of this project is to **track a person's breathing rate wirelessly** using **CSI (Channel State Information)** and **true medical data** for accurate analysis.  

---  

## **Dataset**  

### **1. CSI (Channel State Information)**  
CSI data is collected from **Wi-Fi signals** and consists of:  
- **Amplitude**  
- **Phase**  
- **Timestamp**  
- **RSSI (Received Signal Strength Indicator)**  

### **2. True Data (Medical Device Readings)**  
- Breathing rate is also measured using a **medical device** that is directly connected to the body.  
- This serves as **ground truth data** to validate the CSI-based predictions.  

---  

## **Procedure**  

### **1. Experiment Setup**  
- The subject **sits in a controlled environment**.  
- A **Wi-Fi router** is placed **behind the subject**.  
- A **Wi-Fi chipset (ESP32, Picoscenes, or Nexmon)** is placed **in front of the subject**.  
- A **display unit** in front generates **Wi-Fi traffic** between the router and the chipset, enabling CSI data collection.  

### **2. Data Collection & Cleaning**  
- CSI data packets are continuously recorded as **Wi-Fi signals interact with the subject’s body movements**.  
- The collected data is **structured and cleaned** to remove **unwanted noise** before further processing.  

### **3. Data Processing & Model Training**  
- **Deep learning models** are designed based on the **amount and structure** of the collected data.  
- The models process both:  
  - **CSI Data** (wireless signal variations)  
  - **True Medical Data** (reference for accuracy)  
- This allows the system to **learn patterns in breathing rate fluctuations**.  

### **4. Model Deployment**  
- Once trained, the following components are **saved for deployment**:  
  - **Preprocessing pipeline** (to clean and format incoming data)  
  - **Scaler models** (to normalize data for real-time use)  
  - **Final trained deep learning model**  

This enables **real-time, wireless breathing rate tracking** without direct body contact.
