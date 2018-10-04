---
title: Guardar datos mediante el uso de una transacción | Documentos de Microsoft
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- saving data, using transactions
- System.Transactions namespace
- transactions, saving data
- data [Visual Studio], saving
ms.assetid: 8b835e8f-34a3-413d-9bb5-ebaeb87f1198
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: c88bd18e8b02c62a31743427bf70cc7eac68ed79
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47575158"
---
# <a name="save-data-by-using-a-transaction"></a>Guardar datos mediante una transacción
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [guardar datos mediante el uso de una transacción](https://docs.microsoft.com/visualstudio/data-tools/save-data-by-using-a-transaction).  
  
  
Guardar datos en una transacción mediante la <xref:System.Transactions> espacio de nombres. Use la <xref:System.Transactions.TransactionScope> objeto participe en una transacción que se administra automáticamente.  
  
 Los proyectos no se crean con una referencia al ensamblado System.Transactions, por lo que deberá agregar manualmente una referencia a los proyectos que utilizan transacciones.  
  
> [!NOTE]
>  El <xref:System.Transactions> espacio de nombres se admite en Windows 2000 o posterior.  
  
 La manera más fácil de implementar una transacción es crear una instancia un <xref:System.Transactions.TransactionScope> objeto en un `using` instrucción. (Para obtener más información, consulte [instrucción Using](http://msdn.microsoft.com/library/665d1580-dd54-4e96-a9a9-6be2a68948f1), y [instrucción using](http://msdn.microsoft.com/library/afc355e6-f0b9-4240-94dd-0d93f17d9fc3).) El código que se ejecuta dentro de la `using` instrucción participa en la transacción.  
  
 Para confirmar la transacción, llame a la <xref:System.Transactions.TransactionScope.Complete%2A> bloquear el método como el uso de la última instrucción.  
  
 Para revertir la transacción, producir una excepción antes de llamar a la <xref:System.Transactions.TransactionScope.Complete%2A> método.  
  
 Para obtener más información, consulte [guardar datos en una transacción](../data-tools/save-data-in-a-transaction.md).  
  
### <a name="to-add-a-reference-to-the-systemtransactions-dll"></a>Para agregar una referencia al archivo dll System.Transactions  
  
1.  En el **proyecto** menú, seleccione **Agregar referencia**.  
  
2.  En el **.NET** ficha (**SQL Server** ficha para proyectos de SQL Server), seleccione **System.Transactions**y, luego,**Aceptar**.  
  
     En el proyecto se agrega una referencia a System.Transactions.dll.  
  
### <a name="to-save-data-in-a-transaction"></a>Para guardar los datos en una transacción  
  
-   Agregar código para guardar los datos de uso de la instrucción que contiene la transacción. El código siguiente muestra cómo crear y crear una instancia de un <xref:System.Transactions.TransactionScope> objeto en un formulario mediante declaración:  
  
     [!code-csharp[VbRaddataSaving#11](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Form2.cs#11)]
     [!code-vb[VbRaddataSaving#11](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Form2.vb#11)]  
  
## <a name="see-also"></a>Vea también  
 [Guardar los datos de nuevo en la base de datos](../data-tools/save-data-back-to-the-database.md)
