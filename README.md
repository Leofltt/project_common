Common repository for The Sound of AI Open Source Research Project.

# Main app
This main app provides scripts to install and run the end-to-end pipeline. This includes Speech-to-Text, Text-to-Sound, and Sound Generation services, as well as the sampler/playback tool.

## Dependencies
### Csound
* Csound https://csound.com/
* latest version should run, tested version in this project is `6.16.2`
* https://github.com/csound/csound/releases/tag/6.16.2
* install .exe 
* or unzip .zip version in a folder that is added to the system path

On MacOs, if homebrew is installed, the setup script will install Csound automatically.

### Python
* Python version 3.8 is to be used
* in case python 3.8 available on the system but not the default one then use `setup3.8.bat` instead of `setup.bat`

## Setup and Run
Each service requires its own virtual python environment which is created during the setup. 
⚠️ This may take several minutes.

A manual that describes the UI functionalities and how to use the app is available at https://github.com/TheSoundOfAIOSR/rg_production/blob/main/Manual.md

### windows
```
git clone --recurse-submodules https://github.com/TheSoundOfAIOSR/project_common.git
cd project_common
setup.bat
run.bat
```

### Mac
```
git clone --recurse-submodules https://github.com/TheSoundOfAIOSR/project_common.git
cd project_common
bash setup_mac.sh
bash run_mac.sh
```

### update

if already cloned without `--recurse-submodule`
```bash
cd project_common
git submodule update --init --recursive
```
further updates
```bash
git pull --recurse-submodules
```

# Sound Generator webapp
The Sound generator module can also be used via a web app - [follow these instructions](https://github.com/TheSoundOfAIOSR/rg_sound_generation/blob/main/SOUND_GENERATOR.md) to get it running.
