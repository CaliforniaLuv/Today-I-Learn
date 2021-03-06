### 1. 시간 복잡도

  - 입력값이 커짐에 따라 증가하는 시간의 비율을 최소화한 알고리즘
  - 주로 Big-O 표기법을 사용
  - 빅오 표기법은 최악의 경우를 고려
  - 최악이 경우 예: 해당 알고리즘 출력 시간이 100초 소요됨. 그러나 실제로 걸린 시간이 1시간
  - O(1): 입력값이 증가하더라도 시간이 늘어나지 않음. 다시 말해 입력값의 크기와 관계없이, 즉시 출력값을 얻어낼 수 있다는 의미
  - O(n): 입력값이 증가함에 따라 시간 또한 같은 비율로 증가, 입력값이 증가함에 따라 같은 비율로 걸리는 시간이 늘어남
  - O(log n): O(1) 다음으로 빠른 시간 복잡도, BST의 값 탐색도 같은 로직으로 O(log n)의 시간 복잡도를 가진 알고리즘(탐색기법)
  - O(n^2): 입력값이 증가함에 따라 시간이 n의 제곱수의 비율로 증가, 예를 들어 입력값이 1일 경우 1초가 걸리던 알고리즘에 5라는 값을 주었더니 25초가 걸리게 된다면 이 알고리즘의 시간 복잡도는 O(n2)
  - O(2^n): Big-O 표기법 중 가장 느린 시간 복잡도, 재귀로 구현하는 피보나치 수열은 O(2^n)의 시간 복잡도를 가진 대표적인 알고리즘
