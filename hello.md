## git 명령어 요약

- clone: 원격 저장소 (github) 을 내 컴퓨터에 복사해 온다.
- add: 내 컴퓨터에서 작업한 파일들을 스테이지에 추가
- commit: 스테이지에 올라온 파일들을 가지고 내 컴퓨터에 저장 (세이브와 같다.)
- push: 커밋들을 원격 저장소에 업로드

## 파일의 내용 되돌리기

- 특정 파일의 내용을 마지막 커밋으로 돌리고 싶다면 해당 파일 선택 후 '코드 뭉치 버리기' 선택

## 브랜치 변경하기

- 브랜치 : 기존 내용을 유지한 채 새로운 내용을 추가하고 싶을 때 사용한다.
- 체크아웃: 특정 브랜치 혹은 커밋으로 돌아가고 싶을 때 사용한다.
- 소스트리의 체크아웃: 브랜치 이름을 더블 클릭하는 것 만으로 체크아웃 가능

## 병합하기 1

- 헤드 브랜치에 변경사항이 없고,
- 병합 대상 브랜치가 헤드로부터 시작된 경우
- 아주 쉽게 병합 가능 = Fast-Foward

## 병합하기 2

- 헤드 브랜치에 추가적인 커밋이 생기는 경우
- 진짜 병합이 필요해진다.
- 충둘이 안나면 좋은데, 충돌이 나도 겁내지 말자.

## 충돌 해결하기

- 제일 중요한 점 : 겁내지 말기!
- 같은 파일을 병합 대상 두 컴시에서 동시 수정했을 경우 충돌이 날 확률이 높다.
- 에디터 사용, 혹은 SourceTree를 사용해서 충돌 해결 ㅅ가능하다.

## 커밋 되돌리기

### reset

- 쉽지만 커밋이 날아간다.
- 강제 푸시가 필요하다.

### 브랜치를 만들어서 되돌리기

- reset과 달리 내용이 사라지지 않는다.
- 장점 : 쉽다.
- 단점 : 트리가 지저분해진다.

### revert

- 역시 커밋은 없어지지 않는다.
- 장점 : 가장 정석적이다.
- 단점 : 충돌이 날 수 있다.

### revert2

- revert로 여러 커밋을 되돌리려면 최신부터 순서대로 revert한다.
- 그렇게 하면 충돌을 막을 수 있다.

## 커밋 덮어쓰기

- 필요하다면 이전 커밋 덮어쓰기도 가능
- 'commit --amend'
- 이미 push를 한 경우 'push --force'가 필요하다.

## stash 

- 다른 브랜치로 체크아웃하기 전에 현재 작업 내용을 저장하는 임시 저장소

## rebase로 병합하기

- merge처럼 두 브랜치를 합칠 때 사용된다. 현재 브랜치가 대상 브랜치 위로 올라간다.
- 장점 : 커밋 히스토리가 깔끔하게 정리된다.
- 단점 : 잘못하면 위험하다. 이미 원격 저장소에 올라간 경우 또는 협업을 하고 있는 경우 특히 위험하다.

## 기타 주의 사항

- 코드를 남기려고 주석을 달지 말자.
- 커밋 메시지를 잘 쓰자.
- 한가지 구현이 완료될 때마다 커밋을 하자(자주).
