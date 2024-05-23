# AIFFEL Campus Code Peer Review Templete
- 코더 : 김소영
- 리뷰어 : 유제민


# PRT(Peer Review Template)
[ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
- 문제에서 요구하는 기능이 정상적으로 작동하는지?
    - 해당 조건을 만족하는 부분의 코드 및 결과물을 근거로 첨부
    - 
    - Quest3_01
    - def update_min_max():
        nonlocal min_value, max_value
        for number in numbers:
            if number < min_value:
                min_value = number
            if number > max_value:
                max_value = number
    - 최대 값과 최소 값을 분류하는 함수를 깔끔하게 작성했습니다.
    -
    - Quest3_02
    - def counter(func):
        count = 0

        def wrapper():
          nonlocal count  # 외부 함수의 변수를 참조
          count += 1  # 호출될 때마다 횟수를 1 증가
          print(f"{func.__name__} 실행횟수 : {count}")  # 함수의 이름과 호출 횟수를 출력.
          return func()
        return wrapper  # 내부 함수를 반환
    - counter 데코레이터를 조건에 맞게 잘 작성했습니다.
      
[ ]  **2. 핵심적이거나 복잡하고 이해하기 어려운 부분에 작성된 설명을 보고 해당 코드가 잘 이해되었나요?**
- 해당 코드 블럭에 doc string/annotation/markdown이 달려 있는지 확인
- 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
- 주석을 보고 코드 이해가 잘 되었는지 확인
    - 잘 작성되었다고 생각되는 부분을 근거로 첨부합니다.
    - 
    - Quest03_01
    - update_min_max()  # 리스트 순회하여 초기 최솟값과 최댓값 설정
    - 함수 내부의 기능에 대해 정확한 설명이 들어가 있습니다.
 
    - Quest03_02
    - def counter(func):
        count = 0

        def wrapper():
          nonlocal count  # 외부 함수의 변수를 참조
          count += 1  # 호출될 때마다 횟수를 1 증가
          print(f"{func.__name__} 실행횟수 : {count}")  # 함수의 이름과 호출 횟수를 출력.
        return func()

      return wrapper  # 내부 함수를 반환
    - 데코레이터의 기능에 대해 설명이 잘 적혀있습니다.
        
[ ]  **3. 에러가 난 부분을 디버깅하여 “문제를 해결한 기록”을 남겼나요? 또는 “새로운 시도 및 추가 실험”을 해봤나요?**
- 문제 원인 및 해결 과정을 잘 기록하였는지 확인
- 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 실험이 기록되어 있는지 확인
    - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
    - 
    - 따로 문제를 해결한 기록이나 새로운 시도 및 추가 실험에 대한 내용은 없습니다.
    - 코드를 작성하다 난해했던 부분이나 틀렸던 내용을 어떻게 수정했는지 적혀 있으면 좋을거 같습니다.
        
[ ]  **4. 회고를 잘 작성했나요?**
- 프로젝트 결과물에 대해 배운점과 아쉬운점, 느낀점 등이 상세히 기록 되어 있나요?
- 딥러닝 모델의 경우, 인풋이 들어가 최종적으로 아웃풋이 나오기까지의 전체 흐름을 도식화하여 모델 아키텍쳐에 대한 이해를 돕고 있는지 확인
- 
- Quest 진행하면서 느낀점과 배운 것을 잘 알 수 있었습니다.
        
[ ]  **5. 코드가 간결하고 효율적인가요?**
- 파이썬 스타일 가이드 (PEP8)를 준수하였는지 확인
- 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 모듈화(함수화) 했는지
- 
    - 잘 작성되었다고 생각되는 부분을 근거로 첨부합니다.
    - Quest3_01
    - def update_min_max():
        nonlocal min_value, max_value
        for number in numbers:
            if number < min_value:
                min_value = number
            if number > max_value:
                max_value = number
    - Quest3_01 최대 값과 최소 값을 구하는 함수를 짧게 잘 정리했다고 생각합니다.

# 참고 링크 및 코드 개선
- 파이썬 스타일 가이드 (PEP8)를 준수하였는지 확인
- [코드 개선]
- Quest03_02
    def counter(func):
        count = 0

        def wrapper():
          nonlocal count  # 외부 함수의 변수를 참조
          count += 1  # 호출될 때마다 횟수를 1 증가
          print(f"{func.__name__} 실행횟수 : {count}")  # 함수의 이름과 호출 횟수를 출력.
        return func() --> func() 으로 변경 return 을 주지 않고 func() 호출로도 say_hello를 불러올 수 있기 때문

      return wrapper  # 내부 함수를 반환

