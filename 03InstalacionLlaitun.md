## Crear directorio tools para descargar herramientas desde GitHub
```
mkdir /home/lesand/Desktop/tools
cd /home/lesand/Desktop/tools
```
```
git clone https://github.com/lesandcl/Llaitun.git
```
```
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:deadsnakes/ppa -y
```
```
sudo apt-get  update
```
```
sudo apt-get install python3.7 -y
sudo apt install python3.7-distutils -y
```
```
sudo apt-get install virtualenv -y
virtualenv ENV3.7 -p python3.7
source ENV3.7/bin/activate
```
```
cd /usr/lib/x86_64-linux-gnu/
sudo ln -s -f libc.a liblibc.a
```
```
cd /home/lesand/Desktop/tools/Llaitun/
pip install -r requirements.txt
```
```
sudo $(which python) Llaitun.py
```
