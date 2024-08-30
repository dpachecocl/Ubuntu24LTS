## Instalacion de Docker
```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```
### Verificacion de instalacion de Docker
```
sudo docker run hello-world
```
### Creacion de Ambiente virtual, instalacion de Selenium y Ejecucion de Selenium WebDriver
```
cd /home/lesand/Desktop/tools/
virtualenv ENV-SELENIUM -p python3
source ENV-SELENIUM/bin/activate
```
```
pip install selenium
```
```
sudo docker run -d -p 4444:4444 --name selenium-chrome selenium/standalone-chrome
```
```
mkdir /home/lesand/Desktop/tools/selenium
cd /home/lesand/Desktop/tools/selenium
```
```
nano selenium01.py
```
```
# Importacion de las librerias necesarias.
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.chrome.options import Options

# Configurar las opciones del navegador
options = Options()
options.add_argument('--no-sandbox')
options.add_argument('--headless')
options.add_argument('--disable-dev-shm-usage')

# Crear una instancia del navegador remoto
driver = webdriver.Remote('http://localhost:4444/wd/hub',options=options)

try:
    # Navegar a la página web deseada
    driver.get('https://www.lesand.cl')

    # Imprimir el título de la página
    print(driver.title)
finally:
    # Cerrar el navegador
    driver.quit()
```
