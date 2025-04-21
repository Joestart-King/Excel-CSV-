Excel/CSV 手机号去重工具
一个简单易用的 GUI 工具，用于对比 Excel/CSV 文件中的手机号并去重，或者对文件进行乱序处理。支持动态选择手机号列，适用于数据清洗和随机化需求。
功能特性

手机号去重：通过基准文件对比，移除对比文件中重复的手机号行。
动态列选择：支持用户选择对比文件中的手机号列，适应不同文件结构。
乱序处理：支持对文件行进行随机重新排列，适用于仅需乱序的场景。
乱序开关：通过 Toggle Switch 控制导出文件是否随机排序。
支持格式：支持 .xls、.xlsx 和 .csv 文件格式。
用户友好：提供直观的 GUI 界面，包含进度条、状态提示和错误反馈。

界面预览
## 界面预览

![程序界面截图](images/screenshot.png)
安装步骤

克隆仓库：
git clone https://github.com/your-username/excel-deduplicate-tool.git
cd excel-deduplicate-tool


安装依赖： 确保已安装 Python 3.9 或更高版本，然后安装所需库：
pip install pandas openpyxl xlrd>=2.0.1


运行程序：
python excel_deduplicate.py



使用方法

去重模式：

点击“上传对比文件”和“上传基准文件”，选择 .xls、.xlsx 或 .csv 文件。
基准文件要求：第一列标题为“内容”，第二行起为有效中国大陆手机号。
在对比文件预览中，选择手机号列。
点击“开始处理”，处理完成后点击“导出处理后的文件”保存结果。


乱序模式：

仅上传对比文件，点击“乱序处理”。
处理完成后点击“导出处理后的文件”保存乱序结果。


乱序开关：

在“选择手机号列”右侧，打开“乱序导出”开关，导出的文件将以随机顺序保存。



依赖

pandas：用于处理 Excel/CSV 文件。
openpyxl：支持 .xlsx 文件。
xlrd>=2.0.1：支持 .xls 文件。
tkinter：用于 GUI 界面（Python 内置）。

打包为可执行文件
您可以使用 PyInstaller 将程序打包为独立的可执行文件：
pip install pyinstaller
pyinstaller --onefile --windowed excel_deduplicate.py

打包后的文件位于 dist 目录下。
贡献
欢迎贡献代码或提出建议！请按照以下步骤：

Fork 本仓库。
创建您的功能分支（git checkout -b feature/YourFeature）。
提交更改（git commit -m 'Add YourFeature'）。
推送到分支（git push origin feature/YourFeature）。
创建 Pull Request。

许可证
本项目采用 MIT 许可证 - 详情请查看 LICENSE 文件。
开发者
菜逼开发：@yingying_guai 号称行业中三天饿九顿的开发
