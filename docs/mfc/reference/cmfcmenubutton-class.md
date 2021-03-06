---
title: "CMFCMenuButton 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCMenuButton
- AFXMENUBUTTON/CMFCMenuButton
- AFXMENUBUTTON/CMFCMenuButton::CMFCMenuButton
- AFXMENUBUTTON/CMFCMenuButton::PreTranslateMessage
- AFXMENUBUTTON/CMFCMenuButton::SizeToContent
- AFXMENUBUTTON/CMFCMenuButton::m_bOSMenu
- AFXMENUBUTTON/CMFCMenuButton::m_bRightArrow
- AFXMENUBUTTON/CMFCMenuButton::m_bStayPressed
- AFXMENUBUTTON/CMFCMenuButton::m_hMenu
- AFXMENUBUTTON/CMFCMenuButton::m_nMenuResult
dev_langs:
- C++
helpviewer_keywords:
- CMFCMenuButton [MFC], CMFCMenuButton
- CMFCMenuButton [MFC], PreTranslateMessage
- CMFCMenuButton [MFC], SizeToContent
- CMFCMenuButton [MFC], m_bOSMenu
- CMFCMenuButton [MFC], m_bRightArrow
- CMFCMenuButton [MFC], m_bStayPressed
- CMFCMenuButton [MFC], m_hMenu
- CMFCMenuButton [MFC], m_nMenuResult
ms.assetid: 53d3d459-1e5a-47c5-8b7f-2e61f6af5187
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: fac8fe59fe5dbfb101ec0881dbf17925cf048caa
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="cmfcmenubutton-class"></a>CMFCMenuButton 类
在用户菜单选项上显示弹出菜单和报表的按钮。  
  
## <a name="syntax"></a>语法  
  
```  
class CMFCMenuButton : public CMFCButton  
```  
  
## <a name="members"></a>成员  
  
### <a name="public-constructors"></a>公共构造函数  
  
