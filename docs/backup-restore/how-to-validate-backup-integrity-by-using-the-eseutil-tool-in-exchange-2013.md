---
title: Validar la integridad de la copia de seguridad mediante la herramienta Eseutil en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: Descubra cómo usar la herramienta de línea de comandos ESEUTIL para validar una copia de seguridad del almacén de Exchange.
ms.openlocfilehash: e8f1a46e2d94729ae5586861317312e277216d63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452800"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>Validar la integridad de la copia de seguridad mediante la herramienta Eseutil en Exchange 2013

Descubra cómo usar la herramienta de línea de comandos ESEUTIL para validar una copia de seguridad del almacén de Exchange. 
  
**Se aplica a:** Exchange Server 2013 
  
Debido a que el servicio de instantáneas de volumen (VSS) puede crear copias de seguridad mientras Exchange sigue escribiendo en la base de datos, el servidor no toca todas las páginas y realiza las comprobaciones de coherencia necesarias. Por este motivo, cualquier aplicación de copia de seguridad y restauración que use VSS debe comprobar la coherencia de la instantánea. Exchange Server 2013 admite los siguientes dos métodos para comprobar la coherencia de la instantánea: 
  
- La API de CHKSGFILES
    
- Herramienta de línea de comandos Eseutil
    
Le recomendamos que use la API CHKSGFILES porque es más fácil para la aplicación de copia de seguridad detectar, diagnosticar e informar de los errores que se encuentran durante la comprobación de coherencia CHKSGFILES. Para obtener información sobre cómo usar la API de CHKSGFILES, consulte [validar la integridad de la copia de seguridad mediante la API de CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).
  
## <a name="running-the-eseutil-tool"></a>Ejecutar la herramienta Eseutil

Para comprobar la coherencia de la instantánea, ejecute el comando Eseutil en los archivos de registro y de base de datos que se identifican en la tabla siguiente. 
  
**Tabla 1. Comandos de Eseutil. exe para cada tipo de copia de seguridad**

|**Tipo de archivo/tipo de copia de seguridad**|**Copia de seguridad completa**|**Copia de seguridad**|**Copia de seguridad incremental**|**Copia de seguridad diferencial**|
|:-----|:-----|:-----|:-----|:-----|
|. edb  <br/> |"Eseutil/k/i"  <br/> |"Eseutil/k/i"  <br/> |No aplicable  <br/> |No aplicable  <br/> |
|. log  <br/> |"Eseutil/k" (1)  <br/> |"Eseutil/k" (1)  <br/> |"Eseutil/k" (2)  <br/> |"Eseutil/k" (2)  <br/> |
   
> [!NOTE]
> No es necesario ejecutar el comando Eseutil en los archivos. stm y. chk. 
  
Todos los archivos de registro que tienen un número de generación de archivos de registro que es igual o mayor que el número de generación del archivo de registro de controles es necesario para recuperar una base de datos de instantáneas. Si existe, el archivo de registro actual (enn. log) también es necesario para la recuperación de la base de datos. Si alguno de los archivos de registro necesarios no supera la comprobación de coherencia, el solicitante debe asegurarse de que el estado del componente de copia de seguridad está establecido en FALSE antes de llamar al método [BackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa382651%28v=vs.85%29.aspx) . Para identificar el archivo de registro de punto de control, ejecute Eseutil. exe en el archivo de punto de control de instantánea y analice el resultado de "Checkpoint:". En el ejemplo siguiente se muestra cómo ejecutar Eseutil. exe en un archivo de punto de control. 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

La segunda línea del ejemplo es el valor devuelto, donde 0x20 es el número de generación de registro hexadecimal del archivo de registro de punto de control. En este ejemplo, los archivos de registro, incluidos E01000020. log y versiones posteriores, no deben estar dañados para poder recuperar la base de datos de instantáneas, incluso si la propia base de datos ya ha superado la comprobación de coherencia física.
  
Todos los archivos de registro de un conjunto de copia de seguridad diferencial o incremental son necesarios para la recuperación de la base de datos. Puede comprobar la coherencia de una secuencia de registro ejecutando Eseutil. exe en el prefijo del archivo de registro. En el ejemplo siguiente se muestra cómo ejecutar comprobaciones de coherencia en todos los archivos del formulario E01xxxxx. log en una ruta de acceso determinada.
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>Comprobación del resultado de Eseutil. exe

El solicitante debe comprobar que todos los valores de error ERRORLEVEL de Exit devueltos son no negativos. Para obtener información acerca de los valores de ERRORLEVEL, consulte [Reference for Common Eseutil Errors](https://technet.microsoft.com/library/aa996759%28v=exchg.80%29.aspx). Para ver el ERRORLEVEL en la línea de comandos, escriba "echo% ERRORLEVEL%" después de que Eseutil. exe termine de ejecutarse. Un ERRORLEVEL negativo indica que uno o varios archivos están dañados.
  
Antes de que el solicitante llame al método **BackupComplete** , debe asegurarse de que el estado del componente de copia de seguridad refleje el resultado de la comprobación de coherencia. Si se encuentra algún daño, el estado será FALSE; Si no se ha encontrado ningún daño, el estado será TRUE. 
  
## <a name="see-also"></a>Vea también

- [Validar la integridad de la copia de seguridad mediante la API de CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [Creación de aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Referencia de clase función cchksgfiles](cchksgfiles-class-reference.md)
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

