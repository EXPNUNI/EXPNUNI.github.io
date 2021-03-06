---
layout: default
title: CreateTrend
parent: Script API
last_modified_date: now
---
# CreateTrend\(id, x, y, width, height, transx, trnasy\)

CreateTrend\(\)

#### Parameters

id : id값을 입력합니다.

x : x축의 좌표를 입력합니다.

y : y축의 좌표를 입력합니다.

width : 폭의 값을 입력합니다.

height : 높이값을 입력합니다.

transx : x축의 이동값을 입력합니다.

transy : y축의 이동값을 입력합니다.

#### Return Value

none

#### Remarks

스크립트를 이용하여 동적으로 트랜드 객체를 생성합니다. 생성된 객체의 속성을 변경하고자 하는 경우에는 [SetAttribute\(\)](https://expnuni.github.io/enuspace_doc/docs/enusscriptapi_setattribute/)함수를 이용합니다.

```lua
-- lua
CreateTrend("ID_TREND", 100, 100, 500, 300, 100, 100)
```

```js
// javascript
CreateTrend("ID_TREND", 100, 100, 500, 300, 100, 100);
```

#### 

#### Examples

```lua
-- lua
function _onmousedown()
    CreateTrend("ID_TREND", 100, 100, 500, 300, 100, 100)
end
```

```js
// JavaScript
function _onmousedown()
{    
    CreateTrend("ID_TREND", 100, 100, 500, 300, 100, 100);
}
```



