---
title: Resolver ambigüedad cuadro de diálogo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.Disambig
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Resolve Ambiguity dialog box
- debugger, Resolve Ambiguity dialog box
- debugging [C++], resolving ambiguity
ms.assetid: d9f47455-a116-4c84-8bad-2dfbf4d77f74
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2cad82add5d397991f2c3e7532bbbf2559f9819e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "55033078"
---
# <a name="resolve-ambiguity-dialog-box"></a>Resolver ambigüedad (cuadro de diálogo)
El cuadro de diálogo `Resolve Ambiguity` aparece cuando el depurador no puede elegir qué ubicación va a mostrar. Por ejemplo, si utiliza plantillas de C++, puede crear varias funciones a partir de una única plantilla de función. Si el depurador se detiene en una ubicación del código fuente de la plantilla, y elige `Go To Disassembly`, el depurador ofrece varias opciones. Cada función creada a partir de la plantilla tiene su propio código de desensamblado, y el depurador no sabe qué código es el que debe mostrar. El cuadro de diálogo `Resolve Ambiguity` permite seleccionar la ubicación deseada en una lista con todas las ubicaciones correspondientes.  
  
 `Choose the specific location`  
 Enumera todas las ubicaciones correspondientes del comando.  
  
 `Address`  
 Muestra las direcciones de memoria de cada función.  
  
 `Function`  
 Muestra el nombre de cada función.  
  
 `Module`  
 Muestra el módulo (EXE o DLL) que contiene el código objeto de la función.  
  
## <a name="see-also"></a>Vea también  
 [Expresiones en el depurador](../debugger/expressions-in-the-debugger.md)