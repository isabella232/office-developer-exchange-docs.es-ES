---
title: Validar la integridad de copia de seguridad mediante la herramienta Eseutil en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: Descubra cómo usar la herramienta de línea de comandos Eseutil para validar una copia de seguridad del almacén Exchange comandos.
ms.openlocfilehash: 0ac994201d1f6c711e5d4d0a3d5835f9bac6e041
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516226"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>Validar la integridad de copia de seguridad mediante la herramienta Eseutil en Exchange 2013

Descubra cómo usar la herramienta de línea de comandos Eseutil para validar una copia de seguridad del almacén Exchange comandos. 
  
**Se aplica a:** Exchange Server 2013 
  
Dado que el Servicio de instantáneas de volumen (VSS) puede crear copias de seguridad mientras Exchange continúa escribiendo en la base de datos, el servidor no toca todas las páginas y realiza las comprobaciones de coherencia necesarias. Por este motivo, cualquier aplicación de copia de seguridad y restauración que use VSS debe comprobar la coherencia de la instantánea. Exchange Server 2013 admite los dos métodos siguientes para comprobar la coherencia de instantáneas: 
  
- LA API CHKSGFILES
    
- La herramienta de línea de comandos Eseutil
    
Se recomienda usar la API CHKSGFILES porque es más fácil que la aplicación de copia de seguridad detecte, diagnostique e informe los errores que se encuentran durante la comprobación de coherencia de CHKSGFILES. Para obtener información sobre cómo usar la API CHKSGFILES, vea [Validate backup integrity by using the CHKSGFILES API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).
  
## <a name="running-the-eseutil-tool"></a>Ejecución de la herramienta Eseutil

Para comprobar la coherencia de la instantánea, ejecute el comando eseutil en la base de datos y los archivos de registro que se identifican en la tabla siguiente. 
  
**Tabla 1. Eseutil.exe comandos para cada tipo de copia de seguridad**

|**Tipo de archivo/tipo de copia de seguridad**|**Copia de seguridad completa**|**Copia de seguridad**|**Copia de seguridad incremental**|**Copia de seguridad diferencial**|
|:-----|:-----|:-----|:-----|:-----|
|.edb  <br/> |"eseutil /k /i"  <br/> |"eseutil /k /i"  <br/> |No aplicable  <br/> |No aplicable  <br/> |
|.log  <br/> |"eseutil /k" (1)  <br/> |"eseutil /k" (1)  <br/> |"eseutil /k" (2)  <br/> |"eseutil /k" (2)  <br/> |
   
> [!NOTE]
> No es necesario ejecutar el comando eseutil en los archivos .stm y .chk. 
  
Todos los archivos de registro que tienen un número de generación de archivos de registro igual o mayor que el número de generación del archivo de registro de punto de control son necesarios para recuperar una base de datos de instantáneas. Si existe, el archivo de registro actual (Enn.log) también es necesario para la recuperación de la base de datos. Si alguno de los archivos de registro necesarios no cumple la comprobación de coherencia, el solicitante debe asegurarse de que el estado del componente de copia de seguridad esté establecido en FALSE antes de llamar al [método BackupComplete.](https://msdn.microsoft.com/library/windows/desktop/aa382651%28v=vs.85%29.aspx) Para identificar el archivo de registro de punto de control, ejecute Eseutil.exe con el archivo de punto de control de instantánea y analice el resultado de "Checkpoint:". En el ejemplo siguiente se muestra cómo ejecutar Eseutil.exe un archivo de punto de control. 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

La segunda línea del ejemplo es el valor devuelto, donde 0x20 es el número de generación de registro hexadecimal del archivo de registro de punto de control. En este ejemplo, los archivos de registro, incluidos E01000020.log y superiores, no deben estar dañados para recuperar la base de datos de instantáneas, incluso si la propia base de datos ya ha pasado la comprobación de coherencia física.
  
Todos los archivos de registro de un conjunto de copia de seguridad incremental o diferencial son necesarios para la recuperación de la base de datos. Puede comprobar la coherencia de una secuencia de registro ejecutando Eseutil.exe con el prefijo de archivo de registro. En el ejemplo siguiente se muestra cómo ejecutar comprobaciones de coherencia en todos los archivos del formulario E01xxxxx.log en una ruta de acceso determinada.
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>Comprobación de la Eseutil.exe salida

El solicitante debe comprobar que todos los valores de error errorLEVEL de salida que se devuelven no son negativos. Para obtener información acerca de los valores ERRORLEVEL, vea [Reference for Common Eseutil Errors](https://technet.microsoft.com/library/aa996759%28v=exchg.80%29.aspx). Para ver ERRORLEVEL en la línea de comandos, escriba "echo %errorlevel%" después de Eseutil.exe finaliza la ejecución. Un ERRORLEVEL negativo indica que uno o varios archivos están dañados.
  
Antes de que el solicitante llame al **método BackupComplete,** debe asegurarse de que el estado del componente de copia de seguridad refleje el resultado de la comprobación de coherencia. Si se encontró algún daño, el estado será FALSE; si no se encontró ningún daño, el estado será TRUE. 
  
## <a name="see-also"></a>Ver también

- [Validar la integridad de copia de seguridad mediante la API CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [Crear aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Referencia de la clase CChkSGFiles](cchksgfiles-class-reference.md)
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

