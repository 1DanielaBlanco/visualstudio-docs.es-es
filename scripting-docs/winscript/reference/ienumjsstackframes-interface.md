---
title: IEnumJsStackFrames (interfaz) | Documentos de Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 49e7b425-df17-4d7f-87ff-0bc82715c911
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c26470e02f6c7e5d8911df7e743bce0cb0e560bb
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "54087885"
---
# <a name="ienumjsstackframes-interface"></a>IEnumJsStackFrames (Interfaz)
Implementado por el depurador para proporcionar la pila de desenredado a jscript9diag.dll para JavaScript.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp
IEnumJsStackFrames : public IUnknown;  
```  
  
## <a name="members"></a>Miembros  
  
### <a name="public-methods"></a>Métodos públicos  
  
|Name|Descripción|  
|----------|-----------------|  
|[IEnumJsStackFrames::Next (Método)](../../winscript/reference/ienumjsstackframes-next-method.md)|Obtiene el número de marcos especificado.|  
|[IEnumJsStackFrames::Reset (Método)](../../winscript/reference/ienumjsstackframes-reset-method.md)|Restablece el marco de pila a la posición anterior al primer elemento.|  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** jscript9diag.h  
  
## <a name="see-also"></a>Vea también  
 [Referencia de interfaces de Windows Script](../../winscript/reference/windows-script-interfaces-reference.md)