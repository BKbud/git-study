# 1. 로컬 저장소 사용을 위한 Git 기본

- git init : 저장소 생성

- git branch : 브랜치 생성
- git checkout : 브랜치 이동
    - git checkout -b : 브랜치 생성 후 바로 이동

- git add : 커밋할 파일 추가
- git commit : 커밋할 파일에 설명을 추가하여 대기
    - git commit -a : add + commit ( 한 번 추적된 적 있는 파일들만 추가된다)
	- git commit -amend : 가장 최근에 커밋한 커밋 메시지를 수정한다.

<aside>
💡 Commit
커밋은 프로젝트에서 의미가 있는 최소한의 단위이다. ‘의미’를 가질 수 있게 되는 시기라면 언제든 커밋을 하는 것을 권장한다.

</aside>

- git merge ‘branch name’ : 현재 작업 중이니 브랜치에 ‘branch name’의 브랜치를 가져와 병합
    - 정상적으로 병합된 경우 변경된 파일과 줄 수를 출력한다.
        
   	 	<img width="430" alt="Screen_Shot_2023-09-05_at_3 16 09_PM" src="https://github.com/BKbud/git-study/assets/80103052/421c1187-e132-4064-90d1-b52bc8e526b7"> 
    
    - 충돌이 발생한 경우 오류 메세지를 띄우며 충돌이 발생한 파일을 출력한다.
        
        <img width="665" alt="Screen_Shot_2023-09-05_at_3 24 23_PM" src="https://github.com/BKbud/git-study/assets/80103052/87c2bffc-91fe-4889-9cbe-8c9a4738623b">


- git log : 커밋 내역을 보여준다.
    - -p :  각 커밋에 적용된 실제 변경 내용을 보여준다.
    - —stat : 각 커밋에서 수정된 파일의 통게 정보를 보여준다.
    - —name-only : 커밋 정보 중에서 수정된 파일의 목록만 보여준다.
    - —graph : 브랜치 분기와 병합 내역을 아스키 그래프로 보여준다.

+  추가로 공부할 것들

commit convention

