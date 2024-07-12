---
author: 이규철 <leegyu4dev@gmail.com>
date: 2024-07-12
---

# DOM/Focus

브라우저 DOM 요소 focus / blur를 활용한 기능은 UI 이벤트들과 충돌이 발생할 수 있다.\

## focus를 가질 수 있는 환경

- a, button, input, select, textarea, iframe 요소는 기본적으로 focus를 가질 수 있다.
- 특정 속성이 있는 요소
    - [contenteditable="true"]
    - [tabindex]

## focus/blur

기본적으로 이벤트 버블링이 일어나지 않는다.

- refs.
    - <https://developer.mozilla.org/en-US/docs/Web/API/Element/focus_event>
    - <https://developer.mozilla.org/en-US/docs/Web/API/Element/blur_event>

## focusin/focusout

내부 자식 요소들의 포커스 이벤트, 포커스 잃음에 대하여 버블링이 일어난다.

- refs.
    - <https://developer.mozilla.org/en-US/docs/Web/API/Element/focusin_event>
    - <https://developer.mozilla.org/en-US/docs/Web/API/Element/focusout_event>

## FocusEvent

- `FocusEvent.relatedTarget` 속성을 통해 포커스를 잃은 요소를 참조할 수 있다.
- aa

## 문제 케이스

### #1 document.execCommand('copy')

보통 execCommand('copy')를 사용할 때, input, textarea 요소에 focus를 주고 실행한다.\
이때, blur 이벤트가 발생하면서 특정한 이벤트 처리를 했다면, execCommand('copy') 실행이 적절히 되지 않는 문제가 있다.

```js
const input = document.createElement('input');

input.addEventListener('blur', () => {
    console.log('blur');
});

```
