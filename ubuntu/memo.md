## 사용자 루트권한
- sudo 사용자파일 열기
```console
sudo /etc/sudoers  
```
```bash
...
root       ALL=(ALL)    ALL  
{계정명}    ALL=(ALL)    ALL  
...
```
root 아래에 권한이 부여될 계정정보 추가
  
  
  
## jdk 설치 및 JAVA_HOME path 설정
```console
sudo apt-get install openjdk-8-jdk
```
  
주의 :  
/etc/enviroment 파일을 수정할 경우 문제가 발생할 수 있다고 함.  
아래와 같이 bash 파일을 생성할것을 권장  
  
```console
sudo vi /etc/profile.d/java.sh
```
  
sh 파일 생성 후 내용으로 export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/ 작성
path 정보는 재로그인시 부터 적용된다고 함
  
### 참고
<https://ark1230.tistory.com/44>
<https://vitux.com/how-to-setup-java_home-path-in-ubuntu/>
  
  
  
## 데스크탑 or 메뉴에 프로그램 생성
```console
sudo apt  install --no-install-recommends gnome-panel  
sudo gnome-desktop-item-edit --create-new {경로 및 .desktop 파일명}  
```
  
