## 사용자 루트권한
- sudo 사용자파일 열기
```console
sudo /etc/sudoers  
```
root       ALL=(ALL)    ALL  
{계정명}    ALL=(ALL)    ALL  
  
사용될 일반 유저정보 추가
  
  
  
## jdk 설치
```console
sudo apt-get install openjdk-8-jdk
```
  
  
  
## 데스크탑 or 메뉴에 프로그램 생성
```console
sudo apt  install --no-install-recommends gnome-panel  
sudo gnome-desktop-item-edit --create-new {경로 및 .desktop 파일명}  
```
  
