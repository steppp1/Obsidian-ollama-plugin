<div align="center">[**简体中文**](README.zh-CN.md)</div>

[简体中文](README.zh-CN.md)

# Obsidian Ollama Plugin (Enhanced for Chinese & Qwen3:8B)

This project is a modified version of the original [Obsidian Ollama Plugin](https://github.com/your-original-plugin-repo-link), aimed at providing better support for the Chinese language and optimized integration for the Qwen3:8B model.

## ✨ Project Overview

The original Obsidian Ollama Plugin is a fantastic tool that lets users interact directly with a locally running Ollama service within the Obsidian note-taking software. However, during use, it was found that its support for **Chinese Prompts** wasn't ideal, and for newer models like **Tongyi Qianwen Qwen3:8B**, the output format could be inconvenient, sometimes including internal thinking processes.

This modified version tackles these issues! It specifically strengthens **native Chinese Prompt support** and adds a "filter" for the Qwen3:8B output, by default removing the model's internal thinking process (like `` or similar markers). This results in cleaner output, making it more suitable for use in your notes.

**📌 Note:** Before using this plugin, please ensure you have the **Ollama service correctly installed and running** on your local machine, and that you have **downloaded the model you want to use** (e.g., by running `ollama pull qwen:8b`).

## 🚀 Key Features

-   **Seamless Chinese Prompt Handling:** Significantly optimized the plugin's logic for processing Chinese Prompts, ensuring your Chinese input is accurately passed to and understood by the Ollama model.
-   **Optimized Qwen3:8B Support:** Integrated and tested specifically with the Tongyi Qianwen Qwen3:8B model, ensuring stable operation within the plugin.
-   **Cleaner Output Filtering:** Automatically identifies and **by default removes** the internal thinking process often included in the Qwen3:8B model's output, leaving only the essential generated text.

## ⬇️ Installation Guide

Installing this plugin is similar to other third-party Obsidian plugins, but since it's a modified version, you'll need to install it manually:

1.  **Locate your Obsidian Vault path:** This is the main folder where you store all your Obsidian notes.
2.  **Navigate to the `.obsidian` folder:** Inside your vault path, find a **hidden folder** named `.obsidian`. If you can't see it, make sure your operating system settings are configured to show hidden files.
3.  **Navigate to the `plugins` folder:** Inside the `.obsidian` folder, find or create a folder named `plugins`.
4.  **Download and Place Project Files:**
    * **Method A (Recommended - Using Git):** Open your terminal or command prompt inside the `plugins` folder and clone this repository:
        ```bash
        git clone [https://github.com/steppp1/Obsidian-ollama-plugin.git](https://github.com/steppp1/Obsidian-ollama-plugin.git)
        ```
        This will create a subfolder named `Obsidian-ollama-plugin` inside `plugins` and download the project code into it.
    * **Method B (Manual Download & Extract):** Go to this project's GitHub page, click the green "Code" button, and select "Download ZIP". After downloading, extract the ZIP file. You'll get a folder (usually named something like `Obsidian-ollama-plugin-master`). Copy or move this **entire folder** into your vault's `.obsidian/plugins/` directory. For tidiness, it's recommended to rename the folder to `Obsidian-ollama-plugin`.
5.  **Enable the Plugin in Obsidian:**
    * Open your Obsidian app.
    * Go to "**Settings**" -> "**Community plugins**".
    * In the "**Installed plugins**" list, find the plugin named "**Obsidian Ollama Plugin (Enhanced)**" or similar.
    * Click the **toggle switch** next to it to turn it on!

## 💡 How to Use

1.  First, **ensure your Ollama service is running** in the background and you **have the required model downloaded** (e.g., `ollama pull qwen:8b`).
2.  After enabling the plugin in Obsidian, its settings should appear in the Obsidian settings menu. Here, you'll likely need to specify the Ollama service address (usually `http://localhost:11434`) and the **name of the model** you want to use by default (e.g., fill in `qwen:8b`).
3.  Then you're ready to go! Based on the plugin's configuration (often triggered via the **command palette** or a **hotkey**), select some text and run an Ollama-related command (like "**Complete text**" or "**Chat**") to have the model generate content for you.

## 🤝 Compatibility

This plugin modification is based on a specific version of the original Obsidian Ollama Plugin and has been tested in particular Obsidian and Ollama environments. While it should theoretically be compatible with newer versions, please feel free to open an Issue if you encounter any strange problems in your setup.

## 🙌 Contributing

Contributions are super welcome! If you find a bug or have cool ideas for improvements, feel free to open an Issue or submit a Pull Request.

1.  Start by Forking this repository.
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'Added an awesome feature'`).
4.  Push your branch to your Forked repository (`git push origin feature/AmazingFeature`).
5.  Finally, open a Pull Request to this repository!

## 📜 License

This project is a modification based on the original plugin. Please refer to the original plugin's license information. It's also recommended that you choose a suitable open-source license for this modified project (like **MIT** or **Apache 2.0**) and include a **LICENSE** file in the project root directory to state it clearly.

## 🙏 Acknowledgements

Huge thanks to the developers of the [original Obsidian Ollama Plugin](https://github.com/your-original-plugin-repo-link)! Their hard work laid the foundation for this project. Thank you!

---

**Quick Notes:**

* Please replace `https://github.com/your-original-plugin-repo-link` with the actual GitHub repository link of the original Obsidian Ollama Plugin. If you can't find the specific link, just writing "the original Obsidian Ollama Plugin" is fine.
* Ensure you have both `README.md` (English version) and `README.zh-CN.md` (Chinese version) files in your project root directory, and that the links at the top of each file correctly point to the other.
* Remember to choose an open-source license and create the `LICENSE` file!