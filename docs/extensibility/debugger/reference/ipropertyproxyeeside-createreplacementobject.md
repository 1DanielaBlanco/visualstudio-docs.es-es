---
title: IPropertyProxyEESide::CreateReplacementObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IPropertyProxyEESide::CreateReplacementObject
helpviewer_keywords:
- IPropertyProxyEESide::CreateReplacementObject
ms.assetid: 0cfe79b8-c3f1-48b0-a225-e39dee2c92fe
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: eb1c2c5478bb24f80646dcaacf64a9e6efb2e425
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54988329"
---
# <a name="ipropertyproxyeesidecreatereplacementobject"></a>IPropertyProxyEESide::CreateReplacementObject
Crea una copia de un objeto de datos específicos del evaluador de expresiones (EE).  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
HRESULT CreateReplacementObject(  
   IEEDataStorage*  dataIn,  
   IEEDataStorage** dataOut  
);  
```  
  
```csharp  
int CreateReplacementObject(  
   IEEDataStorage     dataIn,  
   out IEEDataStorage dataOut  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `dataIn`  
 [in] Un [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) objeto contiene los datos que se va a copiar.  
  
 `dataOut`  
 [out] Devuelve un nuevo `IEEDataStorage` objeto.  
  
## <a name="return-value"></a>Valor devuelto  
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve un código de error.  
  
## <a name="remarks"></a>Comentarios  
 Este método se le asigna un [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) objeto que representa una matriz de bytes. Este objeto de datos entrantes no se suele implementar mediante lo EE. Sin embargo, el objeto devuelto por este método siempre se implementa mediante EE, lo que permite la implemente EE el `IEEDataStorage` interfaz en cualquier clase es el deseado.  
  
 Tenga en cuenta que los datos proporcionan por el entrante `IEEDataStorage` objeto debe ser los mismos datos en la salida `IEEDataStorage` objeto.  
  
## <a name="see-also"></a>Vea también  
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)