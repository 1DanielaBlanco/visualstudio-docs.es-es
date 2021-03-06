---
title: Instalar analizadores de Roslyn
ms.date: 08/03/2018
ms.topic: conceptual
helpviewer_keywords:
- code analysis, managed code
- analyzers
- Roslyn analyzers
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: de4818a57dc09825e6f41a635ea777a9e3f06e2a
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55910516"
---
# <a name="install-net-compiler-platform-analyzers"></a>Instalar analizadores de .NET Compiler Platform

Visual Studio 2017 incluye un conjunto básico de .NET Compiler Platform (*Roslyn*) analizadores. Estos analizadores están siempre disponibles. Puede instalar analizadores adicionales como paquetes de NuGet, o como extensiones de Visual Studio en *VSIX* archivos.

## <a name="to-install-nuget-analyzer-packages"></a>Para instalar paquetes de NuGet analyzer

1. Busque el paquete de analizador que desea instalar en www.nuget.org. Por ejemplo, es posible que desee [instalar los analizadores de FxCop Microsoft](install-fxcop-analyzers.md#to-install-fxcop-analyzers-as-a-nuget-package) para comprobar el código para los problemas de seguridad y rendimiento, entre otros.

2. Instale el paquete en Visual Studio, ya sea mediante el [Package Manager Console](/nuget/quickstart/install-and-use-a-package-in-visual-studio#package-manager-console) o [UI del Administrador de paquetes](/nuget/quickstart/install-and-use-a-package-in-visual-studio#package-manager-console).

   > [!NOTE]
   > La página www.nuget.org para cada paquete del analizador muestra el comando Pegar en el **Package Manager Console**. Incluso hay un botón útil para copiar el texto en el Portapapeles.
   >
   > ![Página de NuGet.org que muestra comandos de consola de administrador de paquetes](media/nuget-install-command.png)

   Los ensamblados del analizador se instalan y aparecen en **el Explorador de soluciones** en **referencias** > **analizadores**.

## <a name="to-install-vsix-analyzers"></a>Para instalar analizadores VSIX

1. En Visual Studio, seleccione **herramientas** > **extensiones y actualizaciones**.

   Se abre el cuadro de diálogo **Extensiones y actualizaciones**.

   > [!NOTE]
   > Como alternativa, puede buscar y descargar la extensión del analizador de directamente desde [Visual Studio Marketplace](https://marketplace.visualstudio.com).

2. Expanda **Online** en el panel izquierdo y, a continuación, seleccione **Visual Studio Marketplace**.

3. En el cuadro de búsqueda, escriba el nombre de la extensión del analizador que desea instalar. Por ejemplo, es posible que desee [instalar los analizadores de FxCop Microsoft](install-fxcop-analyzers.md#to-install-fxcop-analyzers-as-a-vsix) para comprobar el código para los problemas de seguridad y rendimiento, entre otros.

4. Seleccione **descargar**.

   Descargar la extensión.

5. Seleccione **Aceptar** para cerrar el cuadro de diálogo y, a continuación, cierre todas las instancias de Visual Studio para iniciar el **instalador de VSIX**.

   El **instalador de VSIX** abre el cuadro de diálogo.

   ![Instalador de VSIX para el análisis de código de Microsoft](media/vsix-installer-code-analysis.png)

6. Seleccione **modificar** para iniciar la instalación.

7. Después de un minuto o dos, se completa la instalación. Seleccione **cerrar**.

8. Vuelva a abrir Visual Studio.

Si desea comprobar si la extensión está instalada, seleccione **herramientas** > **extensiones y actualizaciones**. En el **extensiones y actualizaciones** cuadro de diálogo, seleccione el **instalado** categoría de la izquierda y, a continuación, busque la extensión por nombre.

## <a name="next-steps"></a>Pasos siguientes

> [!div class="nextstepaction"]
> [Usar analizadores de Roslyn en Visual Studio](../code-quality/use-roslyn-analyzers.md)

## <a name="see-also"></a>Vea también

- [Información general de los analizadores de Roslyn en Visual Studio](../code-quality/roslyn-analyzers-overview.md)
- [Instalar analizadores de FxCop](../code-quality/install-fxcop-analyzers.md)