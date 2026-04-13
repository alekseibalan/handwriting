### arch, cuda, pytorch

```bash
sudo pacman -S nvidia-open cuda python-pycuda pyenv
eval "$(pyenv init - bash)"
pyenv install 3.13
pyenv local 3.13
python -m venv venv
source venv/bin/activate
# when python complains that 200G is not enough for temp, this helps export TMPDIR=$HOME/tmp
pip install -U torch --index-url https://download.pytorch.org/whl/cu130
pip install ipykernel
python -m ipykernel install --user --name=kernelname
jupyter kernelspec list
jupyter notebook
```

clear_cache.sh
```bash
echo -n "deleting python caches [enter] "
read -r -s
echo
find . -type d -name __pycache__ -prune -exec rm -r {} \;
```
