---
title: "CMFCPropertyGridColorProperty 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCPropertyGridColorProperty
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::CMFCPropertyGridColorProperty
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::EnableAutomaticButton
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::EnableOtherButton
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::GetColor
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::SetColor
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::SetColumnsNumber
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::SetOriginalValue
dev_langs:
- C++
helpviewer_keywords:
- CMFCPropertyGridColorProperty [MFC], CMFCPropertyGridColorProperty
- CMFCPropertyGridColorProperty [MFC], EnableAutomaticButton
- CMFCPropertyGridColorProperty [MFC], EnableOtherButton
- CMFCPropertyGridColorProperty [MFC], GetColor
- CMFCPropertyGridColorProperty [MFC], SetColor
- CMFCPropertyGridColorProperty [MFC], SetColumnsNumber
- CMFCPropertyGridColorProperty [MFC], SetOriginalValue
ms.assetid: af37be93-a91e-40a2-9a65-0f3412c6f0f8
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 33c807343c29fca74168167ef5d784e056b350fa
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="cmfcpropertygridcolorproperty-class"></a>CMFCPropertyGridColorProperty 类
`CMFCPropertyGridColorProperty` 类支持用于打开颜色选择对话框的属性列表控件项。  
  
## <a name="syntax"></a>语法  
  
```  
class CMFCPropertyGridColorProperty : public CMFCPropertyGridProperty  
```  
  
## <a name="members"></a>成员  
  
### <a name="public-constructors"></a>公共构造函数  
  
