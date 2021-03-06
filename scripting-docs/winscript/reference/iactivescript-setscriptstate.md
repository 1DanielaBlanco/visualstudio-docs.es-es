---
title: 'IActiveScript:: Setscriptstate | Documentos de Microsoft'
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.SetScriptState
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_SetScriptState
ms.assetid: f2b2700c-0c8d-40db-ad84-dc751c5d9bc2
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 58edef17fec1d94a09b327dff626658c42a273ba
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095035"
---
# <a name="iactivescriptsetscriptstate"></a>IActiveScript::SetScriptState
Coloca el motor de scripting en el estado especificado. Este método se pueda llamar desde subprocesos no son de base sin resultante en una llamada que no sea de base a los objetos de host o a la [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md) interfaz.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp
HRESULT SetScriptState(  
    SCRIPTSTATE ss  // identifier of new state  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `ss`  
 [in] Establece el motor de scripting en el estado especificado. Puede ser uno de los valores definidos en el [SCRIPTSTATE (enumeración)](../../winscript/reference/scriptstate-enumeration.md) enumeración.  
  
## <a name="return-value"></a>Valor devuelto  
 Devuelve uno de los siguientes valores:  
  
|Valor devuelto|Significado|  
|------------------|-------------|  
|`S_OK`|Correcto.|  
|`E_FAIL`|El motor de scripting no admite la transición al estado inicializado. El host debe descartar este motor de scripting y crear, inicializar y cargar un nuevo motor de scripting para lograr el mismo efecto.|  
|`E_UNEXPECTED`|No se esperaba la llamada (por ejemplo, el motor de scripting no se ha cargado o inicializado) y, por tanto, no se pudo.|  
|`OLESCRIPT_S_PENDING`|El método se puso en cola correctamente, pero aún no ha cambiado el estado. Cuando los cambios de estado, el sitio se volverá a llamar a través de la [IActiveScriptSite::OnStateChange](../../winscript/reference/iactivescriptsite-onstatechange.md) método.|  
|`S_FALSE`|El método se realizó correctamente, pero la secuencia de comandos ya estaba en el estado especificado.|  
  
## <a name="remarks"></a>Comentarios  
 Para obtener más información acerca de Estados del motor de scripting, vea la sección de Estados del motor de secuencia de comandos de [motores de scripts de Windows](../../winscript/windows-script-engines.md) .  
  
## <a name="see-also"></a>Vea también  
 [IActiveScript:: Clone](../../winscript/reference/iactivescript-clone.md)   
 [IActiveScript:: Getscriptdispatch](../../winscript/reference/iactivescript-getscriptdispatch.md)   
 [IActiveScript:: Interruptscriptthread](../../winscript/reference/iactivescript-interruptscriptthread.md)   
 [Iactivescriptparse:: Parsescripttext](../../winscript/reference/iactivescriptparse-parsescripttext.md)   
 [IActiveScriptSite::GetItemInfo](../../winscript/reference/iactivescriptsite-getiteminfo.md)