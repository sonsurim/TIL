# requesetAnimationFrame

## 정의
- 브라우저에게 수행하기를 원하는 애니메이션을 알리고 다음 리페인트가 진행되기 전에 해당 애니메이션을 업데이트하는 함수를 호출하게 하는 **자바스크립트 내장 함수**

## 특징
- 루프를 계속 돌림
- 자연스러운 움직임이 필요한 곳에 많이, 반드시 사용됨

  ( Ex. 화려한 캔버스 애니메이션, 3D 컨텐츠 )

## 문법
```
function loop() {
  console.log(1);
  window.requestAnimationFrame(loop);
}

loop();
```
- 계속해서 루프를 돌며 콘솔에 1을 찍음

  → 프레임이 계속 돌고있음

## 예제
```
let cursor_item;
let x = 0;
let y = 0;
let mouseX = 0;
let mouseY = 0;
let speed = 0.05;

window.onload = function(){
  cursor_item = document.getElementsByClassName('cursor_item')[0];
  window.addEventListener('mousemove', mouseFunc, false);

  function mouseFunc(e) {
    x = e.clientX;
    y = e.clientY;
  }

  loop();

  function loop() {
    mouseX += (x - mouseX) * speed;
    mouseY += (y - mouseY) * speed
    cursor_item.style.transform = `translate(${mouseX}px, ${mouseY}px)`
    window.requestAnimationFrame(loop);
  }
}
```
- `mouseX += (x - mouseX) * speed`

> 움직일 값 += (현재 마우스 위치 - 바로 전 위치 값) * 0.05

- Ex. 위치가 0, 마우스 현재 위치가 100인 경우 (0에서 100만큼 이동)

  `0 += (100 - 0) * 0.05` // 5, 10, 15, ...

  - requsetAnimationFrame 미적용 : 한 번에 + 100 → 바로 이동함으로 모션이 부드럽지 않음
  - requsetAnimationFrame 적용 : 조금씩 작은 수를 더함 → 천천히 이동함으로 모션이 부드러움
