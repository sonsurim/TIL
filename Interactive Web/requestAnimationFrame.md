# requesetAnimationFrame

## 정의
- 브라우저에게 수행하기를 원하는 애니메이션을 알리고 다음 리페인트가 진행되기 전에 해당 애니메이션을 업데이트하는 함수를 호출하게 하는 **자바스크립트 내장 함수**

## 특징
- 루프를 계속 돌림
- 자연스러운 움직임이 필요한 곳에 많이, 반드시 사용됨

  ( Ex. 화려한 캔버스 애니메이션, 3D 컨텐츠 )

## 예시
```
function loop() {
  console.log(1);
  window.requestAnimationFrame(loop);
}

loop();
```
- 계속해서 루프를 돌며 콘솔에 1을 찍음

  → 프레임이 계속 돌고있음
