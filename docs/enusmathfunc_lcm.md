---
layout: default
title: LCM
parent: Math functions
grand_parent: Math & Statistics
last_modified_date: now
---

# LCM

Ensor.LCM\(Ensor\* pEnsor\)

#### Parameters

* Ensor\* pEnsor

Ensor.new\(\) 함수등에 의해 만들어진 포인터를 입력합니다.

#### Return Value

Ensor\* pRetEnsor : pEnsor의 엘리먼트에 대한 Least Common Multiple Ensor\*를 반환합니다.

#### Remarks

#### Examples

```lua
function MathEquation()
     local ensor_x = ensor.new("{24,36}")
     local ensor_y = ensor.LCM(ensor_x)

     ensor.Table(ensor_y)
 end
```

#### Result

![](./MathAPI/LCMResult.png)

