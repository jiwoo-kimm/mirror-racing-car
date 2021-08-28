# 🃏 Racing Car Game with TDD & Pair Programming

- Java로 구현한 자동차 경주 게임입니다.
- TDD와 Pair Programming을 통해 구현했습니다.
- `MVC 패턴` 기반 리팩토링을 수행하여 `Domain`의 `View` 의존성을 제거했습니다.
- 테스트 가능한 부분과 테스트하기 힘든 부분을 분리하여 단위 테스트를 수행했습니다.

<br>

## 🎮 프로그램 내용

```
경주할 자동차 이름을 입력하세요(이름은 쉼표(,)를 기준으로 구분)
pobi,crong,honux

시도할 회수는 몇회인가요?
5

실행 결과
pobi  : -
crong : -
honux : -

pobi  : --
crong : -
honux : --

pobi  : ---
crong : --
honux : ---

pobi  : ----
crong : ---
honux : ----

pobi  : -----
crong : ----
honux : -----

pobi  : -----
crong : ----
honux : -----

pobi, honux가 최종 우승했습니다.
```

<br>

## 📌 기능 구현 목록

### 1차

- 자동차 이름 입력받기
    - 자동차 이름 길이 체크(1~5자)
    - 자동차 이름 ,로 구분하기
    - 공백/null 체크
- 시도할 횟수 입력받기
- 랜덤 boolean값 추출하기
- 시도할 횟수만큼 자동차 움직이기
- 결과 출력
- 우승자 출력

### 2차

- [x] `Candidate` 대신 `Race`에 `List<Car>` 필드로 갖고 관리하기
- [x] rename `RandomStrategy` → `MoveStrategy`
- [x] `race`와 `round` 명칭 혼용 이슈 해결
- [x] 도메인의 `toString()`에 담긴 로직을 View로 이동하기
- [x] Exception 메세지를 View와 분리하기
