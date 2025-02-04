# java-calculator-precourse

---

[JunHakLee03](https://github.com/JunHakLee03)의 우테코 7기 프리코스 1주차 미션 문자열 덧셈 계산기입니다.

사용자가 일정한 규칙에 따라 입력한 문자열에서 숫자를 추출하고 덧셈하여 결과를 반환하는 계산기 프로그램입니다.

![java-calculator_JunHakLee03](https://github.com/user-attachments/assets/da311476-eb0b-4142-8938-4441f0f8e5a8)

---

### <규칙>

구분자와 양수로 구성된 문자열
<br> 쉼표 또는 콜론을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환한다
<br> 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다

# 목차

---

- [미션 시작하기](#시작하기)
- [구현할 기능 목록](#구현할-기능-목록)
    - [문자열 입력 받기](#문자열-입력-받기)
    - [입력 받은 문자열 검사하기](#입력-받은-문자열-검사하기)
    - [계산 후 출력하기](#계산-후-출력하기)

## 미션 시작하기

---

레포지토리를 Clone 하고 IDE에서 애플리케이션을 실행합니다.

`git clone -b {브랜치명} --single-branch https://github.com/woowacourse-precourse/java-calculator-7`

## 구현할 기능 목록

---

### 문자열 입력 받기

- 덧셈할 문자열을 입력해 주세요. 라고 출력 한다.
- 사용자로부터 `문자열(userInput)`을 입력 받는다.

### 입력 받은 문자열 검사하기

- 유효한 커스텀 구분자를 사용하는지 확인한다.
    - 사용하지 않는다면 그대로 `실입력값(value)`으로 저장한다.
    - 사용한다면 5번 인덱스부터 `실입력값(value)`으로 저장한다.
    - 양수 표현에 사용될 소수점(.)이나 파이(π), 자연상수(e) 기호는 구분자로 사용 할 수 없다.
- `실입력값(value)`의 각 문자열 인덱스가 양수 혹은 구분자, 커스텀 구분자 중 하나인지 확인한다.
    - 아니라면 IllegalArgumentException을 발생시키고 애플리케이션을 종료한다.

### 계산 후 출력하기

- 구분자와 커스텀 구분자로 입력받은 문자열을 split한 뒤 자료형을 바꿔 전부 덧셈한다.
- 사용자에게 `System.out.println("결과 : " + result)`를 출력한다.