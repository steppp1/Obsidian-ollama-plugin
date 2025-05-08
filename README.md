[简体中文](README.zh-CN.md)

# Obsidian Ollama Plugin (Enhanced for Chinese & Qwen3:8B)

This project is a modified version of the original [Obsidian Ollama Plugin](https://github.com/your-original-plugin-repo-link), aimed at providing better support for Chinese language and optimized integration for specific open-source models.

## Project Overview

The original Obsidian Ollama Plugin is a very useful tool that allows users to interact with a locally running Ollama service directly within the Obsidian note-taking software. However, limitations were found regarding native Chinese Prompt support and potentially inconvenient output formatting for certain emerging models like Qwen3:8B.

This modified version addresses these issues by specifically enhancing native Chinese Prompt support and implementing post-processing for the Qwen3:8B model's output to filter out its internal thinking process, resulting in cleaner and more direct text suitable for note-taking.

**Note:** This plugin requires you to have the Ollama service correctly installed and running on your local machine, and the desired model (e.g., `qwen:8b`) downloaded.

## Key Features

* **Native Chinese Prompt Support:** Optimized handling of Chinese Prompts when interacting with Ollama.
* **Optimized Support for Qwen3:8B Model:** Tested and integrated the Qwen3:8B model for stable usage within the plugin.
* **Filter Qwen3:8B Thinking Process:** Automatically identifies and removes internal thinking blocks (like `<thought>...</thought>` or similar) from the Qwen3:8B model's output, leaving only the final generated text.

## Installation Guide

Installing this modified plugin is similar to installing standard third-party Obsidian plugins, but requires manual steps:

1.  **Locate your Obsidian Vault path:** This is the main folder where your Obsidian notes are stored.
2.  **Navigate to the `.obsidian` folder:** Inside your vault path, find a hidden folder named `.obsidian`. You might need to enable showing hidden files in your operating system settings.
3.  **Navigate to the `plugins` folder:** Inside the `.obsidian` folder, find or create a folder named `plugins`.
4.  **Download and Place Project Files:**
    * **Method A (Recommended - Using Git):** Open your terminal or command prompt inside the `plugins` folder and clone this repository:
        ```bash
        git clone [https://github.com/steppp1/Obsidian-ollama-plugin.git](https://github.com/steppp1/Obsidian-ollama-plugin.git)
        ```
        This will create a new subfolder named `Obsidian-ollama-plugin` inside `plugins` and download the project files into it.
    * **Method B (Manual Download):** Go to this project's GitHub page, click the green "Code" button, and select "Download ZIP". After downloading, extract the ZIP file. You'll get a folder (usually named `Obsidian-ollama-plugin-master` or similar). Copy or move this entire folder into your vault's `.obsidian/plugins/` directory. It's recommended to rename the folder to `Obsidian-ollama-plugin` for consistency.

5.  **Enable the Plugin in Obsidian:**
    * Open Obsidian.
    * Go to "Settings" -> "Community plugins".
    * Find "Obsidian Ollama Plugin (Enhanced)" or similarly named plugin in the "Installed plugins" list.
    * Click the toggle switch next to it to enable the plugin.

## How to Use

1.  **Ensure your Ollama service is running** and you have the necessary models downloaded (e.g., `ollama pull qwen:8b`).
2.  After enabling the plugin in Obsidian, its settings should appear in the Settings menu. You may need to configure the Ollama service address (usually `http://localhost:11434`) and the default model name you wish to use (e.g., `qwen:8b`).
3.  Based on the plugin's configuration (often triggered via the command palette or hotkeys), select text and run an Ollama command (e.g., "Complete text" or "Chat") to interact with the model.

## Compatibility

This plugin modification is based on a specific version of the original Obsidian Ollama Plugin and has been tested in particular Obsidian and Ollama environments. While it should theoretically be compatible with newer versions, please report any issues you encounter in specific setups.

## Contributing

Contributions are welcome! If you find bugs or have suggestions for improvements, feel free to open an Issue or submit a Pull Request.

1.  Fork the repository.
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

## License

This project is a modification of the original plugin. Please refer to the original plugin's license information. It is also recommended to choose an appropriate open-source license for this project (e.g., MIT or Apache 2.0) and create a `LICENSE` file in the project root directory.

## Acknowledgements

Thanks to the developers of the [original Obsidian Ollama Plugin](https://github.com/your-original-plugin-repo-link) for their foundational work.

---

**Please note:** Replace `https://github.com/your-original-plugin-repo-link` with the actual GitHub repository link of the original Obsidian Ollama Plugin. If you don't know it, you can simply write "the original Obsidian Ollama Plugin".