
# Data Architect

## Overview
**Data Architect** is a Colab-based application designed to simplify and enhance dataset generation tasks using an intuitive Gradio UI. The project offers two distinct notebooks:  
1. **data_architect.ipynb**: 
    - Provides a general-purpose dataset generator with user-defined fields, formats, and values.  
2. **data_architect_multishot.ipynb**: 
    - Leverages a multishot approach, allowing users to provide examples to guide the generation process and improve dataset realism and context.

These tools enable users to customize, generate, and manage datasets effortlessly while integrating advanced models and tools for preprocessing, visualization, and storage. With Google Drive integration, users can ensure persistent storage and efficient workflows.

---

## Features
- **Two Notebooks for Dataset Generation**:
  - General-purpose dataset generator (`data_architect.ipynb`).
  - Multishot example-based generator (`data_architect_multishot.ipynb`).
- **Dataset Customization**: Define fields, formats, and example values to tailor synthetic datasets to specific needs.
- **Gradio User Interface**: Simple, interactive UI for intuitive dataset creation and management.
- **Model Integration**: Seamlessly works with Hugging Face `transformers` and OpenAI's API for data generation.
- **Google Drive Integration**: Enables persistent storage of datasets and models across sessions.
- **Preprocessing and Export**: Includes tools for preprocessing, visualization, and exporting datasets.

---

## Setup 

### Clone the Repository
```bash
git clone https://github.com/emads22/Data-Architect.git
cd Data-Architect
```

### Open the Notebooks in Colab
- **[data_architect.ipynb](https://colab.research.google.com/drive/1TilvUxshUfbSCQDZ8ps2to5OrtIrYWWC)**  
- **[data_architect_multishot.ipynb](https://colab.research.google.com/drive/16j09NYKs9FPTreZELs9z8wKmXLiDtN_C)**

### Configure Runtime
1. Open the desired Colab notebook.
2. Go to `Runtime` > `Change runtime type`.
3. Select `GPU` (preferably `T4` or higher) and connect to the runtime.

### Install Dependencies
Run the following command to install the required libraries:
```bash
!pip install -q requests torch bitsandbytes transformers sentencepiece accelerate openai httpx==0.27.2 gradio
```

### Mount Google Drive
```python
from google.colab import drive
drive.mount("/content/drive")
```

### Set Up API Keys
```python
from huggingface_hub import login
login("your-hugging-face-token")
```

### Configure Storage Directory
For persistent storage:
```python
DRIVE_DIR = "/content/drive/MyDrive"
DRIVE_MODELS_DIR = DRIVE_DIR + "/my_models"
```
For temporary storage:
```python
DRIVE_DIR = "/content"
DRIVE_MODELS_DIR = DRIVE_DIR + "/my_models"
```

---

## Usage
1. **Open the Gradio UI**:
   - Launch the Gradio interface by running the notebook.
   - Specify dataset fields, formats, examples, and the number of samples.

2. **Generate and Customize**:
   - Use `data_architect.ipynb` for general customization.
   - Use `data_architect_multishot.ipynb` to provide multiple examples and refine dataset generation.

3. **Export and Save**:
   - Copy the dataset directly from the Gradio interface.
   - Save datasets and models to Google Drive for future use.

4. **Preprocess and Visualize**:
   - Leverage preprocessing and visualization tools to prepare datasets for machine learning pipelines.

---

## Contributing
Contributions are welcome! Here are some ways you can contribute to the project:
- Report bugs and issues.
- Suggest new features or improvements.
- Submit pull requests with bug fixes or enhancements.

---

## Author
- **Emad**  
  [<img src="https://img.shields.io/badge/GitHub-Profile-blue?logo=github" width="150">](https://github.com/emads22)

---

## License
This project is licensed under the MIT License, which grants permission for free use, modification, distribution, and sublicense of the code, provided that the copyright notice (attributed to [emads22](https://github.com/emads22)) and permission notice are included in all copies or substantial portions of the software. This license is permissive and allows users to utilize the code for both commercial and non-commercial purposes.

Please see the [LICENSE](LICENSE) file for more details.



