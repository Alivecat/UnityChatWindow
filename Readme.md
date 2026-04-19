# 项目快速上手指南(中文)

---

## 🛠️ 环境要求与资源准备

* **Unity 版本**：本项目使用 **Unity 6000.0.31f1** 创建。
* **推荐字体**：**Noto Sans SC**
    * [Google Fonts 下载链接](https://fonts.google.com/noto/specimen/Noto+Sans+SC?preview.script=Hans)
    * *注：你也可以根据需要使用其他中文字体。*

---

## 1. 项目初始化与插件导入

1.  **创建项目**：新建一个本地 **UPR (Universal Project Report)** 项目。
2.  **资源导入**：
    * 将下载的资源文件复制到工程的 `Assets` 文件夹中。
    * 依次导入以下三个核心插件：
        * `DOTween`
        * `UniTask`
        * `Localization`
3.  **输入系统配置**：
    * 依次点击：`Project Settings` -> `Player` -> `Active Input Handling`。
    * 将选项改为 **Both**。
    * **注意**：修改后 Unity 会自动重启以应用设置。

---

## 2. 本地化配置 (Localization)

### 基础设置
1.  在 `Project Settings` -> `Localization` -> `Active Setting` 中点击添加 **Localization Settings**。
2.  在 `Available Locales` 中点击 **Add All**，确保 **Chinese (Simplified) (zh)** 和 **English (en)** 出现。

### Table 资源设置
1.  **Addressable 标记**：
    在 `Assets/Localization/Tables` 文件夹下，选中以下文件，并在 **Inspector** 面板左上角勾选 **Addressable**：
    * `AuthorMessageTable Shared Data` / `en` / `zh`
    * `PlayerMessageTable Shared Data` / `en` / `zh`

2.  **预加载 (Preload) 设置**：
    * 选中 `AuthorMessageTable`，点击 Inspector 中的 **Open In Table Editor**。
    * 在 Table 窗口中勾选 **Preload**。
    * 在 `Selected collection` 的 String Table 中，确保 `AuthorMessageTable` 和 `PlayerMessageTable` 均被勾选。

3.  **刷新资源**：
    * 右键点击 `Assets/Localization/Tables` 文件夹，选择 **Reimport**。

---

## 3. TextMesh Pro (TMP) 中文字体配置

1.  **导入 TMP 资源**：
    * 将下载的 `NotoSansSC-Regular`（或其他中文字体）放入工程。
    * **初次操作**：右键点击字体 `Create -> TextMeshPro -> Font Asset`。如果弹出 **Import TMP Essentials**，请点击导入，完成后重试。
2.  **生成 SDF 字体**：
    * 右键点击字体文件 -> `Create` -> `TextMeshPro` -> **Font Asset**。
    * 系统会自动生成对应的 `SDF` 字体资产。
3.  **替换字体资产**：
    * 在 `Prefab` 文件夹中找到以下组件：
        * `ChooseBox`
        * `TexBoxLeft`
        * `TextBoxRight`
    * 将这些 Prefab 下 `TextMeshPro - Text` 脚本中的 **Font Asset** 替换为新生成的 `SDF` 字体资产。

---

## 4. 运行 Demo

1.  **加载场景**：打开 `ChatWindowsSample` 场景。
2.  **启动**：点击 Editor 顶部的 **Play** 按钮。
3.  **交互说明**：
    * 点击画面右上角的 **方块图标** 弹出窗口。
    * 点击 **AddMessage** 按钮添加信息，验证 UI 和多语言字体显示是否正常。

---

# Project Quick Start Guide

---

## 🛠️ Prerequisites & Resources

* **Unity Version**: This project was created using **Unity 6000.0.31f1**. Please ensure your environment matches or exceeds this version.
* **Recommended Font**: **Noto Sans SC**
    * [Download from Google Fonts](https://fonts.google.com/noto/specimen/Noto+Sans+SC?preview.script=Hans)
    * *Note: You may use other Chinese fonts if preferred.*

---

## 1. Project Initialization & Plugin Setup

1.  **Create Project**: Create a new local **UPR (Universal Project Report)** project.
2.  **Import Assets**:
    * Copy the downloaded resource files into your project's `Assets` folder.
    * Import the following three core plugins:
        * `DOTween`
        * `UniTask`
        * `Localization`
3.  **Input System Configuration**:
    * Navigate to: `Project Settings` -> `Player` -> `Active Input Handling`.
    * Change the setting to **Both**.
    * **Note**: Unity will automatically restart to apply these changes.

---

## 2. Localization Configuration

### Basic Settings
1.  Go to `Project Settings` -> `Localization` -> `Active Setting` and click to add **Localization Settings**.
2.  In the `Available Locales` section, click **Add All**. Ensure **Chinese (Simplified) (zh)** and **English (en)** appear in the list.

### Table Asset Configuration
1.  **Mark as Addressable**:
    In the `Assets/Localization/Tables` folder, select the following files and check the **Addressable** box in the top-left of the **Inspector** panel:
    * `AuthorMessageTable` (Shared Data / en / zh)
    * `PlayerMessageTable` (Shared Data / en / zh)

2.  **Preload Settings**:
    * Select `AuthorMessageTable` and click **Open In Table Editor** in the Inspector.
    * In the Table Editor window, check the **Preload** box.
    * Under the `Selected collection` section, ensure both `AuthorMessageTable` and `PlayerMessageTable` string tables have **Preload** enabled.

3.  **Refresh Assets**:
    * Right-click the `Assets/Localization/Tables` folder and select **Reimport**.

---

## 3. TextMesh Pro (TMP) Font Setup

1.  **Import TMP Resources**:
    * Place the downloaded `NotoSansSC-Regular` (or your chosen font) into the project.
    * **First-time setup**: Right-click the font and select `Create -> TextMeshPro -> Font Asset`. If a prompt for **Import TMP Essentials** appears, click import and try again after completion.
2.  **Generate SDF Font**:
    * Right-click the font file -> `Create` -> `TextMeshPro` -> **Font Asset**.
    * The system will automatically generate an `SDF` font asset.
3.  **Replace Font Assets in Prefabs**:
    * Locate the following components in the `Prefab` folder:
        * `ChooseBox`
        * `TexBoxLeft`
        * `TextBoxRight`
    * In the `TextMeshPro - Text` component of these prefabs, replace the **Font Asset** with your newly generated `SDF` font asset.

---

## 4. Running the Demo

1.  **Load Scene**: Open the `ChatWindowsSample` scene.
2.  **Play**: Click the **Play** button at the top of the Unity Editor.
3.  **Interaction Instructions**:
    * Click the **Square Icon** in the top-right corner of the screen to open the window.
    * Click the **AddMessage** button to add information and verify that the UI and multi-language fonts are displaying correctly.

---
