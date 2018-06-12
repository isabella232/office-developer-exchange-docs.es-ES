---
title: Validar la integridad de la copia de seguridad mediante la herramienta Eseutil en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: Encuentre información acerca de cómo usar la herramienta de línea de comandos de Eseutil para validar una copia de seguridad del almacén de Exchange.
ms.openlocfilehash: 03c4c23d433418911240bbe7c337308a989f3739
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762973"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>Validar la integridad de la copia de seguridad mediante la herramienta Eseutil en Exchange 2013

Encuentre información acerca de cómo usar la herramienta de línea de comandos de Eseutil para validar una copia de seguridad del almacén de Exchange. 
  
**Se aplica a:** Exchange Server 2013 
  
Debido a que el servicio de instantáneas de volumen (VSS) para poder crear las copias de seguridad mientras Exchange continúa escribir en la base de datos, el servidor no toque todas las páginas y realizar las comprobaciones de coherencia es necesario. Por este motivo, cualquier aplicación de copia de seguridad y restauración que usa VSS debe comprobar la coherencia de la instantánea. Exchange Server 2013 es compatible con los dos métodos siguientes para comprobar la coherencia de instantánea: 
  
- La API CHKSGFILES
    
- La herramienta de línea de comandos de Eseutil
    
Se recomienda usar la API CHKSGFILES porque es más fácil para la aplicación de copia de seguridad detectar, diagnosticar y comprobar el informe de errores que se encuentra durante la coherencia CHKSGFILES. Para obtener información acerca de cómo usar la API CHKSGFILES, vea [Validar integridad de la copia de seguridad mediante el uso de la API CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).
  
## <a name="running-the-eseutil-tool"></a>Ejecutar la herramienta Eseutil

Para comprobar la coherencia de instantáneas, ejecute el comando eseutil contra la base de datos y archivos de registro que se identifican en la tabla siguiente. 
  
**La tabla 1. Comandos de Eseutil.exe para cada tipo de copia de seguridad**

|**Tipo de copia de seguridad o tipo de archivo**|**Copia de seguridad completa**|**Copia de seguridad**|**Copia de seguridad incremental**|**Copia de seguridad diferencial**|
|:-----|:-----|:-----|:-----|:-----|
|.edb  <br/> |"eseutil/k /i"  <br/> |"eseutil/k /i"  <br/> |No disponible  <br/> |No disponible  <br/> |
|.log  <br/> |"eseutil/k" (1)  <br/> |"eseutil/k" (1)  <br/> |"eseutil/k" (2)  <br/> |"eseutil/k" (2)  <br/> |
   
> [!NOTE]
> No es necesario ejecutar el comando eseutil en archivos stm y .chk. 
  
Todos los archivos de registro que tienen una generación del archivo de registro de número que es igual o mayor que la generación número el punto de comprobación del archivo de registro son necesarios para recuperar una base de datos de la instantánea. Si existe, el archivo de registro actual (Enn.log del) también se requiere para la recuperación de la base de datos. Si cualquiera de los archivos de registro necesarios producirá un error en la comprobación de coherencia, el solicitante debe asegurarse de que el estado del componente de copia de seguridad se establece en FALSE antes de llamar al método [BackupComplete](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382651%28v=vs.85%29.aspx) . Para identificar el archivo de registro de punto de control, ejecute Eseutil.exe en el archivo de punto de comprobación de instantánea y analizar el resultado para "punto de comprobación:." En el ejemplo siguiente se muestra cómo ejecutar Eseutil.exe en un archivo de punto de control. 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

La segunda línea en el ejemplo es el valor devuelto, donde 0 x 20 es el número de generación de registro hexadecimal el punto de comprobación del archivo de registro. En este ejemplo, cualquiera archivos de registro, incluidos E01000020.log y mayor, deben no estar dañado con el fin de recuperar la base de datos de la instantánea, incluso si la base de datos ya ha pasado la comprobación de coherencia física.
  
Todos los archivos de registro en un conjunto de copia de seguridad diferencial o incremental son necesarios para la recuperación de la base de datos. Puede comprobar la coherencia de una secuencia de registro mediante la ejecución de Eseutil.exe contra el prefijo del archivo de registro. En el ejemplo siguiente se muestra cómo ejecutar comprobaciones de coherencia en todos los archivos del formulario E01xxxxx.log en una ruta de acceso determinada.
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>Comprobación de la salida de Eseutil.exe

El solicitante debe comprobar que todos los valores de error ERRORLEVEL salir que se devuelven son no negativos. Para obtener información acerca de los valores ERRORLEVEL, vea [referencia de los errores comunes de Eseutil](http://technet.microsoft.com/en-us/library/aa996759%28v=exchg.80%29.aspx). Para ver el ERRORLEVEL en la línea de comandos, escriba "echo % errorlevel %" Cuando Eseutil.exe termine de ejecutarse. Un ERRORLEVEL negativo indica que uno o varios archivos está dañado.
  
Antes de que el solicitante llama al método de **BackupComplete** , debe asegurarse de que el estado del componente de copia de seguridad refleja el resultado de la comprobación de coherencia. Si se encuentra cualquier daño, el estado será FALSE; Si no se encuentran daños, el estado será TRUE. 
  
## <a name="see-also"></a>Ver también

- [Validar la integridad de la copia de seguridad mediante el uso de la API CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [Crear copia de seguridad y restauración de aplicaciones para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Referencia de clase CChkSGFiles](cchksgfiles-class-reference.md)
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

