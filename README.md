# Smart-Fridge-Recipe-Generator-

A Samsung PRISM worklet project that integrates multi-modal intelligence using object detection and LLMs for smart kitchen applications. The system identifies food items in a fridge image and suggests recipes using DeepSeek or Google Gemini 2.0 flash. YOLOv8 is used for custom object detection on fridge contents.

---
##  Demo Video Link

https://drive.google.com/file/d/1zEaJBVK8JOU1T1oBN5EW2yqbc7T3KKNl/view?usp=sharing

---
##  Dataset Link

https://drive.google.com/file/d/1FHhGNMO63nJtY8jz9_-KbWvx7ApGuSVa/view

---

## 🚀 Features

- 🧠 Multi-modal recipe generation using fridge images
- 🤖 Supports both **DeepSeek** and **Gemini 2.0**
- 🧊 Custom YOLOv8 training on fridge content dataset
- 📄 Environment file for managing API keys securely

---

## 🔧 Setup Instructions

### 1. Clone the Repository
```
git clone https://github.ecodesamsung.com/SRIB-PRISM/VIT_24LAI13VIT_GenAI_Multi_Modal_Intelligence.git
```
```
cd VIT_24LAI13VIT_GenAI_Multi_Modal_Intelligence
```
2. Create a Virtual Environment
```
python -m venv env
```
```
source env/bin/activate     # For Linux/macOS
```
```
env\Scripts\activate        # For Windows
```
3. Install Dependencies

```
pip install -r requirement.txt
```

🔑 Environment Variable Setup
Create a .env file in the root directory and include your API keys:
dotenv
```
GOOGLE_API_KEY= "your_google_gemini_key"
```

---
🧪 YOLOv8 Model Training Instructions

Open yolov8_model_training.ipynb in Jupyter or Colab.

Run all cells to: Load data, Configure training parameters, Train and validate the YOLOv8 model, Export the best weights

To save the fine-tuned model: model.save("best_yolov8_fridge_model.pt") #The trained model will be saved in the working directory.

---
🧠 Run the Multi-Modal Fridge Assistant
Choose your preferred LLM:

Using DeepSeek:
```
python mealgen_smart_fridge_using_deepseek.py
```
Using Google Gemini 2.0 Pro:
```
python mealgen_smart_fridge_using_gemini_2.py
```

Update the .env.

Update path of saved finetuned Yolo model.

Run any mealgen_smart_fridge_using_gemini_2.py or mealgen_smart_fridge_using_deepseek.py

In Terminal Type 
```
streamlit run project_file_name.py
```
Upload fridge interior image

Provide user preference and get recipe suggestions

---
📌 Notes
Ensure your YOLO model path has been changed in python file.

For best results, ensure fridge images are well-lit and clear.

---
👨‍💻 Authors

Hariharan R.B - M.Sc. Data Science | VIT


Sourabh Tiwari - Samsung R&D Institute | Bangalore,India
