---
title: IDebugDocumentTextEvents2 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugDocumentTextEvents2
helpviewer_keywords:
- IDebugDocumentTextEvents2 interface
ms.assetid: a10cbb6b-11a8-4056-b42a-2ecebf0e690d
caps.latest.revision: 15
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 95eae8da7779a23e9bf285eff2f637fbcd4633e9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47577770"
---
# <a name="idebugdocumenttextevents2"></a>IDebugDocumentTextEvents2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [IDebugDocumentTextEvents2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugdocumenttextevents2).  
  
Esta interfaz se utiliza para notificar a Visual Studio sobre los cambios en el documento de origen que son proporcionados por el motor de depuración.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
IDebugDocumentTextEvents2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Notas para los implementadores  
 La DE implementa esta interfaz para admitir hacer cambios en el código fuente. Esta interfaz se implementa normalmente en el mismo objeto que implementa el [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) interfaz.  
  
## <a name="notes-for-callers"></a>Notas para los llamadores  
 [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] Obtiene esta interfaz mediante una llamada a la <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint.Advise%2A> método. El <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint> interfaz se obtiene de una llamada a la <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer.EnumConnectionPoints%2A> método. El <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer> interfaz se obtiene mediante una llamada a la [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) método en un [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) interfaz.  
  
## <a name="methods-in-vtable-order"></a>Métodos en orden de Vtable  
 La tabla siguiente muestran los métodos de `IDebugDocumentTextEvents2`.  
  
|Método|Descripción|  
|------------|-----------------|  
|[onDestroy](../../../extensibility/debugger/reference/idebugdocumenttextevents2-ondestroy.md)|Indica que se ha destruido todo el documento.|  
|[onInsertText](../../../extensibility/debugger/reference/idebugdocumenttextevents2-oninserttext.md)|Notifica el paquete de depuración que se ha insertado el texto en el documento.|  
|[onRemoveText](../../../extensibility/debugger/reference/idebugdocumenttextevents2-onremovetext.md)|Notifica el paquete de depuración que se ha quitado el texto del documento.|  
|[onReplaceText](../../../extensibility/debugger/reference/idebugdocumenttextevents2-onreplacetext.md)|Notifica el paquete de depuración que se ha reemplazado el texto del documento.|  
|[onUpdateTextAttributes](../../../extensibility/debugger/reference/idebugdocumenttextevents2-onupdatetextattributes.md)|Notifica el paquete de depuración que se han actualizado los atributos de texto en el documento.|  
|[onUpdateDocumentAttributes](../../../extensibility/debugger/reference/idebugdocumenttextevents2-onupdatedocumentattributes.md)|Notifica al receptor del evento que se han actualizado los atributos del documento.|  
  
## <a name="remarks"></a>Comentarios  
 Solo los motores de depuración que proporcione sus propios documentos podrían aprovechar las ventajas de la `IDebugDocumentTextEvent2` interfaz. Un ejemplo de esto sería un motor de depuración de secuencias de comandos. En el proceso de interpretación de secuencias de comandos, se puede generar nuevo código fuente que no está presente en cualquier archivo de disco y solo lo conoce la DE.  
  
## <a name="requirements"></a>Requisitos  
 Encabezado: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Ensamblado: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vea también  
 [IDebugDocumentText2](../../../extensibility/debugger/reference/idebugdocumenttext2.md)   
 [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md)
