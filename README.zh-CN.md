<div align="center">

[**English**](README.md)

</div>

---

# Obsidian Ollama 插件 (中文及Qwen3:8B 特别版)

本项目基于原版 [Obsidian Ollama 插件](https://github.com/your-original-plugin-repo-link) 进行修改，旨在提供更好的中文支持并优化对Qwen3:8B模型的集成。

## 项目简介

原版 Obsidian Ollama 插件是一个非常实用的工具，它允许用户直接在 Obsidian 笔记软件中与本地运行的 Ollama 模型进行交互。然而，在使用过程中发现其对中文 Prompt 的支持不够理想，且对如通义千问 Qwen3:8B 这类新兴模型在输出格式上可能存在一些不便。

本修改版本针对这些问题进行了优化，特别加强了对中文 Prompt 的原生支持，并对 Qwen3:8B 模型的输出进行了后处理，**默认移除了其内部的思考过程**，使输出更简洁直观，更适合在笔记中使用。

**注意:** 本插件依赖于你在本地正确安装并运行了 Ollama 服务，并且已经下载了你想要使用的模型（例如 `qwen:8b`）。

## 主要特性

* **原生中文 Prompt 支持:** 优化了插件与 Ollama 交互时对中文 Prompt 的处理，确保中文输入能被正确传递和理解。
* **优化支持通义千问 Qwen3:8B 模型:** 对接并测试了 Qwen3:8B 模型，确保其能在插件中稳定使用。
* **过滤 Qwen3:8B 模型输出:** 自动识别并移除 Qwen3:8B 模型输出中通常包含的内部思考过程（例如 `` 或类似的标记），只保留最终的生成文本。

## 安装教程

本插件的安装方式与标准的 Obsidian 第三方插件类似，但由于是修改版本，你需要手动安装：

1.  **找到你的 Obsidian 文件库（Vault）路径：** 这是你存储所有 Obsidian 笔记的文件夹。
2.  **进入 `.obsidian` 文件夹：** 在你的文件库路径下，找到一个名为 `.obsidian` 的隐藏文件夹。如果看不到，请确保你的操作系统设置中允许显示隐藏文件。
3.  **进入 `plugins` 文件夹：** 在 `.obsidian` 文件夹内，找到或创建一个名为 `plugins` 的文件夹。
4.  **下载并放置本项目文件：**
    * **方法 A (推荐 - 使用 Git):** 在 `plugins` 文件夹内打开终端或命令行，运行以下命令克隆本项目仓库：
        ```bash
        git clone [https://github.com/steppp1/Obsidian-ollama-plugin.git](https://github.com/steppp1/Obsidian-ollama-plugin.git)
        ```
        这会在 `plugins` 文件夹下创建一个名为 `Obsidian-ollama-plugin` 的子文件夹，并将本项目文件下载到其中。
    * **方法 B (手动下载):** 前往本项目的 GitHub 页面，点击绿色的 "Code" 按钮，选择 "Download ZIP"。下载完成后，将 ZIP 文件解压。你会得到一个文件夹（通常是 `Obsidian-ollama-plugin-master` 或类似名称），将这个文件夹完整地复制或移动到你文件库的 `.obsidian/plugins/` 目录下。为了保持一致性，建议将文件夹名称重命名为 `Obsidian-ollama-plugin`。

5.  **在 Obsidian 中启用插件：**
    
    * 打开 Obsidian。
    * 进入 "设置" (Settings) -> "第三方插件" (Community plugins)。
    * 在 "已安装插件" (Installed plugins) 列表中找到 "Obsidian Ollama Plugin (Enhanced)" 或类似名称的插件。
    * 点击旁边的开关按钮启用该插件。

## 如何使用

1.  **确保 Ollama 服务正在运行** 并且你已经下载了所需的模型（如 `ollama pull qwen:8b`）。
2.  在 Obsidian 中启用本插件后，通常会在设置中出现 Ollama 插件的配置项。你可能需要在这里指定 Ollama 服务的地址（通常是 `http://localhost:11434`）以及你想默认使用的模型名称（例如 `qwen:8b`）。
3.  根据插件的设定（通常可以通过命令面板或快捷键触发），选择文本并运行 Ollama 命令（例如 "Complete text" 或 "Chat"）来与模型进行交互。

## 兼容性

本插件修改基于原版 Obsidian Ollama 插件的某个版本进行，并已在特定的 Obsidian 版本和 Ollama 环境下进行测试。虽然理论上应该兼容较新版本的 Obsidian 和 Ollama，但如果在特定环境中遇到问题，欢迎提交 Issue。

## 贡献

欢迎对此项目做出贡献！如果你发现 Bug 或有改进建议，请随时提交 Issue 或 Pull Request。

1.  Fork 本仓库。
2.  创建你的特性分支 (`git checkout -b feature/AmazingFeature`)。
3.  提交你的更改 (`git commit -m 'Add some AmazingFeature'`)。
4.  推送到分支 (`git push origin feature/AmazingFeature`)。
5.  打开一个 Pull Request。

## 致谢

感谢 [原版 Obsidian Ollama 插件](https://github.com/hinterdupfinger/obsidian-ollama) 的开发者们，他们的工作为本项目奠定了基础。

