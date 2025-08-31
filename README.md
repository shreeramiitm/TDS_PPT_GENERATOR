# TDS_PPT_GENERATOR
This repo is for bonus project 1 tools in Data Science
# GyaanSetu Deck: AI-Powered PPTX Generator

**GyaanSetu Deck** is a powerful tool that leverages large language models (LLMs) to automatically generate professional PowerPoint presentations from your text. This project, originally a bonus project for a Data Science course, provides a seamless way to transform raw text into visually appealing and well-structured presentations.



## 🌟 Key Features

* **Effortless Content to Slides**: Simply paste your text or markdown, and the application will intelligently structure it into a presentation with titles and bullet points.
* **Multi-Provider LLM Support**: Choose from a variety of leading LLM providers to power your presentation generation:
    * **AI Pipe (OpenRouter)**
    * **OpenAI**
    * **Gemini (Google)**
    * **Anthropic (Claude)**
* **Template-Driven Customization**: Maintain brand consistency and a professional look by using your own `.pptx` or `.potx` files as templates. The generated presentation will inherit the design, layouts, and styles from your template.
* **Smart Image Reuse**: Optionally reuse images from your template in the generated slides. The tool intelligently places the images to avoid overlapping with text.
* **Flexible Slide Control**: You have complete control over the length of your presentation. Specify the exact number of slides you need, from a concise summary to a detailed deep-dive (1 to 40 slides).
* **Intuitive Web Interface**: The application features a user-friendly, single-page web interface for a smooth and intuitive user experience.

## 🛠️ How It Works

The application is built with a modern Python backend using **FastAPI** and a vanilla **JavaScript** frontend. Here's a high-level overview of the process:

1.  **User Input**: The user provides text, guidance, and optional parameters through the web interface.
2.  **LLM-Powered Slide Planning**: The backend sends a request to the selected LLM provider with a carefully crafted prompt to structure the text into a JSON object representing the slides.
3.  **Presentation Generation**: The application uses the `python-pptx` library to create a new presentation. If a template is provided, it's used as the base.
4.  **Content Population**: The slide plan from the LLM is used to populate the presentation with titles and bullet points.
5.  **Image Handling**: If image reuse is enabled, images from the template are added to the corresponding slides in a non-overlapping manner.
6.  **Download**: The generated `.pptx` file is sent to the user for download.

## 🚀 Getting Started

Follow these steps to run the application locally:

1.  **Clone the Repository**:
    ```bash
    git clone [https://github.com/shreeramiitm/tds_ppt_generator.git](https://github.com/shreeramiitm/tds_ppt_generator.git)
    cd tds_ppt_generator
    ```

2.  **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Application**:
    ```bash
    uvicorn app:app --reload
    ```

4.  **Access the Web Interface**:
    Open your browser and navigate to `http://127.0.0.1:8000`.

## ⚙️ Configuration

To use the application, you'll need an API key for the LLM provider you want to use. You can enter the API key directly in the web interface.

## ☁️ Deployment

The project includes a `vercel.json` file, making it easy to deploy to **Vercel**. The configuration file is set up to handle the FastAPI application and serve the frontend.

## 🤝 Contributing

Contributions are welcome! If you have any ideas for improvements or new features, feel free to open an issue or submit a pull request.

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
