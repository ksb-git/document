### 2019.05.20

@BatchSize(size = 5)  
@Fetch(FetchMode.SUBSELECT)  

jpa 1:N 쿼리에 대한 대처방법, 좀 더 자세히 알아볼 필요가 있음

---

### java 파일처리 
- 파일처리 시 Path 오브젝트가 닫히지 않아 프로세스 점유발생
- 일정량 이상 파일경로에 대한 점유가 생기면 접근불가로 오류발생함
- InputStream, DirectoryStream 으로 작업하며 완료후 반드시 닫아야함
- 아래 내용 링크는 프로세스의 점유에 대한 확인부분
http://blog.leekyoungil.com/?p=219

```cosole
ps aux | grep {프로세스명}

#프로세스번호 획득

ls -l /proc/{프로세스번호}/fd/ | wc -l
```
