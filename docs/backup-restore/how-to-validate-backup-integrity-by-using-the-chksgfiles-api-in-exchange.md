---
title: Validar la integridad de la copia de seguridad mediante el uso de la API CHKSGFILES en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: Descubra cómo usar la API CHKSGFILES para validar una copia de seguridad del almacén de Exchange en Exchange 2013.
ms.openlocfilehash: 968484cd5bb7439730685643683e1d850bec33ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762981"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>Validar la integridad de la copia de seguridad mediante el uso de la API CHKSGFILES en Exchange 2013

Descubra cómo usar la API CHKSGFILES para validar una copia de seguridad del almacén de Exchange en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
Durante las operaciones de copia de seguridad administradas por el servicio de copia de instantáneas de volumen (VSS), Exchange Server 2013 no se puede leer cada archivo de base de datos en su totalidad y comprobar su integridad de la suma de comprobación. Por lo tanto, es posible que desea que la aplicación de copia de seguridad para comprobar la integridad de archivos de registro de transacciones y de base de datos. Se recomienda que la aplicación de copia de seguridad comprobar la coherencia física del conjunto de copia sombra antes de que se informa al escritor de Exchange que la copia de seguridad está completa. Después de una copia de seguridad correcta, el almacén de Exchange actualiza los encabezados de las bases de datos de copia de seguridad que refleje que agote el tiempo de la última copia de seguridad correcta y quita los registros de transacciones desde el servidor que ya no son necesarios para desplazar hacia delante desde la última copia de seguridad correcta.
  
## <a name="prerequisites-for-validating-backup-integrity"></a>Requisitos previos para validar la integridad de la copia de seguridad

Antes de la aplicación puede validar la integridad de la copia de seguridad, debe tener acceso a lo siguiente:
  
- Archivos de la copia de seguridad del almacén de Exchange.
- Una versión de Visual Studio desde Visual Studio 2010.
- Los archivos de encabezado y de biblioteca CHKSGFILES. Puede descargar los archivos de encabezado y de biblioteca desde el [Centro de descarga de Microsoft](http://www.microsoft.com/en-us/download/details.aspx?id=36802).
    
## <a name="validate-backup-integrity"></a>Validar la integridad de la copia de seguridad

El siguiente procedimiento describe cómo validar la integridad de los datos en la copia de seguridad y restauración de la aplicación.
  
### <a name="to-validate-backup-integrity"></a>Para validar la integridad de la copia de seguridad

1. Crear una nueva instancia de la clase **CChkSGFiles** . 
   
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

   Las primeras líneas de código creación un objeto error y establezca su valor inicial para el éxito y creación un objeto que se comprueba la validez de la base de datos. A continuación, la [función CChkSGFiles.New](cchksgfiles-new-function.md) crea una nueva instancia de la clase **CChkSGFiles** . Una comprobación rápida del nuevo objeto indica si se ha producido cualquier problema cuando se creó la nueva instancia. 
    
2. Inicializar el objeto **CChkSGFiles** . 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   Para obtener más información acerca de los parámetros, vea la [función CChkSGFiles.ErrInit](cchksgfiles-errinit-function.md).
   
3. Use la [función CChkSGFiles.ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md) para validar la integridad de la base de datos mediante la comprobación de los encabezados de la base de datos.
   
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
   
   Para obtener más información acerca de los parámetros, vea la [función CChkSGFiles.ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md).
   
4. Controlar los errores y use la [función CChkSGFiles.Delete](cchksgfiles-delete-function.md) para quitar la clase **CChkSGFiles** de la memoria. 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>Ver también

- [Referencia de clase CChkSGFiles](cchksgfiles-class-reference.md)
- [Crear copia de seguridad y restauración de aplicaciones para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

