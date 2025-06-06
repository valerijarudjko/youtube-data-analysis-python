 # In case pip broke inside your virtual env
 (can't find pip._internal.build_env)
 and with it, most likely, the necessary Jupyter modules (ipykernel, jupyter-client, etc.
 - so VS Code can't get the kernel up and ‘hangs’ on port timeout.

## To try:
- Activate your environment in the terminal
```bash
cd /Users/youruser/Desktop/folder
source my_env1/bin/activate
```
- Fix the pip:
```bash
 python -m ensurepip --upgrade
python -m pip install --upgrade pip setuptools wheel
```

