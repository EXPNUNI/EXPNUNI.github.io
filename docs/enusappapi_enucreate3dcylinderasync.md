---
layout: default
title: enuCreate3DCylinderAsync
parent: Application API
last_modified_date: now
---
# void enuCreate3DCylinderAsync\(HX3D pX3DHandler, wchar\_t\* strID, float height, float radius, float slices, float transx, float transy, float transz\)

void enuCreate3DCylinderAsync\(HX3D pX3DHandler, wchar\_t\* strID, float height, float radius, float slices, float transx, float transy, float transz\)

#### Parameters

* HX3D pX3DHandler

3d 픽쳐 핸들을 입력합니다.

* wchar\_t\* strID

생성객체의 ID를 지정합니다.

* float height

3D Cylinder객체의 높이값을 입력합니다.

* float radius

3D Cylinder객체의 반지름을 입력합니다.

* float slices

3d Cylinder객체의 slice개수를 입력합니다.

* float transx

3d Cylinder객체의 x축 이동값을 입력합니다.

* float transy

3d Cylinder객체의 y축 이동값을 입력합니다.

* float transz

3d Cylinder객체의 z축 이동값을 입력합니다.

#### Return Value

Type : NONE

#### Remarks

3d 픽쳐 핸들을 이용하여 3d Cylinder객체를 생성합니다.

#### Examples

```cpp
HVIEW ViewHandle = NULL; 
void CSampleView::OnInitialUpdate() 
{ 
    CView::OnInitialUpdate(); 

    enuCreateProject(); 

    // Load Project
    enuLoadProjectFile(L"Project\\sample.enup"); 

    // Create View
    ViewHandle = enuCreate3DView(this->m_hWnd); 

    // ENU View Attach Set Page 
    enuSetX3dPageView(ViewHandle , L"picture\\core_3d.x3d");

    // Get X3D picture handle
    HX3D pX3D = enuGetX3DHandler(ViewHandle); 

    // Create 3D Cylinder.
    enuCreate3DCylinderAsync(pX3D,L"MyCylinder", 100, 100, 10, 0, 0, 0);        // 비동기식 호출    
}
```



