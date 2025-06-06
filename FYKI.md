 # In case pip broke inside your virtual env
 (can't find pip._internal.build_env)
 and with it, most likely, the necessary Jupyter modules (ipykernel, jupyter-client, etc. so VS Code can't get the kernel up and ‘hangs’ on port timeout.

## To try:
- Activate your environment in the terminal
```bash
cd /Users/username/Desktop/folder   #path to the folder
source my_env1/bin/activate
```
- Fix the pip:
```bash
python -m ensurepip --upgrade
python -m pip install --upgrade pip setuptools wheel
```
- Reinstall Jupyter components:
```bash
pip install --force-reinstall ipykernel jupyter-client jupyter-core
```
- Register the kernel (if necessary)
```bash
python -m ipykernel install --user --name my_env1 --display-name "Python 3.11 (my_env1)"
```
- Restart VS Code

- (Optional) increase the kernel startup timeout in the Jupyter-extension settings:
```bash
// settings.json
"jupyter.jupyterServerMaxTimeout": 60_000
```

## iCloud Problem

The system under ‘Optimise Storage’ has uploaded the folder with the project to iCloud, i.e. locally you don't actually have this folder on your drive. That's why when trying to bring up venv and ipykernel VS Code just doesn't find the necessary files.

- What you can do: download the folder locally
In Finder, right-click on the folder → ‘Download Now’. The cloud will then disappear and all files will be available.

## Disable Desktop/Documents Synchronisation in iCloud
- System Preferences → Apple ID → iCloud → ‘Settings...’ next to ‘iCloud Drive’.
- Uncheck ‘Desktop and Documents.’
- macOS will start downloading everything back to your local drive.







### - V.R
