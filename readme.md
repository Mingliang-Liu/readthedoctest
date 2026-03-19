# ReadTheDocs Test

## 新建github仓库
新建了readthedoctest的公开仓库
.gitignore选Python
LICENSE选GPLv3
不初始化readme.md
```
git clone https://github.com/Mingliang-Liu/readthedoctest.git
```

## Sphinx安装
```
conda create -n sphinx python=3.10 -y
conda activate sphinx

pip install sphinx==8.1.3 -i https://repo.sensetime.com/repository/pypi/simple/
```

## 初始化
```
sphinx-quickstart

Welcome to the Sphinx 8.1.3 quickstart utility.

Please enter values for the following settings (just press Enter to
accept a default value, if one is given in brackets).

Selected root path: .

You have two options for placing the build directory for Sphinx output.
Either, you use a directory "_build" within the root path, or you separate
"source" and "build" directories within the root path.
> Separate source and build directories (y/n) [n]: y <--------这里选y表示编译的文件单独放在build中

The project name will occur in several places in the built documentation.
> Project name: ReadTheDocs_Test <--------项目名
> Author name(s): liumingliang   <--------作者
> Project release []: v1.0.0     <--------版本号

If the documents are to be written in a language other than English,
you can select a language here by its language code. Sphinx will then
translate text that it generates into that language.

For a list of supported codes, see
https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
> Project language [en]: zh_CN   <-------- 语言(简体中文)

Creating file /data/program/readthedoctest/source/conf.py.
Creating file /data/program/readthedoctest/source/index.rst.
Creating file /data/program/readthedoctest/Makefile.
Creating file /data/program/readthedoctest/make.bat.

Finished: An initial directory structure has been created.

You should now populate your master file /data/program/readthedoctest/source/index.rst and create other documentation
source files. Use the Makefile to build the docs, like so:
   make builder
where "builder" is one of the supported builders, e.g. html, latex or linkcheck.
```

## 文件组织
tree
```
├── build
├── LICENSE
├── make.bat
├── Makefile
├── readme.md
└── source
    ├── conf.py
    ├── index.rst
    ├── _static
    └── _templates
```

## 修改默认主题
默认的主题alabaster，如果想安装其它的主题，可以先到Sphinx的官网查看：
https://sphinx-themes.org/

安装shibuya主题（可自行选择其他）
```
pip install shibuya==2026.1.9 -i https://repo.sensetime.com/repository/pypi/simple/
```
修改conf.py文件：
```
# html_theme = 'alabaster'
html_theme = 'shibuya'
```

## 支持markdown和markdown表格
```
pip install recommonmark==0.7.1 sphinx_markdown_tables==0.0.17 -i https://repo.sensetime.com/repository/pypi/simple/
```
在conf.py中配置extention：
```
extensions = ['recommonmark','sphinx_markdown_tables']
```

## 编译
```
make html

Running Sphinx v8.1.3
loading translations [zh_CN]... done
making output directory... done
building [mo]: targets for 0 po files that are out of date
writing output... 
building [html]: targets for 1 source files that are out of date
updating environment: [new config] 1 added, 0 changed, 0 removed
reading sources... [100%] index
looking for now-outdated files... none found
pickling environment... done
checking consistency... done
preparing documents... done
copying assets... 
copying static files... 
Writing evaluated template result to /data/program/readthedoctest/build/html/_static/basic.css
Writing evaluated template result to /data/program/readthedoctest/build/html/_static/language_data.js
Writing evaluated template result to /data/program/readthedoctest/build/html/_static/documentation_options.js
copying static files: done
copying extra files... 
copying extra files: done
copying assets: done
writing output... [100%] index
generating indices... genindex done
writing additional pages... search done
dumping search index in Chinese (code: zh)... done
dumping object inventory... done
build succeeded.

The HTML pages are in build/html.
```