# 1. 로컬 저장소 사용을 위한 Git 기본

- git init : 저장소 생성

- git branch : 브랜치 생성
- git checkout : 브랜치 이동
    - git checkout -b : 브랜치 생성 후 바로 이동


- git add : 커밋할 파일 추가
- git commit : 커밋할 파일에 설명을 추가하여 대기
    - git commit -a : add + commit ( 한 번 추적된 적 있는 파일들만 추가된다)

<aside>
💡 Commit
커밋은 프로젝트에서 의미가 있는 최소한의 단위이다. ‘의미’를 가질 수 있게 되는 시기라면 언제든 커밋을 하는 것을 권장한다.

</aside>

- git merge ‘branch name’ : 현재 작업 중이니 브랜치에 ‘branch name’의 브랜치를 가져와 병합
    - 정상적으로 병합된 경우 변경된 파일과 줄 수를 출력한다.
        
        <img width="400" alt="Screen_Shot_2023-09-05_at_3 16 09_PM" src="https://github.com/BKbud/BKbud/assets/80103052/db691beb-e09a-4c1d-ab27-8aff8b5b1f2e">
        
    
    - 충돌이 발생한 경우 오류 메세지를 띄우며 충돌이 발생한 파일을 출력한다.
        
        <img width="650" alt="Screen_Shot_2023-09-05_at_3 24 23_PM" src="https://github.com/BKbud/BKbud/assets/80103052/1b497cee-347e-4014-a838-53e6e5250bcc">
        

- git log : 커밋 내역을 보여준다.
    - -p :  각 커밋에 적용된 실제 변경 내용을 보여준다.
    - —stat : 각 커밋에서 수정된 파일의 통게 정보를 보여준다.
    - —name-only : 커밋 정보 중에서 수정된 파일의 목록만 보여준다.
    - —graph : 브랜치 분기와 병합 내역을 아스키 그래프로 보여준다.

+ 마주한 오류

- 깃 레포지토리를 생성할 때 README 파일을 생성하고 README 파일을 수정후 push하자 발생한 오류

<img width="665" alt="Screen_Shot_2023-09-05_at_3 49 49_PM" src="https://github.com/BKbud/BKbud/assets/80103052/842543f6-727e-4b7f-a226-d6cf9fe3fad9">


원격 저장소에서 README 파일을 추가하는 커밋이 로컬 저장소의 커밋 로그에는 없는 것이 원인이라고 함. (push 명령은 로컬 저장소의 commit 목록과 원격 저장소의 commit 목록을 비교한다.)

위에서 제한하는 대로 git pull을 하게되면 또한 오류가 발생한다. merge를 할 때 원격 저장소와 로컬 저장소가 공통으로 가지는 commit 지점이 존재하며 그 지점으로부터 병합을 시도하는데, 공통되는 커밋이 없어 오류가 발생한 것이다.

임시방편으로 "+" 옵션을 사용하여 해결이 가능하다고 한다.

```
git push origin +main
```

+  추가로 공부할 것들

commit convention
