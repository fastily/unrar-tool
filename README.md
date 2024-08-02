# unrar-tool
[![Python 3.12+](https://upload.wikimedia.org/wikipedia/commons/5/50/Blue_Python_3.12%2B_Shield_Badge.svg)](https://www.python.org)
[![License: GPL v3](https://upload.wikimedia.org/wikipedia/commons/8/86/GPL_v3_Blue_Badge.svg)](https://www.gnu.org/licenses/gpl-3.0.en.html)

A simple web service that makes it easy to convert rar to zip

## Dependencies
* [unar](https://theunarchiver.com/command-line)

## Usage
```bash
# install dependencies
pip install -r requirements.txt

# start in development mode, visit http://127.0.0.1:8000 to view the web interface
python -m unrar_tool

# run w/ gunicorn
gunicorn -w 2 -k uvicorn.workers.UvicornWorker -b "0.0.0.0:8000" is_it_up.__main__:app

# docker build
docker build -t unrar-tool .

# docker run
docker run --dit --rm unrar-tool
```