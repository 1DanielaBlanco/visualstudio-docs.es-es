---
title: Tarea AssignTargetPath| Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 0e830e31-3bcf-4259-b2a8-a5df49b92d51
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: efae349037d6a826c4d267e12d901306eed7629b
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2019
ms.locfileid: "54758702"
---
# <a name="assigntargetpath-task"></a>AssignTargetPath (Tarea)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Esta tarea acepta una archivos de lista de archivos y agrega atributos `<TargetPath>` si no se han especificado ya.  
  
## <a name="task-parameters"></a>Parámetros de tareas  
 En la siguiente tabla se describen los parámetros de la tarea `AssignTargetPath`.  
  
|Parámetro|Descripción|  
|---------------|-----------------|  
|`RootFolder`|Parámetro de entrada `string` opcional.<br /><br /> Contiene la ruta de acceso a la carpeta que contiene los vínculos de destino.|  
|`Files`|Parámetro de entrada <xref:Microsoft.Build.Framework.ITaskItem>`[]` opcional.<br /><br /> Contiene la lista de entrada de archivos.|  
|`AssignedFiles`|Optional<br /><br /> Parámetro de salida <xref:Microsoft.Build.Framework.ITaskItem> `[]`.<br /><br /> Contiene la lista de archivos resultante.|  
  
## <a name="remarks"></a>Comentarios  
 Además de los parámetros mencionados anteriormente, esta tarea hereda los parámetros de la clase <xref:Microsoft.Build.Tasks.TaskExtension>, que a su vez hereda de la clase <xref:Microsoft.Build.Utilities.Task>. Para obtener una lista de estos parámetros adicionales y sus descripciones, vea [TaskExtension Base Class](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Ejemplo  
 En el siguiente ejemplo se ejecuta la tarea `AssignTargetPath` para configurar un proyecto.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="MyProject">  
        <AssignTargetPath  
RootFolder="Resources"  
            Files="@(ResourceFiles)"  
            <Output TaskParameter="AssignedFiles"  
                ItemName="OutAssignedFiles"/>  
        </AssignTargetPath>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Vea también  
 [Tareas](../msbuild/msbuild-tasks.md)   
 [Referencia de tareas](../msbuild/msbuild-task-reference.md)
