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
파일 불러 오기 : git clone (자기 깃 허브 주소 및 파일명까지)
파일 올리기 : git push멀까요~
```
## vim설정
```
set ne = 맨앞에 번호출력
set cindent = c언어 사용할때
set ts = 4 = 탭을 눌르면 4칸씩 띄어짐
set softtabstop=4
set bg=dark
set expandtab
let python_version_2 = 1
let python_highlight_all = 1
filetype indent plugin on

if has("syntax") 
    syntax on
end if =syntax를 가진 파일이면 syntax기능사용(컬러를 준다)
```

## 적외선 인체 감지센서 파이썬 소스
```
  1 #!/usr/bin/python
  2
  3 import time
  4 import RPi.GPIO as GPIO
  5
  6 print GPIO.VERSION
  7 GPIO.setmode(GPIO.BCM)
  8 GPIO.setup(4, GPIO.IN)
  9
 10 def interrupt_fired(channel):
 11     print("interrupt Fired")
 12     print(channel)
 13
 14 GPIO.add_event_detect(4, GPIO.FALLING, callback=interrupt_fired)
 15
 16 while(True):
 17     time.sleep(1)
 18     print("Timer fired")
```
