# 전주비전대 Project

## Install DHT11 sensor
```
git clone http://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT
sudo python setup.py install
cd Adafruit_Python_DHT/examples
```
  - run
  ```
  python AdafruitDHT.py 11 4
  ```



# InfluxDB Installation

## 1. Repository의 GPS Key를 더하기
```
curl -sL https://repos.influxdata.com/influxdb.key | sudo apt-key add -
```
## 2. Repository를 더하기
```
echo "deb https://repos.influxdata.com/debian stretch stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
```
## 3. 프로그램 설치
```
sudo apt update
sudo apt install influxdb
```
## 4. 프로그램 실행
```
sudo service influxdb start
```
## 5. 데이터 베이스 만들기
```
데이터베이스 만드는법 create database<name>
```
```
확인 : show databases
```

# Grafana Installation

## 1. Repository의 GPS key를 더하기
```
curl https://bintray.com/user/downloadSubjectPublicKey?username=bintray | sudo apt-key add -
```
## 2. Respository를 더하기
```
 echo "deb https://dl.bintray.com/fg2it/deb stretch main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
```
## 3. 프로그램 설치
```
 sudo apt update
 sudo apt install grafana
```
## 4. 프로그램 실행
```
sudo service grafana-server start
```
