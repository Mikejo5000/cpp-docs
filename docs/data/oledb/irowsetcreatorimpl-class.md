---
title: "IRowsetCreatorImpl Class | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-data"]
ms.topic: "reference"
f1_keywords: ["ATL::IRowsetCreatorImpl", "ATL.IRowsetCreatorImpl", "ATL::IRowsetCreatorImpl<T>", "ATL.IRowsetCreatorImpl<T>", "IRowsetCreatorImpl"]
dev_langs: ["C++"]
helpviewer_keywords: ["IRowsetCreatorImpl class"]
ms.assetid: 92cc950f-7978-4754-8d9a-defa63867d82
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "data-storage"]
---
# IRowsetCreatorImpl Class
Performs the same functions as `IObjectWithSite` but also enables the OLE DB properties **DBPROPCANSCROLLBACKWARDS DBPROPCANFETCHBACKWARDS**.  
  
## Syntax

```cpp
template < class T >  
class ATL_NO_VTABLE IRowsetCreatorImpl   
   : public IObjectWithSiteImpl< T >  
```  
  
#### Parameters  
 `T`  
 A class derived from **IRowsetCreator**.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[SetSite](../../data/oledb/irowsetcreatorimpl-setsite.md)|Sets the site that contains the rowset object.|  
  
## Remarks  
 This class inherits from [IObjectWithSite](http://msdn.microsoft.com/library/windows/desktop/ms693765) and overrides [IObjectWithSite::SetSite](http://msdn.microsoft.com/library/windows/desktop/ms683869). When a provider command or session object creates a rowset, it calls `QueryInterface` on the rowset object looking for `IObjectWithSite` and calls `SetSite` passing the rowset object's **IUnkown** interface as the site interface.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../../data/oledb/ole-db-provider-templates-cpp.md)   
 [OLE DB Provider Template Architecture](../../data/oledb/ole-db-provider-template-architecture.md)