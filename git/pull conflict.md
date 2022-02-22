### pull conflict 케이스와 해결

- pull을 한다고 해서 로컬과 원격의 소스가 자동으로 동일해 지는 것은 아니며, 상황 별 옵션이 필요함
- checkout은 내가 사용할 브랜치를 지정하는 것.main외 추가 브랜치 설정시 사용

```
git checkout branch 
```

#### fetch와 pull

- fetch : 원격의 commit들을 로컬로 가져옴. 가져오기만 할 뿐 병합(merge)되지는 않는 상태
- pull : fetch의 기능과 함께 merge도 함께 이루어짐
> pull의 경우 <br/>

1. 자동으로 병합 되기에 어떠한 내용이 원격으로 부터 받아져 병합되는지 확인하기 어렵다는 점은 참고해야한다.
2. 옵션 없이 pull 을 하면 불필요한 commit까지 병합 될 수 있다. git 에서 경고 메세지 콘솔에 띄워줌
3. main이 아닌 branch를 체크아웃 후 작업중인 상태에서 git pull origin main 을 실행하면 로컬의 main 저장소에 병합되지 않고, 현재 작업중인 branch의 로컬에 병합되어 버린다.



