# Info
[호숫가의 개미굴](https://boj.kr/28325)

- 난이도: 골드 5
- 분류: 다이나믹 프로그래밍, 그리디 알고리즘

## 💡 풀이 방법 요약

DP 를 사용해서 풀었습니다.

주의할 점은, 1번방과 N번방이 붙어있다는 점입니다.

이를 위해 상황을 나눠서 DP 를 구성했습니다.

먼저 1번방에서 쪽방을 선택한 경우 2번방, N번방 모두 쪽방과 통로방 중 어느 것을 선택해도 상관 없으므로 2~N번방까지 DP를 통해 최대값을 구한 후 1번방의 쪽방 갯수를 더해주었습니다.

만약 1번방에서 통로방을 선택한 경우 2번방, N번방은 모두 쪽방을 선택해야 하고, 3번방부터 N-1번방까진 어느 것을 선택해도 상관 없기에 3~N-1번방까지 DP를 통해 최대값을 구한 후 1번방에서의 통로방(1)과 2, N번방에서의 쪽방 갯수를 더해주었습니다.

이후 두 값 중 최대값을 출력하면 됩니다.

## 👀 실패 이유

## 🙂 마무리

사실 두 DP 모두 점화식이 같습니다.

극한으로 시간, 공간 복잡도를 줄이고 싶다면 DP 테이블도 필요 없고 두 변수(쪽방 선택 가짓수, 통로방 선택 가짓수) 만 트래킹하면 될 것 같습니다.