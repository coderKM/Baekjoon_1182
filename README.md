# Baekjoon_1182
## 백준 - 부분수열의 합(https://www.acmicpc.net/submit/1182/29881738)
존경하는 류호석 강사님께서 로직 부분에만 집중할 수 있게 전체적인 틀은 제공해주셨다.  
부분 수열을 내 멋대로 연속된 수로 단정지어 미로에 빠졌다가,, 결국 강사님의 코드를 참고하여 문제를 풀었다.  
본인을 포함하는, 그리고 포함하지 않는 재귀호출로 깔금하게 전체적인 조합을 만들어낼 수 있다는걸 깨달았다..  

실행 순서는 다음과 같다 :

1. k : 1, value : 0 를 초기 값으로 재귀 함수를 실행
2. k 값을 비교하여 N까지 도달하지 않았을 경우, 아래와 같이 k + 1에 대한 재귀 호출
    * value + num[k] 넘겨 재귀 호출
    * value 그대로 넘겨 재귀 호출
    * 위와 같이 2회 재귀 호출을 하여 연속되지 않은 수열의 조합을 만들어낼 수 있음
3. k 값이 N에 도달하였을 경우, S값과 value값 비교하여 같을 경우 ans++
    * S값이 0일 경우, 기본 데이터(0으로 입력되어 k를 한번도 포함하지 않은 case)에 대해 ans--
4. ans 반환