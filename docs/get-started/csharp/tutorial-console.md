---
title: 'Tutorial: Introducción a las aplicaciones de consola de C#'
description: Aprenda a crear una aplicación de consola de C# en Visual Studio mediante un procedimiento paso a paso.
ms.custom: seodec18, get-started
ms.date: 12/12/2018
ms.technology: vs-ide-general
ms.prod: visual-studio-dev15
ms.topic: tutorial
ms.devlang: CSharp
author: TerryGLee
ms.author: tglee
manager: douge
dev_langs:
- CSharp
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 333eeb3f826663d979e1cec444ede7eda4b55b2a
ms.sourcegitcommit: 35bebf794f528d73d82602e096fd97d7b8f82c25
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "53562222"
---
# <a name="tutorial-get-started-with-a-c-console-app-in-visual-studio"></a>Tutorial: Introducción a la aplicación de consola de C# en Visual Studio

En este tutorial para C#, usará Visual Studio para crear y ejecutar una aplicación de consola y explorar algunas características del [entorno de desarrollo integrado (IDE) de Visual Studio](../visual-studio-ide.md) mientras lo hace.

Si todavía no ha instalado Visual Studio, vaya a la página de [descargas de Visual Studio](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) para instalarlo de forma gratuita.

## <a name="create-a-project"></a>Crear un proyecto

Para empezar, crearemos un proyecto de aplicación de C#. En el tipo de proyecto se incluyen todos los archivos de plantilla que vamos a necesitar, sin necesidad de agregar nada más.

1. Abra Visual Studio 2017.

2. En la barra de menús superior, seleccione **Archivo** > **Nuevo** > **Proyecto**.

3. En el cuadro de diálogo **Nuevo proyecto** del panel de la izquierda, expanda **C#** y seleccione **.NET Core**. En el panel central, elija **Aplicación de consola (.NET Core)**. Después, asigne el nombre *Calculator* al archivo.

   ![Plantilla de proyecto Aplicación de consola (.NET Core) en el cuadro de diálogo Nuevo proyecto en el IDE de Visual Studio](./media/new-project-csharp-calculator-console-app.png)

### <a name="add-a-workgroup-optional"></a>Agregar un grupo de trabajo (opcional)

Si no ve la plantilla de proyecto **Aplicación de consola (.NET Core)**, puede obtenerla si agrega la carga de trabajo **Desarrollo multiplataforma de .NET Core**. Para averiguar cómo hacerlo, vea la sección "[¿Qué es una carga de trabajo y cómo puedo agregar una?](#workload)" de las preguntas frecuentes.

## <a name="create-the-app"></a>Creación de la aplicación

En primer lugar, agregaremos código para crear una calculadora básica. Luego, retocaremos el código para agregarle funcionalidad. Después de eso, depuraremos la aplicación para buscar y corregir errores. Por último, perfeccionaremos el código para que sea más eficaz.

Vamos a comenzar agregando al proyecto el código de calculadora básica.

1. En el editor de código, elimine el código predeterminado "Hello World".

    ![Eliminar el código "Hello World" predeterminado de la nueva aplicación de calculadora](./media/csharp-console-calculator-deletehelloworld.png)

   En concreto, elimine todo el código que vea en el editor de código.

1. Escriba o pegue el siguiente código nuevo en el editor de código:

    ```csharp
    using System;

    namespace Calculator
    {
        class Program
        {
            static void Main(string[] args)
            {
                // Declare variables and then initialize to zero
                int num1 = 0; int num2 = 0;

                // Display title as the C# console calculator app
                Console.WriteLine("Console Calculator in C#\r");
                Console.WriteLine("------------------------\n");

                // Ask the user to type the first number
                Console.WriteLine("Type a number, and then press Enter");
                num1 = Convert.ToInt32(Console.ReadLine());

                // Ask the user to type the second number
                Console.WriteLine("Type another number, and then press Enter");
                num2 = Convert.ToInt32(Console.ReadLine());

                // Ask the user to choose an option
                Console.WriteLine("Choose an option from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                // Use a switch statement to do the math
                switch (Console.ReadLine())
                {
                    case "a":
                        Console.WriteLine($"Your result: {num1} + {num2} = " + (num1 + num2));
                        break;
                    case "s":
                        Console.WriteLine($"Your result: {num1} - {num2} = " + (num1 - num2));
                        break;
                    case "m":
                        Console.WriteLine($"Your result: {num1} * {num2} = " + (num1 * num2));
                        break;
                    case "d":
                        Console.WriteLine($"Your result: {num1} / {num2} = " + (num1 / num2));
                        break;
                }
                // Wait for the user to respond before closing
                Console.Write("Press any key to close the Calculator console app...");
                Console.ReadKey();
            }
        }
    }
    ```
