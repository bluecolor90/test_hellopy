# test collab.
- fork, pull request, merge, branch 작업은 github권장사항이나 지양
- 소규모작업이며 github에 익숙하지 않은 멤버들간 협업방안
- 이를 위해선 작업 원격저장소에 협업멤버 지정이 필요함
## collab. member workflow
1. 시작전에 원격수정사항을 pull
    - ![remote changes from other members](image-5.png)
    - 로컬 수정사항인 <브랜치이름> 의 반영단계가 origin/<브랜치이름>
    - 원격수정사항이 로컬에 반영되어있지않은상태, pull로 반영후 작업
    - fetch로 미리 수정사항 확인가능, vscode는 자동으로 fetch해주는듯함
1. 로컬에 수정사항 발생시 changes에 수정사항 발생
    - ![remote changes - before](image.png)
    - ![remote changes - before commit](image-1.png)
1. 수정사항을 stage, 저장소로 어떠한정보도 업로드되지않은상태
    - ![stage modifications](image-2.png)
    - stage한 이후의 수정사항은 추가로 stage하지않는이상 commit에 포함되지않음
1. commit : stage단계의 수정사항들을 push 준비
    - (주의) 수정사항이 업로드되진않음
    - ![commit modifications](image-3.png)
    - 로컬 장소인 main 만 리비전그래프가 갱신됨
    - push하기 전까지는 로컬 저장소인 main에만 반영되어있는모습
1. push : 원격저장소로 push
    - ![push 버튼](image-4.png)
    - commit된 수정사항들만 저장소에 반영됨
    - vscode에서 stage ~ push를 동시에 진행할 수는 있음
## 필수 workflow
- 작업시작전에 원격수정사항을 pull 하여 검토하는건 필수
    - 단일 branch로 작업하므로 충돌 발생시 되돌리는 과정이 어려워질 수 있음
    - refork혹은 branch로 작업시 여러명의 작업결과물을 구분하여 볼 수 있음
    - conflict 발생예시
        1. 원격수정사항을 fetch하지않고 수정작업진행 (권장x) ![commit w.o. pull](image-6.png)
        1.
