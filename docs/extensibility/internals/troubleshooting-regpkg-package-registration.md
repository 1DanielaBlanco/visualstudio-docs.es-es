---
title: Solución de problemas de registro de paquete RegPkg | Documentos de Microsoft
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- RegPkg
ms.assetid: f33f822f-697a-4bad-9c10-554b4c8f6246
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8a5d8a8a63aabafb9c658d43fc90c1bb28918c8e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54943544"
---
# <a name="troubleshooting-regpkg-package-registration"></a>Solución de problemas del registro de paquete RegPkg
> [!NOTE]
>  Es la mejor manera de registrar paquetes en Visual Studio mediante el uso de los archivos .pkgdef. Esto permite la implementación de extensión sin necesidad de tener acceso al registro del sistema. Archivos pkgdef se crean mediante el [utilidad CreatePkgDef](../../extensibility/internals/createpkgdef-utility.md).  
  
 Para registrar un paquete mediante el uso de RegPkg en [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], debe usar la versión de RegPkg que sea adecuado para el paquete.  
  
## <a name="regpkg-versions-related-to-package-versions"></a>Versiones de RegPkg relacionado con las versiones de paquete  
 Hay dos versiones de RegPkg. Se incluye una versión en [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Use esta versión para registrar los paquetes que se han creado mediante uno de los siguientes ensamblados:  
  
1. Microsoft.VisualStudioShell.9.0.dll  
  
2. Microsoft.VisualStudioShell.10.0.dll  
  
3. Microsoft.VisualStudioShell.11.0.dll  
  
   No puede registrar paquetes que se han creado mediante el ensamblado Microsoft.VisualStudio.Shell.dll anterior.  
  
   La versión anterior de RegPkg puede registrar paquetes que se han creado mediante el ensamblado Microsoft.VisualStudio.Shell.dll. Sin embargo, que no registre los paquetes creados mediante el uso de las versiones posteriores de ese ensamblado.  
  
## <a name="see-also"></a>Vea también  
 [VSPackages](../../extensibility/internals/vspackages.md)