1. Elija **Calculator** para ejecutar el programa, o bien presione **F5**.

   ![Elección del botón Calculator para ejecutar la aplicación desde la barra de herramientas](./media/csharp-console-calculator-button.png)

   Se abre una ventana de consola.

1. Vea la aplicación en la ventana de consola y, después, siga las indicaciones para agregar los números **42** y **119**.

   La ventana de consola debe ser similar a la de la siguiente captura de pantalla:

    ![Ventana de consola en la que se muestra la aplicación Calculator y que incluye mensajes sobre las acciones que se deben realizar](./media/csharp-console-calculator.png)

### <a name="add-decimals"></a>Agregar decimales

En este momento, la aplicación Calculator acepta y devuelve números enteros, pero será más precisa si agregamos código que permita incluir decimales.

Como se muestra en la siguiente captura de pantalla, si ejecutamos la aplicación y dividimos el número 42 entre el número 119, el resultado es 0 (cero), lo cual no es correcto.

![Ventana de consola que muestra una aplicación Calculator que no devuelve un número con decimales como resultado](./media/csharp-console-calculator-nodecimal.png)

Vamos a corregir el código de forma que dé cabida a los decimales.

1. Cambie cada instancia de la variable `int` por `float`.

   (Puede usar el control [Buscar y reemplazar](../../ide/finding-and-replacing-text.md#find-and-replace-control) para ayudarle en esta tarea. Para acceder al control de búsqueda en el editor de código, presione **Ctrl**+**F**. Tras ello, seleccione el botón **Buscar siguiente** o el botón **Buscar anterior** en el control de búsqueda. Para acceder a las opciones de reemplazo, seleccione el botón junto al cuadro de texto **Buscar**. Para realizar un reemplazo puntual, pulse el botón **Reemplazar siguiente** junto al cuadro de texto **Reemplazar**. Para reemplazar todas las coincidencias, seleccione el botón **Reemplazar todo**).

1. Vuelva a ejecutar la aplicación Calculator y divida el número **42** entre el número **119**.

   Fíjese en que ahora la aplicación devuelve un número con decimales en lugar de cero.

    ![Ventana de consola que muestra una aplicación Calculator que ahora devuelve un número con decimales como resultado](./media/csharp-console-calculator-decimal.png)

Sin embargo, la aplicación genera solo un resultado decimal. Vamos a hacer algunos retoques más en el código para que la aplicación calcule decimales también.

1. Cambie cada instancia de la variable `float` por `double`.

1. Cambie cada instancia del método `Convert.ToInt32` por `Convert.ToDouble`.

1. Ejecute la aplicación Calculator y divida el número **42.5** entre el número **119.75**.

   Fíjese en que ahora la aplicación acepta valores decimales y devuelve un número decimal más largo como resultado.

    ![Ventana de consola que muestra una aplicación Calculator que ahora acepta valores decimales y devuelve un número decimal más largo como resultado](./media/csharp-console-calculator-usedecimals.png)

    (Corregiremos el número de posiciones decimales en la sección [Revisar el código](#revise-the-code)).

## <a name="debug-the-app"></a>Depurar la aplicación

Hemos mejorado nuestra aplicación de calculadora básica, pero todavía carece de notificaciones de error que permitan controlar excepciones, como los errores que los usuarios cometen al escribir.

Por ejemplo, si intentamos dividir un número entre cero o introducir un carácter alfanumérico cuando la aplicación espera un carácter numérico (o viceversa), la aplicación deja de funcionar y devuelve un error.

Vamos a ver algunos errores comunes de entradas de usuario, a localizarlos en el [depurador](../../debugger/debugger-feature-tour.md)y a corregirlos en el código.

### <a name="fix-the-divide-by-zero-error"></a>Corregir el error "división entre cero"

Cuando intentamos dividir un número entre cero, la aplicación de consola se congela. Luego, Visual Studio señala qué es incorrecto en el editor de código.

   ![Editor de código de Visual Studio que muestra el error de división entre cero](./media/csharp-console-calculator-dividebyzero-error.png)

Vamos a cambiar el código para controlar este error.

1. Elimine el código que aparece directamente entre `case "d":` y el comentario `// Wait for the user to respond before closing`.

1. Reemplácelo por el código siguiente:

   ```csharp
            // Ask the user to enter a non-zero divisor until they do so
                while (num2 == 0)
                {
                    Console.WriteLine("Enter a non-zero divisor: ");
                    num2 = Convert.ToInt32(Console.ReadLine());
                }
                Console.WriteLine($"Your result: {num1} / {num2} = " + (num1 / num2));
                break;
        }
    ```

   Después de agregar el código, la sección con la instrucción `switch` debe ser similar a la de la siguiente captura de pantalla:

   ![Sección "switch" revisada en el editor de código de Visual Studio](./media/csharp-console-calculator-switch-code.png)

Ahora, cuando dividimos un número entre cero, la aplicación nos pedirá otro número. Mejor aún: no parará de pedirlo hasta que proporcionemos un número distinto de cero.

   ![Editor de código de Visual Studio que muestra el error de división entre cero](./media/csharp-console-calculator-dividebyzero.png)

### <a name="fix-the-format-error"></a>Corregir el error de "formato"

Si introduce un carácter alfanumérico cuando la aplicación espera un carácter numérico (o viceversa), la aplicación de consola se congela. Luego, Visual Studio señala qué es incorrecto en el editor de código.

   ![Editor de código de Visual Studio que muestra un error de formato](./media/csharp-console-calculator-format-error.png)

Para corregir este error, debemos refactorizar el código que hemos escrito anteriormente.

#### <a name="revise-the-code"></a>Revisar el código

En lugar de usar la clase `program` para controlar todo el código, dividiremos nuestra aplicación en dos clases: `calculator` y `program`.  

La clase `calculator` controlará la mayor parte del trabajo de cálculo, mientras que la clase `program` controlará la interfaz de usuario y el trabajo de captura de errores.

Comencemos.

1. Elimine todo el contenido que hay *después* del siguiente bloque de código:

    ```csharp

    using System;

    namespace Calculator
    {

    ```

1. Después, agregue una nueva clase `calculator`, como se indica a continuación:

    ```csharp
    class Calculator
    {
        public static double DoOperation(double num1, double num2, string op)
        {
            double result = double.NaN; // Default value is "not-a-number" which we use if an operation, such as division, could result in an error

            // Use a switch statement to do the math
            switch (op)
            {
                case "a":
                    result = num1 + num2;
                    break;
                case "s":
                    result = num1 - num2;
                    break;
                case "m":
                    result = num1 * num2;
                    break;
                case "d":
                    // Ask the user to enter a non-zero divisor
                    if (num2 != 0)
                    {
                        result = num1 / num2;
                    }
                    break;
                // Return text for an incorrect option entry
                default:
                    break;
            }
            return result;
        }
    }

    ```

1. Luego, agregue una nueva clase `program`, como se indica a continuación:

    ```csharp
    class Program
    {
        static void Main(string[] args)
        {
            bool endApp = false;
            // Display title as the C# console calculator app
            Console.WriteLine("Console Calculator in C#\r");
            Console.WriteLine("------------------------\n");

            while (!endApp)
            {
                // Declare variables and set to empty
                string numInput1 = "";
                string numInput2 = "";
                double result = 0;

                // Ask the user to type the first number
                Console.Write("Type a number, and then press Enter: ");
                numInput1 = Console.ReadLine();

                double cleanNum1 = 0;
                while (!double.TryParse(numInput1, out cleanNum1))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput1 = Console.ReadLine();
                }

                // Ask the user to type the second number
                Console.Write("Type another number, and then press Enter: ");
                numInput2 = Console.ReadLine();

                double cleanNum2 = 0;
                while (!double.TryParse(numInput2, out cleanNum2))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput2 = Console.ReadLine();
                }

                // Ask the user to choose an operator
                Console.WriteLine("Choose an operator from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                string op = Console.ReadLine();

                try
                {
                    result = Calculator.DoOperation(cleanNum1, cleanNum2, op);
                    if (double.IsNaN(result))
                    {
                        Console.WriteLine("This operation will result in a mathematical error.\n");
                    }
                    else Console.WriteLine("Your result: {0:0.##}\n", result);
                }
                catch (Exception e)
                {
                    Console.WriteLine("Oh no! An exception occurred trying to do the math.\n - Details: " + e.Message);
                }

                Console.WriteLine("------------------------\n");

                // Wait for the user to respond before closing
                Console.Write("Press 'n' and Enter to close the app, or press any other key and Enter to continue: ");
                if (Console.ReadLine() == "n") endApp = true;

                Console.WriteLine("\n"); // Friendly linespacing
            }
            return;
        }
    }
    ```
1. Elija **Calculator** para ejecutar el programa, o bien presione **F5**.

1. Siga las indicaciones y divida el número **42** entre el número **119**. La aplicación debe ser similar a la siguiente:

    ![Ventana de consola en la que se muestra la aplicación Calculator refactorizada, que incluye mensajes sobre las acciones que se deben realizar y control de errores de entrada incorrecta](./media/csharp-console-calculator-refactored.png)

    Fíjese en que tiene la opción de especificar más ecuaciones hasta que decida cerrar la aplicación de consola. También hemos reducido el número de posiciones decimales en el resultado.

## <a name="close-the-app"></a>Cierre la aplicación

1. Si aún no lo ha hecho, cierre la aplicación de calculadora.

1. Cierre el panel **Salida** en Visual Studio.

   ![Cierre del panel Salida en Visual Studio](./media/csharp-calculator-close-output-pane.png)

1. En Visual Studio, presione **Ctrl**+**G** para guardar la aplicación.

1. Cierre Visual Studio.

## <a name="code-complete"></a>Código completo

Durante este tutorial, hemos realizado muchos cambios en la aplicación de calculadora. Ahora la aplicación controla los recursos de cálculo más eficazmente y trata la mayoría de los errores de entrada de usuario.

Este es el código completo:

```csharp

using System;

namespace Calculator
{
    class Calculator
    {
        public static double DoOperation(double num1, double num2, string op)
        {
            double result = double.NaN; // Default value is "not-a-number" which we use if an operation, such as division, could result in an error

            // Use a switch statement to do the math
            switch (op)
            {
                case "a":
                    result = num1 + num2;
                    break;
                case "s":
                    result = num1 - num2;
                    break;
                case "m":
                    result = num1 * num2;
                    break;
                case "d":
                    // Ask the user to enter a non-zero divisor
                    if (num2 != 0)
                    {
                        result = num1 / num2;
                    }
                    break;
                // Return text for an incorrect option entry
                default:
                    break;
            }
            return result;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            bool endApp = false;
            // Display title as the C# console calculator app
            Console.WriteLine("Console Calculator in C#\r");
            Console.WriteLine("------------------------\n");

            while (!endApp)
            {
                // Declare variables and set to empty
                string numInput1 = "";
                string numInput2 = "";
                double result = 0;

                // Ask the user to type the first number
                Console.Write("Type a number, and then press Enter: ");
                numInput1 = Console.ReadLine();

                double cleanNum1 = 0;
                while (!double.TryParse(numInput1, out cleanNum1))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput1 = Console.ReadLine();
                }

                // Ask the user to type the second number
                Console.Write("Type another number, and then press Enter: ");
                numInput2 = Console.ReadLine();

                double cleanNum2 = 0;
                while (!double.TryParse(numInput2, out cleanNum2))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput2 = Console.ReadLine();
                }

                // Ask the user to choose an operator
                Console.WriteLine("Choose an operator from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                string op = Console.ReadLine();

                try
                {
                    result = Calculator.DoOperation(cleanNum1, cleanNum2, op);
                    if (double.IsNaN(result))
                    {
                        Console.WriteLine("This operation will result in a mathematical error.\n");
                    }
                    else Console.WriteLine("Your result: {0:0.##}\n", result);
                }
                catch (Exception e)
                {
                    Console.WriteLine("Oh no! An exception occurred trying to do the math.\n - Details: " + e.Message);
                }

                Console.WriteLine("------------------------\n");

                // Wait for the user to respond before closing
                Console.Write("Press 'n' and Enter to close the app, or press any other key and Enter to continue: ");
                if (Console.ReadLine() == "n") endApp = true;

                Console.WriteLine("\n"); // Friendly linespacing
            }
            return;
        }
    }
}

```

## <a name="quick-answers-faq"></a>Respuestas rápidas a preguntas frecuentes

Esta es una sección rápida de P+F para destacar algunos conceptos clave. Las preguntas frecuentes también incluyen respuestas a preguntas que pueden surgir al realizar los procedimientos del tutorial.

### <a name="what-is-c"></a>¿Qué es C#?

C# es un lenguaje de programación con seguridad de tipos que se ejecuta en .NET Framework y .NET Core. Con C#, puede crear aplicaciones Windows, aplicaciones cliente-servidor, aplicaciones de base de datos, servicios web XML, componentes distribuidos, etc.

### <a name="what-is-visual-studio"></a>¿Qué es Visual Studio?

Visual Studio es un conjunto de desarrollo integrado de herramientas de productividad para desarrolladores. Considérelo como un programa que se puede usar para crear programas y aplicaciones.

### <a name="what-is-a-console-app"></a>¿Qué es una aplicación de consola?

Una aplicación de consola toma la entrada y muestra la salida en una ventana de línea de comandos, también conocida como consola.

### <a name="what-is-net-core"></a>¿Qué es .NET Core?

.NET core es el siguiente paso evolutivo de .NET Framework. Donde .NET Framework permitía compartir código entre lenguajes de programación, .NET Core agrega la capacidad de compartir código entre plataformas. Y todavía mejor, es de código abierto.

(Tanto .NET Framework como .NET Core incluyen bibliotecas de funcionalidad creada previamente. También incluyen un Common Language Runtime (CLR), que actúa como una máquina virtual en la que se va a ejecutar el código).

### <a id="workload"></a>¿Qué es una carga de trabajo y cómo puedo agregar una?

Una carga de trabajo en Visual Studio es un conjunto de plantillas y opciones de programación que sirven para personalizar la instalación de Visual Studio. Una carga de trabajo instala únicamente las herramientas necesarias según el lenguaje de programación y la plataforma que hayamos elegido. Aquí explicamos cómo instalarlas.

#### <a name="option-1-use-the-new-project-dialog-box"></a>Opción 1: Uso del cuadro de diálogo Nuevo proyecto

1. Elija el vínculo **Abrir el Instalador de Visual Studio** en el panel de la izquierda del cuadro de diálogo **Nuevo proyecto**.

   ![Elija el vínculo Abrir el Instalador de Visual Studio del cuadro de diálogo Nuevo proyecto](./media/csharp-open-visual-studio-installer-generic-dark.png)

1. Se iniciará el Instalador de Visual Studio. Elija la carga de trabajo **Desarrollo multiplataforma de .NET Core** y, después, elija **Modificar**.

   ![Carga de trabajo Desarrollo multiplataforma de .NET Core en el instalador de Visual Studio](./media/dot-net-core-xplat-dev-workload.png)

#### <a name="option-2-use-the-tools-menu-bar"></a>Opción 2: Uso de la barra del menú Herramientas

1. Cancele para salir del cuadro de diálogo **Nuevo proyecto** y, en la barra de menús superior, seleccione **Herramientas** > **Obtener herramientas y características...**.

1. Se iniciará el Instalador de Visual Studio. Elija la carga de trabajo **Desarrollo multiplataforma de .NET Core** y, después, elija **Modificar**.

## <a name="next-steps"></a>Pasos siguientes

Enhorabuena por completar este tutorial. Para más información, continúe con los tutoriales siguientes.

> [!div class="nextstepaction"]
> [Tutoriales de C#](/dotnet/csharp/tutorials/)

## <a name="see-also"></a>Vea también

* [Curso en vídeo de aspectos básicos de C# para principiantes sin experiencia](https://mva.microsoft.com/en-us/training-courses/c-fundamentals-for-absolute-beginners-16169)