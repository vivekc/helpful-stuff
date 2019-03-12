##### 1. Uninstalling all packages using xargs

```
pip freeze > dump.txt
cat dump.txt | xargs sudo pip uninstall -y
```
