---
title: Validar la integridad de la copia de seguridad mediante la API de CHKSGFILES en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: Descubra cómo usar la API CHKSGFILES para validar una copia de seguridad del almacén de Exchange en Exchange 2013.
ms.openlocfilehash: c101413793cf3b952d3db3e0f792c8bcf2dd9fc9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452863"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>Validar la integridad de la copia de seguridad mediante la API de CHKSGFILES en Exchange 2013

Descubra cómo usar la API CHKSGFILES para validar una copia de seguridad del almacén de Exchange en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
Durante las operaciones de copia de seguridad administradas por el servicio de instantáneas de volumen (VSS), Exchange Server 2013 no puede leer cada archivo de base de datos en su totalidad y comprobar su integridad de suma de comprobación. Por lo tanto, es posible que desee que la aplicación de copia de seguridad Compruebe la integridad del archivo de registro de transacciones y bases de datos. Se recomienda que la aplicación de copia de seguridad Compruebe la coherencia física del conjunto de instantáneas antes de informar al escritor de Exchange de que se ha completado la copia de seguridad. Después de una copia de seguridad correcta, el almacén de Exchange actualiza los encabezados de las bases de datos de copia de seguridad para reflejar los últimos tiempos de copia de seguridad correcta y quita los registros de transacciones del servidor que ya no son necesarios para revertir desde la última copia de seguridad correcta.
  
## <a name="prerequisites-for-validating-backup-integrity"></a>Requisitos previos para validar la integridad de la copia de seguridad

Para que la aplicación pueda validar la integridad de la copia de seguridad, debe tener acceso a lo siguiente:
  
- Archivos de la copia de seguridad del almacén de Exchange.
- Una versión de Visual Studio a partir de Visual Studio 2010.
- La biblioteca CHKSGFILES y los archivos de encabezado. Puede descargar los archivos de la biblioteca y los encabezados desde el [centro de descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=36802).
    
## <a name="validate-backup-integrity"></a>Validar la integridad de la copia de seguridad

El siguiente procedimiento describe cómo validar la integridad de los datos en la aplicación de copia de seguridad y restauración.
  
### <a name="to-validate-backup-integrity"></a>Para validar la integridad de la copia de seguridad

1. Cree una nueva instancia de la clase **función cchksgfiles** . 
   
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

   En las primeras líneas de código se crea un objeto error y se establece su valor inicial en correcto, y se crea un objeto que comprueba la validez de la base de datos. A continuación, la [función función cchksgfiles. New](cchksgfiles-new-function.md) crea una nueva instancia de la clase **función cchksgfiles** Una comprobación rápida del nuevo objeto indica si se produjeron problemas al crear la nueva instancia. 
    
2. Inicialice el objeto **función cchksgfiles** . 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   Para obtener más información acerca de los parámetros, consulte [función función cchksgfiles. ErrInit](cchksgfiles-errinit-function.md).
   
3. Use la [función función cchksgfiles. ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md) para validar la integridad de la base de datos comprobando los encabezados de la base de datos.
   
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
   
   Para obtener más información acerca de los parámetros, consulte [función función cchksgfiles. ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md).
   
4. Controle los errores y use la [función función cchksgfiles. Delete](cchksgfiles-delete-function.md) para quitar la clase **función cchksgfiles** de la memoria. 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>Vea también

- [Referencia de clase función cchksgfiles](cchksgfiles-class-reference.md)
- [Creación de aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

