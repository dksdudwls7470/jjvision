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

# 깃허브 사용방법
```
파일불러오기 : git clone (자기 깃허브 주소 및 파일명까지)
```

## vim설정
```
set ne = 맨앞에 번호출력
set cindent = c언어 사용할때
set ts = 탭을 눌르면 4칸씩 띄어짐
if has("syntax") 
    syntax on
end if =syntax를 가진 파일이면 syntax기능사용(컬러를 준다)
```
