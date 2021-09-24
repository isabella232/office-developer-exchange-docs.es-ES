---
title: Validar la integridad de copia de seguridad mediante la API CHKSGFILES en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: Descubra cómo usar la API CHKSGFILES para validar una copia de seguridad del Exchange en Exchange 2013.
ms.openlocfilehash: 7a12a0a8f66128970a782da50ba59f41767c60d3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516233"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>Validar la integridad de copia de seguridad mediante la API CHKSGFILES en Exchange 2013

Descubra cómo usar la API CHKSGFILES para validar una copia de seguridad del Exchange en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
Durante las operaciones de copia de seguridad administradas por el Servicio de instantáneas de volumen (VSS), Exchange Server 2013 no puede leer todos los archivos de base de datos en su totalidad y comprobar su integridad de suma de comprobación. Por lo tanto, es posible que desee que la aplicación de copia de seguridad compruebe la integridad de la base de datos y el archivo de registro de transacciones. Se recomienda que la aplicación de copia de seguridad compruebe la coherencia física del conjunto de instantáneas antes de informar al Exchange que la copia de seguridad se ha completado. Después de realizar una copia de seguridad correcta, el almacén de Exchange actualiza los encabezados de las bases de datos de copia de seguridad para reflejar los últimos tiempos de copia de seguridad correctos y quita los registros de transacciones del servidor que ya no son necesarios para avanzar desde la última copia de seguridad correcta.
  
## <a name="prerequisites-for-validating-backup-integrity"></a>Requisitos previos para validar la integridad de copia de seguridad

Para que la aplicación pueda validar la integridad de la copia de seguridad, debe tener acceso a lo siguiente:
  
- Archivos de la copia de seguridad Exchange almacén.
- Una versión de Visual Studio a partir de Visual Studio 2010.
- La biblioteca CHKSGFILES y los archivos de encabezado. Puede descargar los archivos de biblioteca y encabezado desde el [Centro de descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=36802).
    
## <a name="validate-backup-integrity"></a>Validar integridad de copia de seguridad

En el siguiente procedimiento se describe cómo validar la integridad de los datos en la aplicación de copia de seguridad y restauración.
  
### <a name="to-validate-backup-integrity"></a>Para validar la integridad de copia de seguridad

1. Cree una nueva instancia de la **clase CChkSGFiles.** 
   
   ```cpp
   CCheckSGFiles::ERRerr = CCheckSGFiles::errSuccess;
   ULONGiDbError = (ULONG)CCheckSGFiles::iDbInvalid;
   CCheckSGFiles * const pcchecksgfiles = CCheckSGFiles::New();
   if ( NULL == pcchecksgfiles )
   {
     err = CCheckSGFiles::errOutOfMemory;
     printf( "ERROR: Could not allocate CCheckSGFiles object.\n" );
     goto HandleError;
   }
   ```

   Las primeras líneas de código crean un objeto de error y establecen su valor inicial en correcto y crean un objeto que comprueba la validez de la base de datos. A continuación, la función [CChkSGFiles.New](cchksgfiles-new-function.md) crea una nueva instancia de la **clase CChkSGFiles.** Una comprobación rápida del nuevo objeto indica si se produjeron problemas cuando se creó la nueva instancia. 
    
2. Inicializar **el objeto CChkSGFiles.** 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   Para obtener más información acerca de los parámetros, vea [la función CChkSGFiles.ErrInit](cchksgfiles-errinit-function.md).
   
3. Use la [función CChkSGFiles.ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md) para validar la integridad de la base de datos comprobando los encabezados de la base de datos.
   
   ```cpp
   err = pcchecksgfiles->ErrCheckDbHeaders(
   &amp;cbDbPageSize,
   &amp;cDbHeaderPages,
   &amp;iDbError );
   if ( CCheckSGFiles::errSuccess != err )
   {
   if ( CCheckSGFiles::iDbInvalid != iDbError )
   {
   printf(
   "ERROR: Database header validation for '%S' failed with error %d (0x%x)\n",
   rgwszDb[ iDbError ],
   err,
   err );
   }
   goto HandleError;
   }
   ```
   
   Para obtener más información acerca de los parámetros, vea [la función CChkSGFiles.ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md).
   
4. Controlar errores y usar la función [CChkSGFiles.Delete](cchksgfiles-delete-function.md) para quitar la clase **CChkSGFiles** de la memoria. 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>Ver también

- [Referencia de la clase CChkSGFiles](cchksgfiles-class-reference.md)
- [Crear aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

