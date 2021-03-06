---
layout: default
title: image
parent: 기초객체(2D)
grand_parent: enuSpace Tutorial
last_modified_date: now
---

# image

![](./assets/tutorial/image_image.png)

---

이미지 객체에 대하여 설명합니다. enuSpace는 SVG의 포맷을 이용하며, 확장된 속성 정보를 포함하고 있습니다.

## Properties

아래의 테이블의 속성정보는 스크립트상에서 연계되는 속성 이름과 데이터 타입정보 입니다.

| Property | Type | Description | Value |
| :--- | :--- | :--- | :--- |
| visibility | bool | 객체의 visibility 속성 | true, false |
| lock | bool | 객체의 잠금 속성 | true, false |
| x | float | 객체의 x위치 속성 | value |
| y | float | 객체의 y위치 속성 | value |
| width | float | 객체의 넓이 속성 | value |
| height | float | 객체의 높이 속성 | value  |
| href | string | 객체의 파일 패스 속성 | value |
| translate\_x | float | 객체의 x축 이동 | value |
| translate\_y | float | 객체의 y축 이동 | value |
| scale\_x | float | 객체의 x 스케일 | value |
| scale\_y | float | 객체의 y 스케일 | value |
| center\_x | float | 객체의 x 센터 설정 | value |
| center\_y | float | 객체의 y 센터 설정 | value |

#### 

## Script Example

스크립트는 lua스크립트와 javascript를 이용하여 적용할 수 있습니다.

객체의 속성을 설정하는 방법에는 직접 객체의 변수에 접근하여 적용하는 방법과 [SetAttribute](/ScriptAPI/SetAttribute.html)함수를 통하여 적용할 수 있습니다. 직접 변수에 접근하고자 할 경우에는 위 테이블의 속성이름을 통하여 접근을 수행합니다.

SetAttribute함수는 전역기반의 함수로 객체의 이름과 속성을 조합하여 값을 설정합니다. 스크립트를 SVG노드에서 추가하였을 경우에는 해당객체의 ID와 속성을 통하여 스크립트를 작성합니다.

### lua Script

lua Script \(객체내부의 onmousedown 함수에서의 구현한 예시\)

```lua
function _onmousedown()

    --TODO Add your lua script code here
    href = "\\resource\\jupiter_logo.png"
    -- or SetAttribute("ID_IMAGE.href", "\\resource\\jupiter_logo.png")        

end
```

lua Script \(SVG의 onmousedown 함수에서의 구현한 예시\)

```lua
function _onmousedown()

    --TODO Add your lua script code here
    ID_IMAGE.href = "\\resource\\jupiter_logo.png"
    -- or SetAttribute("ID_IMAGE.href", "\\resource\\jupiter_logo.png")    
end
```

### javascript

javascript를 이용하여 적용하였을 경우, 웹 랜더러를 이용하여 동적 웹 가시화가 가능합니다.

javascript \(객체내부의 onmousedown 함수에서의 구현한 예시\)

```js
function _onmousedown()
{    
    //TODO Add your javascript code here
    href = "\\resource\\jupiter_logo.png";

}
```

## enuSpace의 속성 윈도우

enuSpace 스튜디오를 통하여 객체의 편집 및 속성정보를 확인할 수 있습니다.

![](./assets/tutorial/image_property.png)

## SVG Tag 예시

객체의 내부에 추가된 스크립트 예시

```xml
<?xml version="1.0" encoding="UTF-16"?>
<svg
	id="ID_1evI63"
	stroke="rgb(0,119,189)"
	stroke-opacity="1.00"
	stroke-width="1.00"
	transform="translate(0.00,0.00) rotate(0.00) scale(1.0000, 1.0000)"
	pg-xcenter="0.00"
	pg-ycenter="0.00"
	style="stroke:rgb(127,127,127);stroke-opacity:1.00;stroke-width:2.00;stroke-dasharray:1,1,1;"
	enuspace-version="3.0.3.0"
	xmlns="http://www.w3.org/2000/svg"
	xmlns:xlink="http://www.w3.org/1999/xlink"
	width="1920"
	height="1080"
>
	<image
		id="ID_IMAGE"
		stroke="rgb(65,65,65)"
		stroke-opacity="1.00"
		stroke-width="1.00"
		transform="translate(58.76,105.05) rotate(0.00) scale(1.0000, 1.0000)"
		pg-xcenter="0.00"
		pg-ycenter="0.00"
		stroke-linecap="butt"
 		stroke-linejoin="miter"
 		stroke-dasharray="1 1"
 		onmousedown="_onmousedown()"
		x="0.00"
		y="124.45"
		width="149.35"
		height="137.55"
		xlink:href="\resource\jupiter_logo.png"
	>
		<script
			id="ID_1evebm"
			type="text/javascript"
		>
				<![CDATA[
function _onmousedown()
{	
	//TODO Add your javascript code here
	href = "\\resource\\jupiter_logo.png";
}]]>
		</script>
	</image>
</svg>

```

## 



