---
title: "IRowsetLocateImpl::Compare | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-data"]
ms.topic: "reference"
f1_keywords: ["ATL.IRowsetLocateImpl.Compare", "IRowsetLocateImpl::Compare", "IRowsetLocateImpl.Compare", "ATL::IRowsetLocateImpl::Compare"]
dev_langs: ["C++"]
helpviewer_keywords: ["Compare method"]
ms.assetid: 6f84052c-c68c-480a-982f-03748faa7d5d
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "data-storage"]
---
# IRowsetLocateImpl::Compare
Compares two bookmarks.  
  
## Syntax  
  
```cpp
      STDMETHOD (Compare )(HCHAPTER /* hReserved */,  
   DBBKMARK cbBookmark1,  
   const BYTE* pBookmark1,  
   DBBKMARK cbBookmark2,  
   const BYTE* pBookmark2,  
   DBCOMPARE* pComparison);  
```  
  
#### Parameters  
 See [IRowsetLocate::Compare](https://msdn.microsoft.com/en-us/library/ms709539.aspx) in the *OLE DB Programmer's Reference*.  
  
## Remarks  
 Either of the bookmarks can be a standard OLE DB-defined [standard bookmark](https://msdn.microsoft.com/en-us/library/ms712954.aspx) (**DBBMK_FIRST**, **DBBMK_LAST**, or **DBBMK_INVALID**). The value returned in `pComparison` indicates the relationship between the two bookmarks:  
  
-   **DBCOMPARE_LT** (`cbBookmark1` is before `cbBookmark2`.)  
  
-   **DBCOMPARE_EQ** (`cbBookmark1` is equal to `cbBookmark2`.)  
  
-   **DBCOMPARE_GT** (`cbBookmark1` is after `cbBookmark2`.)  
  
-   **DBCOMPARE_NE** (The bookmarks are equal and not ordered.)  
  
-   **DBCOMPARE_NOTCOMPARABLE** (The bookmarks cannot be compared.)  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetLocateImpl Class](../../data/oledb/irowsetlocateimpl-class.md)