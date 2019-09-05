# Introduce

## Button Test 1

IE8~IE11+, Chrome, Firefox, S`<button class="gui-btn">버튼</button>`7을 배제하면서 input 타입 제외!!

* 기본적으로 줄바꿈 없음! 줄바꿈이 필요할 경우는 해당 style css파일에서 별도 스타일 적용!!

  [HTML](./) [SCRIPT](./) [STYLE](./)

{% code-tabs %}
{% code-tabs-item title="scripts" %}
```javascript
;(function ($, global, GsBase) {

    if (GsBase.device == 'pc') {
        $(document).on('focusin', '.gui-btn', function(){
            $(this).addClass('focus')
        })
        .on('focusout mouseleave', '.gui-btn', function(){
            $(this).removeClass('focus')
        });

        // IE 버튼 active 
        if (GsBase.browserName == 'ie') {
            $(document).on('mousedown', '.gui-btn', function(){
                $(this).addClass('active')
            })
            .on('mouseup', '.gui-btn', function(){
                $(this).removeClass('active')
            });
        }
    }
}) (jQuery, window, window.GsBase = window.GsBase || {});
```
{% endcode-tabs-item %}

{% code-tabs-item title="css" %}
```css
// 상대경로로 common 지정!!

@import "../common/styles/basic/component/button";
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Bold

## Options

사이즈\( Height \)의 경우 폰트 크기에 맞게 변경되는 가변 단위였으나  
PC 브라우져별 한글 line-height의 차이가 보여 크로스 브라우징을 위해 사이즈 고정

* 옵션 : 사이즈, 컬러, 라운딩, 글라데이션
* Size : mini, tiny, small, default, large, big, huge, giant

### Size

### Color

```text

```

### Gradiant

```text

```

### Invert

```text

```

### Invert Dimmer

```text

```

### Radius

```text
Round2
Round3
Round
Round5
Round10
```

### With Icon \(sprite images\)

```text
오른쪽 sprite image 아이콘 




왼쪽 sprite image 아이콘
```

### Only Icon

```text
// 아이콘 버튼
이전 상품보기
다음 상품보기
```

### Group Button

```text
// 라운딩 처리 : 클래스 round 추가

    Group 1
    Group 2
    Group 3
```

