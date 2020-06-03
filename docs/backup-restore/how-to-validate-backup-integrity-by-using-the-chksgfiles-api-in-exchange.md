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
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a><span data-ttu-id="293c3-103">Validar la integridad de la copia de seguridad mediante la API de CHKSGFILES en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="293c3-103">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>

<span data-ttu-id="293c3-104">Descubra cómo usar la API CHKSGFILES para validar una copia de seguridad del almacén de Exchange en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="293c3-104">Find out how to use the CHKSGFILES API to validate a backup of the Exchange store in Exchange 2013.</span></span>
  
<span data-ttu-id="293c3-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="293c3-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="293c3-106">Durante las operaciones de copia de seguridad administradas por el servicio de instantáneas de volumen (VSS), Exchange Server 2013 no puede leer cada archivo de base de datos en su totalidad y comprobar su integridad de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="293c3-106">During backup operations managed by the Volume Shadow Copy Service (VSS), Exchange Server 2013 cannot read each database file in its entirety and verify its checksum integrity.</span></span> <span data-ttu-id="293c3-107">Por lo tanto, es posible que desee que la aplicación de copia de seguridad Compruebe la integridad del archivo de registro de transacciones y bases de datos.</span><span class="sxs-lookup"><span data-stu-id="293c3-107">Therefore, you might want your backup application to verify database and transaction log file integrity.</span></span> <span data-ttu-id="293c3-108">Se recomienda que la aplicación de copia de seguridad Compruebe la coherencia física del conjunto de instantáneas antes de informar al escritor de Exchange de que se ha completado la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="293c3-108">We recommend that your backup application verify the physical consistency of the shadow copy set prior to informing the Exchange writer that the backup is complete.</span></span> <span data-ttu-id="293c3-109">Después de una copia de seguridad correcta, el almacén de Exchange actualiza los encabezados de las bases de datos de copia de seguridad para reflejar los últimos tiempos de copia de seguridad correcta y quita los registros de transacciones del servidor que ya no son necesarios para revertir desde la última copia de seguridad correcta.</span><span class="sxs-lookup"><span data-stu-id="293c3-109">After a successful backup, the Exchange store updates the headers of the backed-up databases to reflect the last successful backup times and removes transaction logs from the server that are no longer required to roll forward from the last successful backup.</span></span>
  
## <a name="prerequisites-for-validating-backup-integrity"></a><span data-ttu-id="293c3-110">Requisitos previos para validar la integridad de la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="293c3-110">Prerequisites for validating backup integrity</span></span>

<span data-ttu-id="293c3-111">Para que la aplicación pueda validar la integridad de la copia de seguridad, debe tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="293c3-111">Before your application can validate the integrity of your backup, you must have access to the following:</span></span>
  
- <span data-ttu-id="293c3-112">Archivos de la copia de seguridad del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="293c3-112">Files from your Exchange store backup.</span></span>
- <span data-ttu-id="293c3-113">Una versión de Visual Studio a partir de Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="293c3-113">A version of Visual Studio starting with Visual Studio 2010.</span></span>
- <span data-ttu-id="293c3-114">La biblioteca CHKSGFILES y los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="293c3-114">The CHKSGFILES library and header files.</span></span> <span data-ttu-id="293c3-115">Puede descargar los archivos de la biblioteca y los encabezados desde el [centro de descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=36802).</span><span class="sxs-lookup"><span data-stu-id="293c3-115">You can download the library and header files from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802).</span></span>
    
## <a name="validate-backup-integrity"></a><span data-ttu-id="293c3-116">Validar la integridad de la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="293c3-116">Validate backup integrity</span></span>

<span data-ttu-id="293c3-117">El siguiente procedimiento describe cómo validar la integridad de los datos en la aplicación de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="293c3-117">The following procedure describes how to validate data integrity in your backup and restore application.</span></span>
  
### <a name="to-validate-backup-integrity"></a><span data-ttu-id="293c3-118">Para validar la integridad de la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="293c3-118">To validate backup integrity</span></span>

1. <span data-ttu-id="293c3-119">Cree una nueva instancia de la clase **función cchksgfiles** .</span><span class="sxs-lookup"><span data-stu-id="293c3-119">Create a new instance of the **CChkSGFiles** class.</span></span> 
   
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

   <span data-ttu-id="293c3-120">En las primeras líneas de código se crea un objeto error y se establece su valor inicial en correcto, y se crea un objeto que comprueba la validez de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="293c3-120">The first lines of code create an error object and set its initial value to success, and create an object that checks the validity of the database.</span></span> <span data-ttu-id="293c3-121">A continuación, la [función función cchksgfiles. New](cchksgfiles-new-function.md) crea una nueva instancia de la clase **función cchksgfiles**</span><span class="sxs-lookup"><span data-stu-id="293c3-121">Then, the [CChkSGFiles.New function](cchksgfiles-new-function.md) creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="293c3-122">Una comprobación rápida del nuevo objeto indica si se produjeron problemas al crear la nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="293c3-122">A quick check of the new object indicates whether any issues occurred when the new instance was created.</span></span> 
    
2. <span data-ttu-id="293c3-123">Inicialice el objeto **función cchksgfiles** .</span><span class="sxs-lookup"><span data-stu-id="293c3-123">Initialize the **CChkSGFiles** object.</span></span> 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   <span data-ttu-id="293c3-124">Para obtener más información acerca de los parámetros, consulte [función función cchksgfiles. ErrInit](cchksgfiles-errinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="293c3-124">For more information about the parameters, see [CChkSGFiles.ErrInit function](cchksgfiles-errinit-function.md).</span></span>
   
3. <span data-ttu-id="293c3-125">Use la [función función cchksgfiles. ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md) para validar la integridad de la base de datos comprobando los encabezados de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="293c3-125">Use the [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md) to validate database integrity by checking the database headers.</span></span>
   
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
   
   <span data-ttu-id="293c3-126">Para obtener más información acerca de los parámetros, consulte [función función cchksgfiles. ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md).</span><span class="sxs-lookup"><span data-stu-id="293c3-126">For more information about the parameters, see [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md).</span></span>
   
4. <span data-ttu-id="293c3-127">Controle los errores y use la [función función cchksgfiles. Delete](cchksgfiles-delete-function.md) para quitar la clase **función cchksgfiles** de la memoria.</span><span class="sxs-lookup"><span data-stu-id="293c3-127">Handle errors, and use the [CChkSGFiles.Delete function](cchksgfiles-delete-function.md) to remove the **CChkSGFiles** class from memory.</span></span> 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a><span data-ttu-id="293c3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="293c3-128">See also</span></span>

- [<span data-ttu-id="293c3-129">Referencia de clase función cchksgfiles</span><span class="sxs-lookup"><span data-stu-id="293c3-129">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md)
- [<span data-ttu-id="293c3-130">Creación de aplicaciones de copia de seguridad y restauración para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="293c3-130">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
- [<span data-ttu-id="293c3-131">Conceptos de copia de seguridad y restauración para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="293c3-131">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    

