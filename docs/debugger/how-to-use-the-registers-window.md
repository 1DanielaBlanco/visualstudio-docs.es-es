---
title: Ver los valores de registro en el depurador | Microsoft Docs
ms.custom: seodec18
ms.date: 11/19/2018
ms.topic: conceptual
f1_keywords:
- vs.debug.registers
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- registers, debugging
- register contents
- flags, Registers window
- register groups
- debugging [Visual Studio], Registers window
- Registers window
ms.assetid: 2918ffa2-562f-40d6-9053-ef321bbeb767
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: dfc0482152b3da0b52950ab6389cc9f7d9e83e3a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54974287"
---
# <a name="view-register-values-in-the-registers-window-c-c-visual-basic-f"></a>Ver los valores de registro en la ventana registros (C#, C++, Visual Basic, F#)

El **registra** ventana muestra el contenido del registro durante la depuración de Visual Studio. Para obtener una introducción de alto nivel conceptos relacionados con los registros y la **registra** ventana, consulte [Fundamentos de la depuración: Ventana Registros](../debugger/debugging-basics-registers-window.md).

> [!NOTE]
> Información de registro no está disponible para la secuencia de comandos o las aplicaciones SQL.

Durante la depuración, registrar el cambio de valores mientras se ejecuta código en la aplicación. Los valores que han cambiado recientemente aparecen en rojo en el **registra** ventana.

Por motivos de claridad, la ventana **Registros** organiza los registros en grupos que varían según la plataforma y el tipo de procesador. Puede mostrar u ocultar grupos de registros. Para obtener más información, vea [Cómo: mostrar y ocultar grupos de registros](../debugger/how-to-display-and-hide-register-groups.md).

Se pueden modificar los valores de los registros. Para obtener más información, vea [Cómo: editar un valor de registro](../debugger/how-to-edit-a-register-value.md).

**Para abrir la ventana registros**

1. Habilitar la depuración de nivel de dirección, seleccionando **habilitar la depuración de nivel de dirección** en **herramientas** (o **depurar**) > **opciones**  >  **Depuración**.

1. Mientras la depuración está en ejecución o en un punto de interrupción, seleccione **depurar** > **Windows** > **registra**, o bien presione **Alt** + **5**.

>[!NOTE]
>Cuadros de diálogo y comandos de menú pueden diferir dependiendo de la configuración o edición de Visual Studio. Para cambiar la configuración, seleccione **importar y exportar configuraciones** en Visual Studio **herramientas** menú. Para obtener más información, vea [Restablecer la configuración](../ide/environment-settings.md#reset-settings).

### <a name="see-also"></a>Vea también

- [Fundamentos de la depuración: Ventana Registros](../debugger/debugging-basics-registers-window.md)
- [Ver datos en el depurador](../debugger/viewing-data-in-the-debugger.md)
