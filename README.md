使用LangChain的生成式AI
使用LangChain创建生成式AI应用。

环境
您可以使用conda（推荐）或pip在本地安装环境。提供了conda和pip的环境配置。请注意，如果您选择pip作为安装工具，您可能需要进行额外的调整。

如果您在环境中遇到任何问题，请提出一个问题，展示您遇到的错误。如果您感到自信，可以直接创建一个拉取请求。

对于pip和poetry，确保在您的系统中安装了pandoc。在 MacOS 使用 brew:

brew install pandoc
在 Ubuntu 或 Debian linux 上，使用 apt:

sudo apt-get install pandoc
在Windows上，可以使用一个安装程序。

Conda
这是安装依赖项的推荐方法。请确保你已经安装了anaconda。

首先创建包含所有依赖项的书籍环境：

conda env create --file langchain_ai.yaml --force
conda环境被称为langchain_ai。你可以像下面这样激活它：

conda activate langchain_ai 
Pip
Pip是Python中的默认依赖管理工具。使用pip，您应该能够从requirements文件安装所有库：

pip install -r requirements.txt
Docker
环境也有一个docker文件。它使用docker环境并启动一个ipython笔记本。使用它，首先构建它，然后运行它：

docker build -t new_image .
docker run -it new_image
你应该能在你的浏览器中找到笔记本，地址为http://localhost:8080。

Poetry
确保你已经安装了poetry。在Linux和MacOS上，你应该能够使用requirements文件：

poetry install
这应该会获取pyproject.toml文件并安装所有依赖项。

代码验证
要在ruff中运行代码验证，请运行

ruff check .
贡献
如果你发现笔记本或依赖项有任何问题，请随时创建一个拉取请求。

如果你想更改conda依赖项规范（yaml文件），你可以像这样测试它：

conda env create --file langchain_ai.yaml --force
你可以像这样更新pip的需求：

pip freeze > requirements.txt
请确保你保持这两种维护依赖关系的方式同步。

然后确保，在新的环境中测试笔记本，看它们是否运行。
