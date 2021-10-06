# Component
SPA를 만들기 위해 기본이 되는 Component

## 설명
```js
new Component(target, props);
```
- props: 상속받은 데이터 저장하는 변수
- target: 작성한 html을 적용할 element

### 동작 원리
```js
constructor(target, props) {
  this._props = props
  this._target = target;
  this.init();
  this.render();
  this.setEvent();
}
```
1. 매개변수로 받아준 props, target을 내부변수에 매핑시켜준다.
2. init() : 필요한 상수나 변수를 미리 초기화해준다. (state에 담아준다!)
3. render() : 만들어놓은 html template을 적용시켜줌
4. setEvent() : template까지 적용이 되었다면, 이제 이벤트를 걸어주자.
