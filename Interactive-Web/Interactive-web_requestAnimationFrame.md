# requesetAnimationFrame

## μ μ π
- λΈλΌμ°μ μκ² μννκΈ°λ₯Ό μνλ μ λλ©μ΄μμ μλ¦¬κ³  λ€μ λ¦¬νμΈνΈκ° μ§νλκΈ° μ μ ν΄λΉ μ λλ©μ΄μμ μλ°μ΄νΈνλ ν¨μλ₯Ό νΈμΆνκ² νλ **μλ°μ€ν¬λ¦½νΈ λ΄μ₯ ν¨μ**

## νΉμ§ π
- λ£¨νλ₯Ό κ³μ λλ¦Ό
- μμ°μ€λ¬μ΄ μμ§μμ΄ νμν κ³³μ λ§μ΄, λ°λμ μ¬μ©λ¨

  ( Ex. νλ €ν μΊλ²μ€ μ λλ©μ΄μ, 3D μ»¨νμΈ  )

## λ¬Έλ² π
```
function loop() {
  console.log(1);
  window.requestAnimationFrame(loop);
}

loop();
```
- κ³μν΄μ λ£¨νλ₯Ό λλ©° μ½μμ 1μ μ°μ

  β νλ μμ΄ κ³μ λκ³ μμ

## μμ  π
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

> μμ§μΌ κ° += (νμ¬ λ§μ°μ€ μμΉ - λ°λ‘ μ  μμΉ κ°) * 0.05

- Ex. μμΉκ° 0, λ§μ°μ€ νμ¬ μμΉκ° 100μΈ κ²½μ° (0μμ 100λ§νΌ μ΄λ)

  `0 += (100 - 0) * 0.05` // 5, 10, 15, ...

  - requsetAnimationFrame λ―Έμ μ© : ν λ²μ + 100 β λ°λ‘ μ΄λν¨μΌλ‘ λͺ¨μμ΄ λΆλλ½μ§ μμ
  - requsetAnimationFrame μ μ© : μ‘°κΈμ© μμ μλ₯Ό λν¨ β μ²μ²ν μ΄λν¨μΌλ‘ λͺ¨μμ΄ λΆλλ¬μ

- - -
μμ λ΄μ©μ Interactive Webμ κ³΅λΆνλ©° κ°μΈμ μΌλ‘ μ λ¦¬ν λ΄μ©μλλ€.
## μΆμ² π
- [μΈνλ° κ°μ - λͺ μ€λ‘ λλ΄λ μΈν°λν°λΈ μΉ κ°λ° λΈνμ° [μ΄κΈνΈ]](https://www.inflearn.com/course/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9D%B8%ED%84%B0%EB%9E%99%ED%8B%B0%EB%B8%8C-%EC%9B%B9/dashboard)