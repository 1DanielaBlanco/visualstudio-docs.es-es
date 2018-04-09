---
title: Analizar las infracciones de las reglas de umbral en las pruebas de carga en Visual Studio | Microsoft Docs
ms.date: 10/19/2016
ms.topic: article
f1_keywords:
- vs.test.load.monitor.threshholdresult
helpviewer_keywords:
- load tests, thresholds
- threshold violations
- threshold counts
- load tests, threshold violations
- load test results, analyzing threshold violations
- thresholds in load tests
ms.assetid: 969ed346-cf2e-4d48-82b3-edb3e075e1c0
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-ide-test
ms.openlocfilehash: 761d277612242cc4b14b0a24d1a2ac7663b2b152
ms.sourcegitcommit: 900ed1e299cd5bba56249cef8f5cf3981b10cb1c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2018
---
# <a name="analyzing-threshold-rule-violations-in-load-tests-using-the-load-test-analyzer"></a>Analizar las infracciones de las reglas de umbral en las pruebas de carga usando el Analizador de prueba de carga

Las reglas de umbral están asociadas a contadores de rendimiento específicos, y las infracciones indican que un contador de rendimiento ha superado o no ha llegado a un valor especificado. Cuando ejecute una prueba de carga, puede analizar las infracciones que se producen para las reglas de umbral previamente definidas.

Si se ha producido alguna infracción, aparece un hipervínculo de **infracciones de umbral** en la barra de estado del Analizador de pruebas de carga con el número de infracciones que se han producido. Puede elegir el hipervínculo para mostrar la tabla de infracciones de umbral. También puede ver las infracciones de umbral en la ventana **Contadores** y en el gráfico.

## <a name="view-threshold-violations-in-the-table"></a>Ver las infracciones de umbral en la tabla

 La tabla de infracciones de umbral muestra las primeras 1.000 infracciones. La tabla siguiente contiene estas columnas:

|Columna|Description|Visible de forma predeterminada|
|------------|-----------------|------------------------|
|Tiempo|La hora de la prueba de carga a la que se produjo la infracción.|Sí|
|Equipo|El nombre del equipo bajo comprobación en el que se produjo la infracción. **Nota:** Esto es importante cuando se ejecutan pruebas de carga en plataformas de pruebas.|Sí|
|Categoría|La categoría del contador de rendimiento en el que se produjo la infracción.|Sí|
|Contador|El nombre del contador de rendimiento en el que se produjo la infracción.|Sí|
|Instancia|La instancia del contador de rendimiento en la que se produjo la infracción.|Sí|
|Mensaje|Mensaje que describe la infracción de umbral. Por ejemplo, **El valor 5 supera el valor de umbral crítico de 0**.|Sí|

> [!NOTE]
> Puede ordenar la tabla eligiendo los encabezados de columna.

 Para obtener más información, vea [Analizar los errores y resultados de pruebas de carga en la vista Tablas](../test/analyze-load-test-results-and-errors-in-the-tables-view.md).

## <a name="view-threshold-violations-in-the-counters-panel"></a>Ver las infracciones de umbral en el panel Contadores

 Puede ver las infracciones de umbral en el panel **Contadores**, en el árbol que contiene los contadores de rendimiento de la prueba de carga. Los iconos del panel **Contadores** indican las infracciones de umbral. El icono puede ser alguno de los siguientes:

 El icono puede ser alguno de los siguientes:

 ![Ninguna infracción del umbral](../test/media/icon_ltest_1.gif "Icon_LTest_1") Ninguna infracción del umbral.

 ![Se ha producido una infracción del umbral grave en el último intervalo](../test/media/icon_ltest_2.gif "Icon_LTest_2") Se ha producido una infracción del umbral grave en el último intervalo.

 ![Se ha producido una infracción del umbral grave en un intervalo anterior](../test/media/icon_ltest_3.gif "Icon_LTest_3") Se ha producido una infracción del umbral grave en un intervalo anterior.

 ![Se ha producido una infracción del umbral de advertencia en el último intervalo](../test/media/icon_ltest_4.gif "Icon_LTest_4") Se ha producido una infracción del umbral de advertencia en el último intervalo.

 ![Se ha producido una infracción del umbral de advertencia en un intervalo anterior](../test/media/icon_ltest_5.gif "Icon_LTest_5") Se ha producido una infracción del umbral de advertencia en un intervalo anterior.

 Opcionalmente, las infracciones del umbral también se pueden mostrar en el gráfico. El icono de umbral aparece en el gráfico junto al punto de datos donde se ha producido la infracción de umbral.

 En el árbol de contadores, el icono de una infracción de umbral se propaga desde el nodo de contador específico hasta el nodo raíz. Esto sirve para avisarle de que una infracción en un contador puede no estar visible en el árbol porque éste no se ha expandido.

 Para obtener más información, vea [Usar el panel Contadores en vista Gráficos y la vista Tablas](../test/counters-panel-in-load-test-analyzer.md).

## <a name="view-threshold-violations-on-the-graph"></a>Ver las infracciones de umbral en el gráfico

 Puede ver las infracciones de umbral en el gráfico. Al igual que en el panel **Contadores**, los iconos indican las infracciones de umbral en el gráfico. Los iconos aparecen en el gráfico junto al punto de datos donde se ha producido la infracción de umbral. Si se produce una infracción de umbral en un contador que no aparece en el gráfico, puede agregarlo a este si lo arrastra desde el panel **Contadores** al gráfico.

 Para obtener más información, vea [Analizar los resultados de pruebas de carga en la vista Gráficos del Analizador de pruebas de carga](../test/analyze-load-test-results-in-the-graphs-view.md).

## <a name="see-also"></a>Vea también

- [Especificar los conjuntos de contadores y las reglas de umbral para equipos en una prueba de carga](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md)
- [Analizar resultados de pruebas de carga](../test/analyze-load-test-results-using-the-load-test-analyzer.md)
- [Analizar los errores y resultados de pruebas de carga en la vista Tablas](../test/analyze-load-test-results-and-errors-in-the-tables-view.md)