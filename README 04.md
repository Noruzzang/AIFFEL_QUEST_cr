# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 조규원
- 리뷰어 : 이익현

# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
   import math  # math 모듈 사용

def integer(message):  # 정수 함수 정의
  try:
    return int(input(message))
  except ValueError:
    print("잘못된 입력입니다. 정수를 입력해 주세요.")
    return integer(message)  # 잘못된 입력 시 재귀 호출로 입력 받기

def calculater(number1, number2, order):  # 연산 수행 함수
  if order == '+':
    return number1 + number2
  elif order == '-':
    return number1 - number2
  elif order == '*':
    return number1 * number2
  elif order == '/':
    if number2 == 0:  # 두 번째 정수가 0인 경우
      return "0으로 나눌 수 없습니다."  # 오류 메시지 출력
    return number1 / number2  # 적절한 나눗셈 메시지 출력
  elif order == '**':
    return math.pow(number1, number2)  # 제곱 연산 수행
  else:
    return "지원하지 않는 연산자입니다."  # 지원하지 않는 연산자 오류 메시지

number1 = integer("첫 번째 정수 : ")
number2 = integer("두 번째 정수 : ")
order = input("연산자 입력 (+, -, *, /, **): ")

result = calculater(number1, number2, order)  # 연산 수행
print(f"결과 : {result}")

calculator = input("계속 계산기를 사용하겠습니까? (y/n) : ")  # 계산기 사용 여부 질문
if calculator == 'y':
  print("계산기를 사용합니다.")
else:
  print("계산기를 사용하지 않습니다.")
  잘되있다
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
주석이 이해하는데 도움이 되었다   # 잘못된 입력 시 재귀 호출로 입력 받기
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
calculator = input("계속 계산기를 사용하겠습니까? (y/n) : ")  # 계산기 사용 여부 질문
if calculator == 'y':
  print("계산기를 사용합니다.")
else:
  print("계산기를 사용하지 않습니다.")

    첫번째떄 none으로 나와서 다시 작성하였다.         
- [ ]  **4. 회고를 잘 작성했나요?**
    회고가 잘작성되있고  공감이 갔다
        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    코드가 간결하지만 예외처리부분이 아쉬운거같다.
        - 


# 회고(참고 링크 및 코드 개선)
```
elif order == '/':
    if number2 == 0:  # 두 번째 정수가 0인 경우
      return "0으로 나눌 수 없습니다."  # 오류 메시지 출력
    return number1 / number2  # 적절한 나눗셈 메시지 출력
두번째 정수가 0일때 오류가되는 부분을 
 except ZeroDivisionError:     # 나눗셈에서 b가 0인 경우 에러 처리
    print("0으로 나눌 수 없습니다")
    return None
부분으로 ZeroDivisonError를 사용했으면 더 좋았을거같다
