---
layout: default
title: SetAttribute3D
parent: Script API
last_modified_date: now
---
# SetAttribute3D\(\)

SetAttribute3D\(\)

#### Parameters

variable : 속성값을 적용하고자하는 변수이름을 입력합니다.

value : 속성값을 입력합니다.

#### Return Value

none

#### Remarks

그래픽 객체의 속성값을 변경하는 함수입니다. 객체의 속성에 값을 할당합니다.

SetAttribute3D의 함수는 문자열형태로 변수명과 값을 입력하여 처리됩니다.

```lua
-- lua
SetAttribute3D("ID_BOX.size_x", "10")

-- equal expression
ID_BOX.size_x = 10
```

```js
// javascript
SetAttribute3D("ID_BOX.size_x", "10");

// equal expression
ID_BOX.size_x" = 10;
```

#### 

#### Examples

```lua
-- lua
function _onmousedown()
    SetAttribute3D("ID_BOX.size_x", "10")
end
```

```js
// JavaScript
function _onmousedown()
{    
    SetAttribute3D("ID_BOX.size_x", "10");
}
```



