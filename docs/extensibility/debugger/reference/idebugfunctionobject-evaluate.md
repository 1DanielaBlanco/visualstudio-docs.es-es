---
title: IDebugFunctionObject::Evaluate | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugFunctionObject::Evaluate
helpviewer_keywords:
- IDebugFunctionObject::Evaluate method
ms.assetid: 29349ea3-d5c1-4135-aa76-ced073ab9683
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8d7de9a5a6d159987db5816341a048e74065c128
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54954675"
---
# <a name="idebugfunctionobjectevaluate"></a>IDebugFunctionObject::Evaluate
Llama a la función y devuelve el valor resultante como un objeto.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
HRESULT Evaluate(   
   IDebugObject** ppParams,  
   DWORD          dwParams,  
   DWORD          dwTimeout,  
   IDebugObject** ppResult  
);  
```  
  
```csharp  
int Evaluate(  
   IDebugObject[]   ppParams,   
   IntPtr           dwParams,   
   uint             dwTimeout,   
   out IDebugObject ppResult  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `ppParams`  
 [in] Una matriz de [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) objetos que representan los parámetros de entrada. Cada uno de estos parámetros se creó con uno de los `Create` métodos en el [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) interfaz.  
  
 `dwParams`  
 [in] El número de parámetros en el `ppParams` matriz.  
  
 `dwTimeout`  
 [in] Especifica el tiempo máximo, en milisegundos para esperar antes de volver de este método. Use `INFINITE` para esperar indefinidamente.  
  
 `ppResult`  
 [out] Devuelve un [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) que representa el valor de la función como un objeto.  
  
## <a name="return-value"></a>Valor devuelto  
 Si se realiza correctamente, devuelve S_OK; en caso contrario, devuelve un código de error.  
  
## <a name="remarks"></a>Comentarios  
 Este método configura y ejecuta una llamada a la función representada por el [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) objeto.  
  
## <a name="see-also"></a>Vea también  
 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)