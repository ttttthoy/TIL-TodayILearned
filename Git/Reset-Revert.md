### reset

```
//특정파일 하나의 add를 취소
git reset HEAD 파일명 

//파일명을 명시하지 않으면 전체 add내역을 취소한다.
git reset HEAD
```
```
//직전커밋 취소
git reset HEAD^

//마지막 n개의 커밋 취소
git reset HEAD~n
```
```
//원격저장소의 마지막 커밋 상태로 되돌림
git reset --hard HEAD

//커밋취소, unstaged상태, working directory에서 삭제
git reset --hard HEAD^

//커밋취소, unstaged상태, working directory에서 보존
//git reset HEAD^ 와 같은 상태
git reset --mixed HEAD^

//커밋취소, staged상태, working directory에서 보존
git reset --soft HEAD^

//커밋 메세지 변경할 때
git commit --amend
```

### revert

```
git revert 커밋id/hash
```
revert의 가장 큰 특징이자 reset과 구분 되는 점은,커밋을 취소한 이력이 남는 다는 점.
reset은 특정 시점의 커밋으로 되돌아 가면서 이후의 커밋이력을 모두 지우지만, revert는 특정 커밋의 내용만! 지우고 나머지 커밋은 그대로 보존하며 revert된 커밋의 이력도 포함한다.
