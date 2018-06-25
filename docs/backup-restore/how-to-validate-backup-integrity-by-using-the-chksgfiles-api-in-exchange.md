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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762981"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a><span data-ttu-id="9c357-103">Validar la integridad de la copia de seguridad mediante el uso de la API CHKSGFILES en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9c357-103">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>

<span data-ttu-id="9c357-104">Descubra cómo usar la API CHKSGFILES para validar una copia de seguridad del almacén de Exchange en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="9c357-104">Find out how to use the CHKSGFILES API to validate a backup of the Exchange store in Exchange 2013.</span></span>
  
<span data-ttu-id="9c357-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c357-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="9c357-106">Durante las operaciones de copia de seguridad administradas por el servicio de copia de instantáneas de volumen (VSS), Exchange Server 2013 no se puede leer cada archivo de base de datos en su totalidad y comprobar su integridad de la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="9c357-106">During backup operations managed by the Volume Shadow Copy Service (VSS), Exchange Server 2013 cannot read each database file in its entirety and verify its checksum integrity.</span></span> <span data-ttu-id="9c357-107">Por lo tanto, es posible que desea que la aplicación de copia de seguridad para comprobar la integridad de archivos de registro de transacciones y de base de datos.</span><span class="sxs-lookup"><span data-stu-id="9c357-107">Therefore, you might want your backup application to verify database and transaction log file integrity.</span></span> <span data-ttu-id="9c357-108">Se recomienda que la aplicación de copia de seguridad comprobar la coherencia física del conjunto de copia sombra antes de que se informa al escritor de Exchange que la copia de seguridad está completa.</span><span class="sxs-lookup"><span data-stu-id="9c357-108">We recommend that your backup application verify the physical consistency of the shadow copy set prior to informing the Exchange writer that the backup is complete.</span></span> <span data-ttu-id="9c357-109">Después de una copia de seguridad correcta, el almacén de Exchange actualiza los encabezados de las bases de datos de copia de seguridad que refleje que agote el tiempo de la última copia de seguridad correcta y quita los registros de transacciones desde el servidor que ya no son necesarios para desplazar hacia delante desde la última copia de seguridad correcta.</span><span class="sxs-lookup"><span data-stu-id="9c357-109">After a successful backup, the Exchange store updates the headers of the backed-up databases to reflect the last successful backup times and removes transaction logs from the server that are no longer required to roll forward from the last successful backup.</span></span>
  
## <a name="prerequisites-for-validating-backup-integrity"></a><span data-ttu-id="9c357-110">Requisitos previos para validar la integridad de la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="9c357-110">Prerequisites for validating backup integrity</span></span>

<span data-ttu-id="9c357-111">Antes de la aplicación puede validar la integridad de la copia de seguridad, debe tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c357-111">Before your application can validate the integrity of your backup, you must have access to the following:</span></span>
  
- <span data-ttu-id="9c357-112">Archivos de la copia de seguridad del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9c357-112">Files from your Exchange store backup.</span></span>
- <span data-ttu-id="9c357-113">Una versión de Visual Studio desde Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="9c357-113">A version of Visual Studio starting with Visual Studio 2010.</span></span>
- <span data-ttu-id="9c357-114">Los archivos de encabezado y de biblioteca CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="9c357-114">The CHKSGFILES library and header files.</span></span> <span data-ttu-id="9c357-115">Puede descargar los archivos de encabezado y de biblioteca desde el [Centro de descarga de Microsoft](http://www.microsoft.com/en-us/download/details.aspx?id=36802).</span><span class="sxs-lookup"><span data-stu-id="9c357-115">You can download the library and header files from the [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802).</span></span>
    
## <a name="validate-backup-integrity"></a><span data-ttu-id="9c357-116">Validar la integridad de la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="9c357-116">Validate backup integrity</span></span>

<span data-ttu-id="9c357-117">El siguiente procedimiento describe cómo validar la integridad de los datos en la copia de seguridad y restauración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c357-117">The following procedure describes how to validate data integrity in your backup and restore application.</span></span>
  
### <a name="to-validate-backup-integrity"></a><span data-ttu-id="9c357-118">Para validar la integridad de la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="9c357-118">To validate backup integrity</span></span>

1. <span data-ttu-id="9c357-119">Crear una nueva instancia de la clase **CChkSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="9c357-119">Create a new instance of the **CChkSGFiles** class.</span></span> 
   
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

   <span data-ttu-id="9c357-120">Las primeras líneas de código creación un objeto error y establezca su valor inicial para el éxito y creación un objeto que se comprueba la validez de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9c357-120">The first lines of code create an error object and set its initial value to success, and create an object that checks the validity of the database.</span></span> <span data-ttu-id="9c357-121">A continuación, la [función CChkSGFiles.New](cchksgfiles-new-function.md) crea una nueva instancia de la clase **CChkSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="9c357-121">Then, the [CChkSGFiles.New function](cchksgfiles-new-function.md) creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="9c357-122">Una comprobación rápida del nuevo objeto indica si se ha producido cualquier problema cuando se creó la nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="9c357-122">A quick check of the new object indicates whether any issues occurred when the new instance was created.</span></span> 
    
2. <span data-ttu-id="9c357-123">Inicializar el objeto **CChkSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="9c357-123">Initialize the **CChkSGFiles** object.</span></span> 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   <span data-ttu-id="9c357-124">Para obtener más información acerca de los parámetros, vea la [función CChkSGFiles.ErrInit](cchksgfiles-errinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="9c357-124">For more information about the parameters, see [CChkSGFiles.ErrInit function](cchksgfiles-errinit-function.md).</span></span>
   
3. <span data-ttu-id="9c357-125">Use la [función CChkSGFiles.ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md) para validar la integridad de la base de datos mediante la comprobación de los encabezados de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9c357-125">Use the [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md) to validate database integrity by checking the database headers.</span></span>
   
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
   
   <span data-ttu-id="9c357-126">Para obtener más información acerca de los parámetros, vea la [función CChkSGFiles.ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md).</span><span class="sxs-lookup"><span data-stu-id="9c357-126">For more information about the parameters, see [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md).</span></span>
   
4. <span data-ttu-id="9c357-127">Controlar los errores y use la [función CChkSGFiles.Delete](cchksgfiles-delete-function.md) para quitar la clase **CChkSGFiles** de la memoria.</span><span class="sxs-lookup"><span data-stu-id="9c357-127">Handle errors, and use the [CChkSGFiles.Delete function](cchksgfiles-delete-function.md) to remove the **CChkSGFiles** class from memory.</span></span> 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a><span data-ttu-id="9c357-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c357-128">See also</span></span>

- [<span data-ttu-id="9c357-129">Referencia de clase CChkSGFiles</span><span class="sxs-lookup"><span data-stu-id="9c357-129">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md)
- [<span data-ttu-id="9c357-130">Crear copia de seguridad y restauración de aplicaciones para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9c357-130">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
- [<span data-ttu-id="9c357-131">Conceptos de copia de seguridad y restauración para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9c357-131">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    

