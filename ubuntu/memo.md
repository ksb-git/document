## 사용자 루트권한

- sudo 사용자파일 열기
```console
sudo /etc/sudoers  
```
root    ALL=(ALL)    ALL  
{계정명}    ALL=(ALL)    ALL  
  
  
## 데스크탑 or 메뉴에 프로그램 생성
```console
sudo apt  install --no-install-recommends gnome-panel  
sudo gnome-desktop-item-edit --create-new {경로 및 .desktop 파일명}  
```
  
