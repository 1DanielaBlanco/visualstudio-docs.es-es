---
title: BUILT_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BUILT_TYPE
helpviewer_keywords:
- BUILT_TYPE structure
ms.assetid: cc02c32c-0f65-4210-ad25-a9b1899066e8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 692391379c3f2581e535a9e5c885f776565fb93d
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315498"
---
# <a name="builttype"></a>BUILT_TYPE
Esta estructura especifica información sobre un tipo de campo que se toman de los metadatos.

## <a name="syntax"></a>Sintaxis

```cpp
typedef struct _tagTYPE_BUILT {
    ULONG32      ulAppDomainID;
    GUID         guidModule;
    IDebugField* pUnderlyingField;
} BUILT_TYPE;
```

```csharp
public struct BUILT_TYPE {
    public uint        ulAppDomainID;
    public Guid        guidModule;
    public IDebugField pUnderlyingField;
};
```

#### <a name="parameters"></a>Parámetros
ulAppDomainID  
Identificador de la aplicación del que procede el símbolo. Esto se utiliza para identificar de forma exclusiva una instancia de la aplicación.

guidModule  
El GUID del módulo que contiene este campo.

pUnderlyingField  
Un [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) objeto que identifica el campo subyacente asociado a este campo integrado.

## <a name="remarks"></a>Comentarios
Esta estructura aparece como parte de la unión en el [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) estructura cuando la `dwKind` campo de la `TYPE_INFO` estructura está establecida en `TYPE_KIND_BUILT` (un valor de la [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) enumeración).

## <a name="requirements"></a>Requisitos
Encabezado: sh.h

Espacio de nombres:  Microsoft.VisualStudio.Debugger.Interop

Ensamblado: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Vea también
[Estructuras y uniones](../../../extensibility/debugger/reference/structures-and-unions.md)  
[TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)  
[dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)  
[IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
