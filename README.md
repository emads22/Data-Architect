
# Data Architect

## Overview
**Data Architect** is a Colab-based application designed to streamline dataset generation tasks using an intuitive Gradio UI. It enables users to customize and generate datasets effortlessly while leveraging advanced models and tools for preprocessing and visualization. The project is tailored for tasks involving data preparation, model integration, and dataset customization, offering persistent storage via Google Drive for enhanced usability.

## Features
- **Dataset Customization**: Allows users to define fields, formats, and values for generating synthetic datasets.
- **Gradio User Interface**: Provides a simple and interactive UI for dataset creation and management.
- **Integration with Models**: Supports seamless integration with Hugging Face `transformers` and OpenAI's API for data generation tasks.
- **Google Drive Integration**: Enables persistent storage of models and datasets across sessions.
- **Preprocessing and Export**: Includes preprocessing, visualization, and dataset export functionalities for end-to-end data management.

## Setup and Installation
1. **Install Dependencies**:
   Run the following command to install the required libraries:
   ```bash
   !pip install -q requests torch bitsandbytes transformers sentencepiece accelerate openai httpx==0.27.2 gradio
   ```

2. **Mount Google Drive**:
   Mount Google Drive to the Colab environment for saving and accessing files:
   ```python
   from google.colab import drive
   drive.mount("/content/drive")
   ```

3. **Set Up API Keys**:
   Configure secrets for Hugging Face Hub and OpenAI:
   ```python
   from huggingface_hub import login
   login("your-hugging-face-token")
   ```

## Usage
1. **Customize Your Dataset**:
   - Open the Gradio UI and specify the required fields, number of samples, and example values.
   - Adjust parameters to fit your specific requirements.

2. **Generate Datasets**:
   - Use the Gradio interface to generate synthetic datasets based on your inputs.

3. **Export and Save**:
   - Save generated datasets and models to Google Drive for persistent storage or download them directly from the interface.

4. **Validate and Utilize**:
   - Review and validate the generated datasets for use in your data science or machine learning pipelines.

## Contributing
Contributions are welcome! Here are some ways you can contribute to the project:
- Report bugs and issues.
- Suggest new features or improvements.
- Submit pull requests with bug fixes or enhancements.

## Author
- **Emad**  
  [<img src="https://img.shields.io/badge/GitHub-Profile-blue?logo=github" width="150">](https://github.com/emads22)

## License
This project is licensed under the MIT License, which grants permission for free use, modification, distribution, and sublicense of the code, provided that the copyright notice (attributed to [emads22](https://github.com/emads22)) and permission notice are included in all copies or substantial portions of the software. This license is permissive and allows users to utilize the code for both commercial and non-commercial purposes.

Please see the [LICENSE](LICENSE) file for more details.
