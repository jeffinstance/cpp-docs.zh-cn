---
title: "实施 CComObject、 CComAggObject 和 CComPolyObject |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CComPolyObject
- CComAggObject
- CComObject
dev_langs:
- C++
helpviewer_keywords:
- CComPolyObject class, implementing
- CreateInstance method
- CComAggObject class
- CComObject class, implementing
ms.assetid: 5aabe938-104d-492e-9c41-9f7fb1c62098
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 54f237a629c4af9ea7ae30aeca21c03786abcd97
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="implementing-ccomobject-ccomaggobject-and-ccompolyobject"></a>实施 CComObject、 CComAggObject 和 CComPolyObject
模板类[CComObject](../atl/reference/ccomobject-class.md)， [CComAggObject](../atl/reference/ccomaggobject-class.md)，和[CComPolyObject](../atl/reference/ccompolyobject-class.md)始终是继承链中的大多数派生的类。 它是他们的责任来处理所有中的方法**IUnknown**: `QueryInterface`， `AddRef`，和**版本**。 此外，`CComAggObject`和`CComPolyObject`（时用于聚合对象） 提供特殊的引用计数和`QueryInterface`未知的内部对象所需的语义。  
  
 是否`CComObject`， `CComAggObject`，或`CComPolyObject`使用取决于你声明一个 （或无） 以下宏：  
  
|宏|效果|  
|-----------|------------|  
|`DECLARE_NOT_AGGREGATABLE`|始终使用`CComObject`。|  
|`DECLARE_AGGREGATABLE`|使用`CComAggObject`如果对象进行了聚合和`CComObject`如果它不是。 `CComCoClass`包含此宏因此，如果没有任何**DECLARE_\*_AGGREGATABLE**宏声明在类中，这将是默认值。|  
|`DECLARE_ONLY_AGGREGATABLE`|始终使用`CComAggObject`。 如果对象不会聚合，则返回错误。|  
|`DECLARE_POLY_AGGREGATABLE`|ATL 创建的实例**CComPolyObject\<CYourClass >**时**IClassFactory::CreateInstance**调用。 在创建期间，会检查未知的外部对象的值。 如果它是**NULL**， **IUnknown**为非聚合对象实现。 如果不是未知的外部对象**NULL**， **IUnknown**为聚合对象实现。|  
  
 使用的优点`CComAggObject`和`CComObject`在于的实现**IUnknown**针对所创建对象的类型进行了优化。 例如，非聚合的对象只需引用计数，而聚合的对象需要未知的内部对象的引用计数和指向未知的外部对象的指针。  
  
 使用的优点`CComPolyObject`是，你可以避免同时`CComAggObject`和`CComObject`处理聚合和非聚合情况你模块中。 单个`CComPolyObject`对象处理这两种情况。 这意味着你的模块中存在的 vtable 只有一个副本和函数的一个副本。 如果你 vtable 很大，这会显著降低模块大小。 但是，如果你 vtable 很小，则使用`CComPolyObject`由于未经过优化聚合或非聚合对象，可能会导致稍大一些的模块大小允许进行`CComAggObject`和`CComObject`。  
  
## <a name="see-also"></a>请参阅  
 [ATL COM 对象的基础知识](../atl/fundamentals-of-atl-com-objects.md)   
 [聚合和类工厂宏](../atl/reference/aggregation-and-class-factory-macros.md)

