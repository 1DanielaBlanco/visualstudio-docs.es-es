---
title: Encapsulado, sangría y alineación de parámetros
ms.date: 02/13/2019
ms.topic: reference
author: kendrahavens
ms.author: kendrahavens
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 1490ff0bcae91a6f4870b0cfb623d975fa1e064b
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/18/2019
ms.locfileid: "56335886"
---
# <a name="wrap-indent-and-align-parameters"></a>Encapsulado, sangría y alineación de parámetros

Esta refactorización se aplica a lo siguiente:

- C#

- Visual Basic

**Qué:** permite encapsular, aplicar sangría y alinear parámetros.

**Cuándo:** si se tiene una llamada o declaración de método con varios parámetros.

**Por qué:** es más fácil leer una larga lista de parámetros cuando están encapsulados o con una sangría según la preferencia del usuario.

## <a name="how-to"></a>Procedimiento

1. Coloque el cursor en una lista de parámetros.
2. Presione **Ctrl**+**.** para activar el menú **Acciones rápidas y refactorizaciones**.

   ![Encapsulado, sangría y alineación de parámetros](media/wrap-parameters.png)

3. Presione **ENTRAR** para aceptar la refactorización.

   ![Aplicación de encapsulado, sangría y alineación de parámetros](media/wrap-parameters-completed.png)

## <a name="see-also"></a>Vea también

- [Refactorización](../refactoring-in-visual-studio.md)
