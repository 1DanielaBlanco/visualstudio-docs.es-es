---
title: BasicType | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- BasicType enumeration
ms.assetid: 19ae53ba-cd6e-47b6-9f94-27ae663ce955
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3bc24a62281e754af8d97e641e8fa6e6866f7570
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318033"
---
# <a name="basictype"></a>BasicType
Especifica el tipo básico del símbolo.

## <a name="syntax"></a>Sintaxis

```C++
enum BasicType {
    btNoType   = 0,
    btVoid     = 1,
    btChar     = 2,
    btWChar    = 3,
    btInt      = 6,
    btUInt     = 7,
    btFloat    = 8,
    btBCD      = 9,
    btBool     = 10,
    btLong     = 13,
    btULong    = 14,
    btCurrency = 25,
    btDate     = 26,
    btVariant  = 27,
    btComplex  = 28,
    btBit      = 29,
    btBSTR     = 30,
    btHresult  = 31,
    btChar16   = 32,  // char16_t
    btChar32   = 33,  // char32_t
};
```

## <a name="elements"></a>Elementos
btNoType  
Se especifica ningún tipo básico.

btVoid  
Tipo básico es un `void`.

btChar  
Tipo básico es un `char` (tipo de C o C++).

btWChar  
Es de tipo básico de caracteres anchos (Unicode) (`WCHAR`).

btInt  
Es de tipo básico `signed int` (tipo de C o C++).

btUInt  
Es de tipo básico `unsigned int` (tipo de C o C++).

btFloat  
Tipo básico es un número de punto flotante (`FLOAT`).

btBCD  
Tipo básico es un decimal codificado en binario (`BCD`).

btBool  
Tipo básico es un valor booleano (`BOOL`).

btLong  
Tipo básico es un `long int` (tipo de C o C++).

btULong  
Tipo básico es un `unsigned long int` (tipo de C o C++).

btCurrency  
Tipo básico es la moneda.

btDate  
Tipo básico es la fecha y hora (`DATE`).

btVariant  
Tipo básico es una estructura de tipo de variable (`VARIANT`).

btComplex  
Tipo básico es un número complejo.

btBit  
Tipo básico es un poco.

btBSTR  
Tipo básico es una cadena binaria o básica (`BSTR`).

btHresult  
Tipo básico es un `HRESULT`.

## <a name="remarks"></a>Comentarios
Devuelven los valores de esta enumeración la [Get_basetype](../../debugger/debug-interface-access/idiasymbol-get-basetype.md) método.

## <a name="requirements"></a>Requisitos
Encabezado: cvconst.h

## <a name="see-also"></a>Vea también
[Enumeraciones y estructuras](../../debugger/debug-interface-access/enumerations-and-structures.md)  
[IDiaSymbol::get_baseType](../../debugger/debug-interface-access/idiasymbol-get-basetype.md)  
[IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol-get-length.md)
