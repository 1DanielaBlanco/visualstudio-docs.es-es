---
title: IDebugExpressionContext (interfaz) | Documentos de Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugExpressionContext Interface
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugExpressionContext interface
ms.assetid: 52af82e8-0dec-49e2-a7f3-d00f66ca1401
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 12b997d5edab866f77dcb71f4d5ea0273786c577
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345986"
---
# <a name="idebugexpressioncontext-interface"></a>IDebugExpressionContext (Interfaz)
Representa un contexto donde se pueden evaluar expresiones. El objeto de marco de pila implementa esta interfaz.  
  
 Además de los métodos heredados de `IUnknown`, el `IDebugExpressionContext` interfaz expone los métodos siguientes.  
  
## <a name="methods-in-vtable-order"></a>Métodos en orden de Vtable  
  
|Método|Descripción|  
|------------|-----------------|  
|[IDebugExpressionContext::ParseLanguageText](../../winscript/reference/idebugexpressioncontext-parselanguagetext.md)|Crea una expresión de depuración para el texto especificado.|  
|[IDebugExpressionContext::GetLanguageInfo](../../winscript/reference/idebugexpressioncontext-getlanguageinfo.md)|Devuelve un nombre y GUID para el lenguaje que posee este contexto.|