|名称|描述|  
|----------|-----------------|  
|[CMFCMenuButton::CMFCMenuButton](#cmfcmenubutton)|构造 `CMFCMenuButton` 对象。|  
  
### <a name="public-methods"></a>公共方法  
  
|名称|描述|  
|----------|-----------------|  
|[CMFCMenuButton::PreTranslateMessage](#pretranslatemessage)|由框架窗口消息进行转换之前被发送调用。 （重写 `CMFCButton::PreTranslateMessage`。）|  
|[CMFCMenuButton::SizeToContent](#sizetocontent)|根据其文本和图像的大小的按钮的大小更改。|  
  
### <a name="data-members"></a>数据成员  
  
|name|描述|  
|----------|-----------------|  
|[CMFCMenuButton::m_bOSMenu](#m_bosmenu)|指定是否可以显示的默认系统弹出菜单或者使用[CContextMenuManager::TrackPopupMenu](../../mfc/reference/ccontextmenumanager-class.md#trackpopupmenu)。|  
|[CMFCMenuButton::m_bRightArrow](#m_brightarrow)|指定是否将显示弹出菜单，下方或右侧的按钮。|  
|[CMFCMenuButton::m_bStayPressed](#m_bstaypressed)|指定用户释放左键后的菜单按钮是否更改其状态。|  
|[CMFCMenuButton::m_hMenu](#m_hmenu)|附加的 Windows 菜单句柄。|  
|[CMFCMenuButton::m_nMenuResult](#m_nmenuresult)|一个指示哪一项的标识符用户从弹出菜单中选择。|  
  
## <a name="remarks"></a>备注  
 `CMFCMenuButton`类派生自[CMFCButton 类](../../mfc/reference/cmfcbutton-class.md)，反过来，派生自[CButton 类](../../mfc/reference/cbutton-class.md)。 因此，你可以使用`CMFCMenuButton`中你的代码将使用的相同方式`CButton`。  
  
 当你创建`CMFCMenuButton`，你必须将传递句柄给相关联的弹出菜单。 接下来，调用该函数`CMFCMenuButton::SizeToContent`。 `CMFCMenuButton::SizeToContent`检查该按钮的大小足以包含指向弹出窗口出现的位置-即下方或右侧的按钮的位置的箭头。  
  
## <a name="example"></a>示例  
 下面的示例演示如何设置附加到按钮的菜单的句柄、 调整大小的按钮根据其文本和图像的大小，以及设置由框架显示的弹出菜单。 此代码片段属于[新控件示例](../../visual-cpp-samples.md)。  
  
 [!code-cpp[NVC_MFC_NewControls#38](../../mfc/reference/codesnippet/cpp/cmfcmenubutton-class_1.h)]  
[!code-cpp[NVC_MFC_NewControls#39](../../mfc/reference/codesnippet/cpp/cmfcmenubutton-class_2.cpp)]  
  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CButton](../../mfc/reference/cbutton-class.md)  
  
 [CMFCButton](../../mfc/reference/cmfcbutton-class.md)  
  
 [CMFCMenuButton](../../mfc/reference/cmfcmenubutton-class.md)  
  
## <a name="requirements"></a>惠?  
 **标头：** afxmenubutton.h  
  
##  <a name="cmfcmenubutton"></a>CMFCMenuButton::CMFCMenuButton  
 构造一个新[CMFCMenuButton](../../mfc/reference/cmfcmenubutton-class.md)对象。  
  
```  
CMFCMenuButton();
```  
  
##  <a name="m_bosmenu"></a>CMFCMenuButton::m_bOSMenu  
 指示哪个弹出菜单的 Boolean 成员变量框架显示。  
  
```  
BOOL m_bOSMenu;  
```  
  
### <a name="remarks"></a>备注  
 如果`m_bOSMenu`是`TRUE`，框架都会调用继承`TrackPopupMenu`此对象的方法。 否则，框架会调用[CContextMenuManager::TrackPopupMenu](../../mfc/reference/ccontextmenumanager-class.md#trackpopupmenu)。  
  
##  <a name="m_brightarrow"></a>CMFCMenuButton::m_bRightArrow  
 指示弹出菜单的位置的布尔成员变量。  
  
```  
BOOL m_bRightArrow;  
```  
  
### <a name="remarks"></a>备注  
 当用户按下的菜单按钮时，应用程序将显示一个弹出菜单。 框架将显示弹出菜单中的按钮下或右侧的按钮。 该按钮还包括小箭头，该值指示弹出菜单出现的位置。 如果`m_bRightArrow`是`TRUE`，框架显示弹出菜单右侧的按钮。 否则，将显示弹出菜单中的按钮下。  
  
##  <a name="m_bstaypressed"></a>CMFCMenuButton::m_bStayPressed  
 用户进行的选择从弹出菜单情况下按下的 Boolean 成员变量，该值指示是否显示的菜单按钮。  
  
```  
BOOL m_bStayPressed;  
```  
  
### <a name="remarks"></a>备注  
 如果`m_bStayPressed`成员是`FALSE`，菜单不会变得按下按钮时单击按钮时使用。 在这种情况下，框架显示仅弹出菜单。  
  
 如果`m_bStayPressed`成员是`TRUE`，用户单击按钮时，将成为要在按下了菜单按钮。 用户关闭弹出菜单中，通过以上方法选择或取消后，它始终处于直到按下。  
  
##  <a name="m_hmenu"></a>CMFCMenuButton::m_hMenu  
 附加菜单句柄。  
  
```  
HMENU m_hMenu;  
```  
  
### <a name="remarks"></a>备注  
 框架显示指示此成员变量，当用户单击的菜单按钮的菜单。  
  
##  <a name="m_nmenuresult"></a>CMFCMenuButton::m_nMenuResult  
 一个整数，指示哪一项用户从弹出菜单中选择。  
  
```  
int m_nMenuResult;  
```  
  
### <a name="remarks"></a>备注  
 如果用户取消菜单不做任何选择，或如果出错，此成员变量的值为零。  
  
##  <a name="pretranslatemessage"></a>CMFCMenuButton::PreTranslateMessage  
 由框架窗口消息进行转换之前被发送调用。  
  
```  
virtual BOOL PreTranslateMessage(MSG* pMsg);
```  
  
### <a name="parameters"></a>参数  
 [in] `pMsg`  
 指向[消息](../../mfc/reference/msg-structure1.md)结构，其中包含要处理的消息。  
  
### <a name="return-value"></a>返回值  
 如果消息已转换，并且不应将调度; 则为非 0如果消息已不转换，并且应将调度，则为 0。  
  
### <a name="remarks"></a>备注  
  
##  <a name="sizetocontent"></a>CMFCMenuButton::SizeToContent  
 根据其文本大小和映像的大小的按钮的大小更改。  
  
```  
virtual CSize SizeToContent(BOOL bCalcOnly = FALSE);
```  
  
### <a name="parameters"></a>参数  
 [in] `bCalcOnly`  
 一个布尔型参数，该值指示此方法是否调整大小的按钮。  
  
### <a name="return-value"></a>返回值  
 A [CSize](../../atl-mfc-shared/reference/csize-class.md)指定按钮的新大小的对象。  
  
### <a name="remarks"></a>备注  
 如果调用此函数和`bCalcOnly`是`TRUE`，`SizeToContent`将计算仅按钮的新大小。  
  
 按钮的新大小计算以适应按钮文本、 图像和箭头。 框架还将添加在水平边缘的 10 个像素和垂直边缘的 5 个像素的预定义的边距。  
  
## <a name="see-also"></a>请参阅  
 [层次结构图](../../mfc/hierarchy-chart.md)   
 [类](../../mfc/reference/mfc-classes.md)   
 [CMFCButton 类](../../mfc/reference/cmfcbutton-class.md)
