### pull conflict 케이스와 해결

- pull을 한다고 해서 로컬과 원격의 소스가 자동으로 동일해 지는 것은 아니며, 상황 별 옵션이 필요함
- checkout은 내가 사용할 브랜치를 지정하는 것.main외 추가 브랜치 설정시 사용

```
git checkout branch 
```

### fetch와 pull 차이

- fetch : 원격의 최신 이력들을 확인할 수 있고 원격의 commit들을 로컬로 가져옴. 가져오기만 할 뿐 병합(merge)되지는 않는 상태<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;로컬저장소는 최근 커밋이력의 위치를 가리키고, 원격저장소는 로컬로 가져온 커밋이력 중 가장 최근 커밋이력의 위치를 가리킨다.
- pull : fetch의 기능과 함께 merge도 함께 이루어짐
> pull의 경우 <br/>

1. 자동으로 병합 되기에 어떠한 내용이 원격으로 부터 받아져 병합되는지 확인하기 어렵다는 점은 참고해야한다.
2. 옵션 없이 pull 을 하면 불필요한 commit까지 병합 될 수 있다. git 에서 경고 메세지 콘솔에 띄워줌
3. main이 아닌 branch를 체크아웃 후 작업중인 상태에서 git pull origin main 을 실행하면 로컬의 main 저장소에 병합되지 않고, 현재 작업중인 branch의 로컬에 병합되어 버린다.

### fetch + merge

```
git fetch --all
git fetch remotename
```

```
git reset --hard origin/main
```
reset은 되돌리기, 재설정의 역할을 한다.  여기에 --hard 옵션을 주면 뒤에 적은 원격명과 브랜치 명에 해당하는 이력을 fetch로 가져온 이력으로 모두 재설정 해주고 초기화 되는 것이다. 
<br/>
- --hard  :  reset하고자 하는 이력을 모두 초기화 하고 재설정해준다.
- --soft  :  이력만 되돌릴 뿐 해당이력의 내용이나 인덱스는 지워지지 않고 그대로 있다. 언제라도 다시 커밋할 수 있는 상태. 
- --mixed  :  이력이 되돌려지고 해당 내용도 남아있지만, 인덱스는 지워진 상태
