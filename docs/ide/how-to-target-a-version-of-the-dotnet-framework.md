---
title: Uso de una versión de .NET Framework como destino
ms.date: 02/06/2018
ms.topic: conceptual
helpviewer_keywords:
- targeting .NET Framework [Visual Studio]
- .NET Framework version [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: bc8a808ba3a5da46b4dbe3be3aa00921ea869cb6
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55954093"
---
# <a name="how-to-target-a-version-of-the-net-framework"></a>Filtrar Uso de una versión de .NET Framework como destino

En este documento se describe cómo crear un proyecto que tiene como destino una versión de .NET Framework y cómo se cambia la versión de destino en un proyecto de Visual Basic, C# o Visual F# existente.

> [!IMPORTANT]
> Para obtener información sobre cómo cambiar la versión de destino para los proyectos de C++, vea [Cómo: Modificar la plataforma de destino y el conjunto de herramientas de la plataforma](/cpp/build/how-to-modify-the-target-framework-and-platform-toolset).

## <a name="to-target-a-version-when-you-create-a-project"></a>Para especificar una versión de destino al crear un proyecto

Al crear un proyecto, las versiones de .NET Framework disponibles dependen de qué versiones están instaladas y de la plantilla seleccionada en el cuadro de diálogo **Nuevo proyecto**.

1. En la barra de menús, elija **Archivo** > **Nuevo** > **Proyecto**.

1. En la lista de plantillas instaladas, elija el tipo de proyecto que quiere crear y escriba un nombre para el proyecto.

1. En la lista desplegable **Plataforma** situada en la parte inferior del cuadro de diálogo **Nuevo proyecto**, elija la versión de .NET Framework de destino que quiera especificar para el proyecto.

    En la lista de los plataformas se muestran solo aquellas versiones aplicables a la plantilla que eligió. Algunos tipos de proyecto, como .NET Core, no requieren .NET Framework. En tales casos, la lista desplegable **Plataforma** se mantiene oculta.

    ![Desplegable Plataforma en el cuadro de diálogo Nuevo proyecto](media/vside-newproject-framework.png)

1. Elija el botón **Aceptar** .

## <a name="to-change-the-targeted-version"></a>Para cambiar la versión de destino

Puede cambiar la versión de .NET Framework de destino en un proyecto de Visual Basic, C# o Visual F# si sigue este procedimiento.

Para obtener información sobre cómo cambiar la versión de destino para los proyectos de C++, vea [Cómo: Modificar la plataforma de destino y el conjunto de herramientas de la plataforma](/cpp/build/how-to-modify-the-target-framework-and-platform-toolset).

1. En el **Explorador de soluciones**, abra el menú contextual del proyecto que quiere cambiar y después elija **Propiedades**.

    ![Propiedades del Explorador de soluciones de Visual Studio](../ide/media/vs_slnexplorer_properties.png)

1. En la columna izquierda de la ventana **Propiedades**, elija la pestaña **Aplicación**.

    ![Propiedades de aplicación de Visual Studio, pestaña Aplicación](../ide/media/vs_slnexplorer_properties_applicationtab.png)

    > [!NOTE]
    > Después de crear una aplicación para UWP, no puede cambiar la versión de destino de Windows ni de .NET Framework.

1. En la lista **Plataforma de destino**, elija la versión que quiera.

1. En el cuadro de diálogo de comprobación que aparece, elija el botón **Sí**.

    Se descarga el proyecto. Cuando se vuelva a cargar, la versión de .NET Framework de destino será la que acaba de elegir.

    > [!NOTE]
    > Si el código contiene referencias a una versión de .NET Framework distinta de la que indicó, pueden aparecer mensajes de error al compilar o ejecutar el código. Para resolver estos errores, deberá modificar las referencias. Consulte [Solucionar problemas de versión de .NET Framework de destino](../msbuild/troubleshooting-dotnet-framework-targeting-errors.md).

## <a name="see-also"></a>Vea también

- [Información general sobre la compatibilidad con múltiples versiones de Visual Studio](../ide/visual-studio-multi-targeting-overview.md)
- [Solucionar problemas de versión de .NET Framework de destino](../msbuild/troubleshooting-dotnet-framework-targeting-errors.md)
- [Página de aplicación, Diseñador de proyectos (C#)](../ide/reference/application-page-project-designer-csharp.md)
- [Página de aplicación, Diseñador de proyectos (Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md)
- [Cómo: Modificar la plataforma de destino y el conjunto de herramientas de la plataforma (C++)](/cpp/build/how-to-modify-the-target-framework-and-platform-toolset)