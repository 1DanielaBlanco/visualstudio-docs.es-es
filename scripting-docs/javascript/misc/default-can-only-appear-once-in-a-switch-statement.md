---
title: "'default' solo puede aparecer una vez en una instrucción 'switch' | Microsoft Docs"
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- javascript
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.WebClient.Help.SCRIPT1027
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: a94100f4-6ee5-4759-b635-9d309e47111e
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a4f254825e27793999932b772ac4bc2512908fae
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/16/2019
ms.locfileid: "54347312"
---
# <a name="default-can-only-appear-once-in-a-switch-statement"></a>'default' solo puede aparecer una vez en una instrucción 'switch'.
Se intentó utilizar el **predeterminada** instrucción más de una vez dentro de una instrucción switch. El caso predeterminado siempre es la última instrucción case en una instrucción switch (es el caso desestimado).  
  
### <a name="to-correct-this-error"></a>Para corregir este error  
  
-   Quite cualquier adicional **predeterminada** caso las instrucciones de su `switch` instrucción (uso en la mayoría una instrucción case default en la instrucción switch).  
  
## <a name="see-also"></a>Vea también  
 [switch (instrucción)](../../javascript/reference/switch-statement-javascript.md)   
 [Controlar el flujo del programa](../../javascript/controlling-program-flow-javascript.md)   
 [Palabras reservadas de JavaScript](../../javascript/reference/javascript-reserved-words.md)