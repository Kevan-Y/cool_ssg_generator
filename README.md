
# cool_ssg_generator
A simple SSG generator made with Python.
Current version is 0.1.0

### Dependencies
- [Python 3.8.5](https://www.python.org/downloads/) (or higher)

### Installation
Make sure you have installed Python version 3.8.5 or above. No other dependencies is currently needed.

To clone this project, use:
```console
git clone https://github.com/lmpham1/cool_ssg_generator.git
```
Then, you'll probably want to navigate to the project's root folder:
```console
cd cool_ssg_generator
```

#### For Anaconda users (optional)
If you want to quickly set up a virtual development environment with Anaconda, use the following commands in the project's root folder:
```console
conda env create -f environment.yml
conda activate ssg_env
```
For more information on Anaconda, please refer to their [official documentation](https://docs.anaconda.com/)

---

### Basic Usage
Navigate to the project folder (if you haven't done so already):
```console
cd cool_ssg_generator
```
Generate a website from a file or folder:
```console
python main.py --input <INPUT_FILE_OR_FOLDER>
```
Default output folder is `./dist/`, to specify a custom output folder:
```console
python main.py --input <INPUT_FILE_OR_FOLDER> --output <OUTPUT_FOLDER>
```
CSS can be used via the `--stylesheet` flag:
```console
python main.py --input <INPUT_FILE_OR_FOLDER> --stylesheet <STYLESHEET_URL>
```
For more usage, please refer to:
```console
python main.py -h
```
---

### Cool Features
Wanna know what make the `cool_ssg_generator` so cool? Aside from the totally-intentional doubled 'generator' in the name, it offers the following awesome features:
* Support multiple stylesheets! Simply use the `-s` or `--stylesheet` flags and separate each stylesheet link with space `' '`, i.e.:
```console
python main.py -i index.txt -s sheet1.css sheet2.css sheet3.css
```
* Markdown (.md files) support for **bold** (`**example**` or `__example__`), *italics* (`*example*` or `_example_`), and [links](https://github.com/lmpham1/cool_ssg_generator) (`[Example](www.example.com)`)
* Language for the output HTML documents can be configured with `-l` or `--lang` flag (default is `en-CA`):
```
python main.py -i test.txt -l en-UK
```
**Note**: No validation for `--lang`/`-l` option is implemented yet. See issue [#14](https://github.com/lmpham1/cool_ssg_generator/issues/14) for more information
* You can save your command-line options in a config file! No need to manually type all the options everytime, just use `--config`/`-c` flag with a json file:
```
python main.py -c config.json
```
**Note**: Using `--config`/`-c` option will ignore/override other options

---

### License
[MIT](LICENSE)
