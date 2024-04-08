### Github의 main branch에는 완성된 버전을 올려서 관리합니다!!!!!

### 로컬 영역(git)에서 작업을 수행하고, commit합니다!

- git add .
- git commit -m "커밋메세지 남깁니다"

### 일정수준 이상 기능이 완성되어서 공유가 필요하다고 느껴질 때, Github의 main branch와 비교하여 Merge합니다(병합합니다)

- git fetch origin main (선택입니다)
- git merge origin/main

### 충돌 해결(merge conflict)
```
<<<<<<< HEAD // 이 부분을 지우고
'내가 Git에서 수정한 내용'  //1번
============  // 이 부분도 지우고
'원격 저장소에 저장되어있으나, 현재 내 Git에는 작성되어있지 않은 수정사항' //2번
>>>>>>> origin  // 이 부분도 지우고

이런 식으로 파일이 변경되어있는데,
//뒤에 작성되어있는 '이 부분을 지우고' 부분은 지우고,
1번과 2번 내용의 순서 혹은 코드를 기존 코드의 작성자와 상의해서 충돌을 해결하면 됩니다!
```
### Git에서(로컬에서) 모든 충돌을 다 해결하고, 브랜치 자체를 원격 저장소에 올립니다!

git push origin (브랜치이름!!! Main 말고 브랜치 이름!!!!!)
- ex) git push origin sanghwa_login_function

### 여기까지 진행했다면 sanghwa_login_function에는 문제없는 코드가 들어가있겠죠..? 그걸 바탕으로 main브랜치에 PR을 날립니다(PULL REQUEST)
