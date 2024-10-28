# MAX78000-Evaluation-App
Learning with the MAX78000 Feather Board

## install pyenv
https://github.com/pyenv/pyenv#set-up-your-shell-environment-for-pyenv

Next, close the Terminal, open a new Terminal and install Python 3.11.8.
```console
pyenv install 3.11.8
```
## Upstream Code
```console
$ cd <your/project>
$ git clone --recursive https://github.com/analogdevicesinc/ai8x-training.git
$ git clone --recursive https://github.com/analogdevicesinc/ai8x-synthesis.git
```
## Creating the Virtual Environment
```console
cd ai8x-training
pyenv local 3.11.8
python -m venv .venv --prompt ai8x-training
echo "*" > .venv/.gitignore
source .venv/bin/activate
(ai8x-training) $ pip3 install -U pip wheel setuptools
(ai8x-training) $ pip3 install -r requirements.txt --extra-index-url https://download.pytorch.org/whl/cu121
(ai8x-training) $ pip3 install -r requirements.txt --extra-index-url https://download.pytorch.org/whl/rocm5.7
```
## MSDK Updates
```
https://github.com/analogdevicesinc/msdk
```
## Synthesis Project
```console
(ai8x-training) $ deactivate
cd <your/project>
cd ai8x-synthesis
pyenv local 3.11.8
python -m venv .venv --prompt ai8x-synthesis
echo "*" > .venv/.gitignore
source .venv/bin/activate
(ai8x-synthesis) $ pip3 install -U pip setuptools
(ai8x-synthesis) $ pip3 install -r requirements.txt

