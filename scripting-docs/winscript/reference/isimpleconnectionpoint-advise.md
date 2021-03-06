---
title: ISimpleConnectionPoint::Advise | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ISimpleConnectionPoint.Advise
apilocation:
- pdm.dll
helpviewer_keywords:
- ISimpleConnectionPoint::Advise
ms.assetid: 59ded60d-b938-4110-aca3-e69ba234ca9a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b3c0ea37e6fabb051458a11c4838061126bd98bf
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "54091746"
---
# <a name="isimpleconnectionpointadvise"></a>ISimpleConnectionPoint::Advise
Establece una conexión entre el objeto de punto de conexión simple y el receptor del cliente.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp
HRESULT Advise(  
   IDispatch*  pdisp,  
   DWORD*      pdwCookie  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `pdisp`  
 [in] Puntero a la `IDispatch` receptor de notificaciones de interfaz en el cliente. Receptor del cliente que recibe llamadas salientes desde el punto de conexión simple.  
  
 `pdwCookie`  
 [out] Puntero a un token devuelto que identifica esta conexión. El llamador utiliza este token posteriormente para eliminar la conexión pasándolo a la `ISimpleConnectionPoint::Unadvise` método. Si la conexión no se ha establecido correctamente, este valor es cero.  
  
## <a name="return-value"></a>Valor devuelto  
 El método devuelve un objeto `HRESULT`. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.  
  
|Valor|Descripción|  
|-----------|-----------------|  
|`S_OK`|El método se realizó correctamente.|  
  
## <a name="remarks"></a>Comentarios  
 Este método establece una conexión entre el objeto de punto de conexión simple y el receptor del cliente.  
  
## <a name="see-also"></a>Vea también  
 [ISimpleConnectionPoint (interfaz)](../../winscript/reference/isimpleconnectionpoint-interface.md)   
 [ISimpleConnectionPoint::Unadvise](../../winscript/reference/isimpleconnectionpoint-unadvise.md)