|名称|描述|  
|----------|-----------------|  
|[CMFCPropertyGridColorProperty::CMFCPropertyGridColorProperty](#cmfcpropertygridcolorproperty)|构造 `CMFCPropertyGridColorProperty` 对象。|  
|`CMFCPropertyGridColorProperty::~CMFCPropertyGridColorProperty`|析构函数。|  
  
### <a name="public-methods"></a>公共方法  
  
|名称|描述|  
|----------|-----------------|  
|[CMFCPropertyGridColorProperty::EnableAutomaticButton](#enableautomaticbutton)|使*自动*颜色选择对话框上的按钮。 (标准的自动按钮标记为**自动**。)|  
|[CMFCPropertyGridColorProperty::EnableOtherButton](#enableotherbutton)|使*其他*颜色选择对话框上的按钮。 (标准其他按钮标记为**其他颜色**。)|  
|`CMFCPropertyGridColorProperty::FormatProperty`|设置属性值的文本表示形式的格式。 (重写[cmfcpropertygridproperty:: Formatproperty](../../mfc/reference/cmfcpropertygridproperty-class.md#formatproperty)。)|  
|[CMFCPropertyGridColorProperty::GetColor](#getcolor)|获取属性的当前颜色。|  
|`CMFCPropertyGridColorProperty::GetThisClass`|由框架用于获取指向的指针[CRuntimeClass](../../mfc/reference/cruntimeclass-structure.md)与此类类型关联的对象。|  
|`CMFCPropertyGridColorProperty::OnClickButton`|当用户单击属性中包含的按钮时，由框架调用。 (重写[cmfcpropertygridproperty:: Onclickbutton](../../mfc/reference/cmfcpropertygridproperty-class.md#onclickbutton)。)|  
|`CMFCPropertyGridColorProperty::OnDrawValue`|由框架调用以显示属性值。 (重写[cmfcpropertygridproperty:: Ondrawvalue](../../mfc/reference/cmfcpropertygridproperty-class.md#ondrawvalue)。)|  
|`CMFCPropertyGridColorProperty::OnEdit`|当用户要修改属性值时由框架调用。 (重写[cmfcpropertygridproperty:: Onedit](../../mfc/reference/cmfcpropertygridproperty-class.md#onedit)。)|  
|`CMFCPropertyGridColorProperty::OnUpdateValue`|当可编辑属性值已更改时由框架调用。 (重写[cmfcpropertygridproperty:: Onupdatevalue](../../mfc/reference/cmfcpropertygridproperty-class.md#onupdatevalue)。)|  
|[CMFCPropertyGridColorProperty::SetColor](#setcolor)|设置属性的新颜色。|  
|[CMFCPropertyGridColorProperty::SetColumnsNumber](#setcolumnsnumber)|指定当前颜色属性网格中的列数。|  
|[CMFCPropertyGridColorProperty::SetOriginalValue](#setoriginalvalue)|设置可编辑属性的原始值。|  
  
## <a name="remarks"></a>备注  
 `CMFCPropertyGridColorProperty` 类支持可添加到属性列表控件的颜色属性。 有关详细信息，请参阅[CMFCPropertyGridCtrl 类](../../mfc/reference/cmfcpropertygridctrl-class.md)。  
  
## <a name="example"></a>示例  
 下面的示例演示如何构造 `CMFCPropertyGridColorProperty` 类的对象，以及如何使用 `CMFCPropertyGridColorProperty` 类的各种方法来配置此对象。 下面的代码介绍如何启用“自动”按钮和“其他”按钮，以及如何设置颜色和列数。 此示例摘自[新控件示例](../../visual-cpp-samples.md)。  
  
 [!code-cpp[NVC_MFC_NewControls#13](../../mfc/reference/codesnippet/cpp/cmfcpropertygridcolorproperty-class_1.cpp)]  
  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CMFCPropertyGridProperty](../../mfc/reference/cmfcpropertygridproperty-class.md)  
  
 [CMFCPropertyGridColorProperty](../../mfc/reference/cmfcpropertygridcolorproperty-class.md)  
  
## <a name="requirements"></a>惠?  
 **标头：** afxpropertygridctrl.h  
  
##  <a name="cmfcpropertygridcolorproperty"></a>CMFCPropertyGridColorProperty::CMFCPropertyGridColorProperty  
 构造 `CMFCPropertyGridColorProperty` 对象。  
  
```  
CMFCPropertyGridColorProperty(
    const CString& strName,  
    const COLORREF& color,  
    CPalette* pPalette = NULL,  
    LPCTSTR lpszDescr = NULL,  
    DWORD_PTR dwData = 0);
```  
  
### <a name="parameters"></a>参数  
 [in] `strName`  
 属性的名称。  
  
 [in] `color`  
 属性的颜色值。  
  
 [in] `pPalette`  
 指向一个颜色的调色板。 默认值为 `NULL`。  
  
 [in] `lpszDescr`  
 属性说明中。 默认值为 `NULL`。  
  
 [in] `dwData`  
 应用程序特定数据，如整数或与属性关联的其他数据的指针。 默认值为 0。  
  
##  <a name="enableautomaticbutton"></a>CMFCPropertyGridColorProperty::EnableAutomaticButton  
 使*自动*颜色选择对话框上的按钮。 (标准的自动按钮标记为**自动**。)  
  
```  
void EnableAutomaticButton(
    LPCTSTR lpszLabel,  
    COLORREF colorAutomatic,  
    BOOL bEnable=TRUE);
```  
  
### <a name="parameters"></a>参数  
 [in] `lpszLabel`  
 自动按钮标签文本。  
  
 [in] `colorAutomatic`  
 自动 （默认值） 颜色的 RGB 颜色值。  
  
 [in] `bEnable`  
 `TRUE`若要启用自动按钮;否则为`FALSE`。 默认值为 `TRUE`。  
  
### <a name="remarks"></a>备注  
  
##  <a name="enableotherbutton"></a>CMFCPropertyGridColorProperty::EnableOtherButton  
 使*其他*颜色选择对话框上的按钮。 (标准其他按钮标记为**其他颜色**。)  
  
```  
void EnableOtherButton(
    LPCTSTR lpszLabel,  
    BOOL bAltColorDlg = TRUE,  
    BOOL bEnable = TRUE);
```  
  
### <a name="parameters"></a>参数  
 [in] `lpszLabel`  
 其他按钮的标签文本。  
  
 [in] `bAltColorDlg`  
 `TRUE`若要显示`CMFCColorDialog`对话框;`FALSE`以显示标准颜色选择对话框。 默认值为 `TRUE`。  
  
 [in] `bEnable`  
 `TRUE`若要显示其他按钮;否则为`FALSE`。  默认值为 `TRUE`。  
  
### <a name="remarks"></a>备注  
  
##  <a name="getcolor"></a>CMFCPropertyGridColorProperty::GetColor  
 获取属性的当前颜色。  
  
```  
COLORREF GetColor() const;  
```  
  
### <a name="return-value"></a>返回值  
 RGB 颜色值。  
  
### <a name="remarks"></a>备注  
  
##  <a name="setcolor"></a>CMFCPropertyGridColorProperty::SetColor  
 设置属性的新颜色。  
  
```  
void SetColor(COLORREF color);
```  
  
### <a name="parameters"></a>参数  
 [in] `color`  
 RGB 颜色值。  
  
### <a name="remarks"></a>备注  
  
##  <a name="setcolumnsnumber"></a>CMFCPropertyGridColorProperty::SetColumnsNumber  
 指定当前颜色属性网格中的列数。  
  
```  
void SetColumnsNumber(int nColumnsNumber);
```  
  
### <a name="parameters"></a>参数  
 [in] `nColumnsNumber`  
 首选在颜色属性网格中的列数。  
  
### <a name="remarks"></a>备注  
 此方法设置的值`m_nColumnsNumber`受保护的数据成员。  
  
##  <a name="setoriginalvalue"></a>CMFCPropertyGridColorProperty::SetOriginalValue  
 设置可编辑属性的原始值。  
  
```  
virtual void SetOriginalValue(const COleVariant& varValue);
```  
  
### <a name="parameters"></a>参数  
 [in] `varValue`  
 一个值。  
  
### <a name="remarks"></a>备注  
 使用[cmfcpropertygridproperty:: Resetoriginalvalue](../../mfc/reference/cmfcpropertygridproperty-class.md#resetoriginalvalue)方法来重置已编辑属性的原始值。  
  
## <a name="see-also"></a>请参阅  
 [层次结构图](../../mfc/hierarchy-chart.md)   
 [类](../../mfc/reference/mfc-classes.md)   
 [CMFCPropertyGridCtrl 类](../../mfc/reference/cmfcpropertygridctrl-class.md)   
 [CMFCPropertyGridProperty 类](../../mfc/reference/cmfcpropertygridproperty-class.md)
