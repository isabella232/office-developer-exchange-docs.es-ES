---
title: CChkSGFiles.ErrCheckLogs (función)
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: 5b1070de73bc23ae09ddb7835bd72c8e8a71a95f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762980"
---
# <a name="cchksgfileserrchecklogs-function"></a><span data-ttu-id="5d525-103">CChkSGFiles.ErrCheckLogs (función)</span><span class="sxs-lookup"><span data-stu-id="5d525-103">CChkSGFiles.ErrCheckLogs function</span></span>

<span data-ttu-id="5d525-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d525-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="5d525-105">Valida los archivos de registro de todos los archivos de base de datos que se especificaron en la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="5d525-105">Validates the log files of all the database files that were specified in the **ErrInit** function.</span></span> <span data-ttu-id="5d525-106">Los registros de validado son aquellos que existen en la ruta de acceso, y que tienen el nombre de archivo de registro de base de tres letras que se pasan a **ErrInit**.</span><span class="sxs-lookup"><span data-stu-id="5d525-106">The validated logs are those that exist in the path, and that have the three-letter base log file name passed to **ErrInit**.</span></span>
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="5d525-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d525-107">Parameters</span></span>

### <a name="pfonlyunnecessarylogscorrupt"></a><span data-ttu-id="5d525-108">pfOnlyUnnecessaryLogsCorrupt</span><span class="sxs-lookup"><span data-stu-id="5d525-108">pfOnlyUnnecessaryLogsCorrupt</span></span> 
  
<span data-ttu-id="5d525-109">Parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="5d525-109">Output parameter.</span></span> <span data-ttu-id="5d525-110">Cuando **true**, este parámetro indica que se encontraron errores en los archivos de registro de transacciones, pero esos errores se han poner todos los que se encuentran en los archivos de registro que no son necesarios para la base de datos en un estado de cierre limpio sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="5d525-110">When **true**, this parameter indicates that errors were found in the transaction log files, but those errors were all found in log files that are not needed to bring the database to a clean-shutdown state without data loss.</span></span> <span data-ttu-id="5d525-111">Un valor **true** devuelto en este parámetro sólo es válido cuando **ErrCheckLogs** devuelve **errSuccess**.</span><span class="sxs-lookup"><span data-stu-id="5d525-111">A **true** value returned in this parameter is valid only when **ErrCheckLogs** returns **errSuccess**.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="5d525-112">ulFlags</span><span class="sxs-lookup"><span data-stu-id="5d525-112">ulFlags</span></span>
  
<span data-ttu-id="5d525-113">Parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="5d525-113">Optional input parameter.</span></span> <span data-ttu-id="5d525-114">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5d525-114">This value is reserved for future use.</span></span> <span data-ttu-id="5d525-115">El valor pasado por este parámetro debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5d525-115">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5d525-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d525-116">Return value</span></span>

<span data-ttu-id="5d525-117">Un código de error de la enumeración [ERR](cchksgfiles-err-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="5d525-117">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
<span data-ttu-id="5d525-118">Es importante recordar que esta función puede devolver **errSuccess** incluso cuando se encuentran errores en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="5d525-118">It's important to remember that this function can return **errSuccess** even when errors are found in the log files.</span></span> <span data-ttu-id="5d525-119">Por lo tanto, cuando **ErrCheckLogs** devuelve **errSuccess**, la aplicación debe comprobar también el parámetro de devolución de **pfOnlyUnnecessaryLogsCorrupt** .</span><span class="sxs-lookup"><span data-stu-id="5d525-119">Therefore, when **ErrCheckLogs** returns **errSuccess**, the application should also check the  **pfOnlyUnnecessaryLogsCorrupt** return parameter.</span></span> <span data-ttu-id="5d525-120">Si **pfOnlyUnnecessaryLogsCorrupts** es **true** cuando **ErrCheckLogs** devuelve **errSuccess**, esto indica que se han encontrado uno o más errores, pero sólo en los archivos de registro que no sea necesarios para actualizar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5d525-120">If **pfOnlyUnnecessaryLogsCorrupts** is **true** when **ErrCheckLogs** returns **errSuccess**, this indicates that one or more errors were found, but only in log files not needed to bring the database up-to-date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d525-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d525-121">Remarks</span></span>

<span data-ttu-id="5d525-122">Para poder llamar a la función **ErrCheckLogs** , se debe llamar a la función **ErrCheckDbHeaders** .</span><span class="sxs-lookup"><span data-stu-id="5d525-122">The **ErrCheckDbHeaders** function must be called before the **ErrCheckLogs** function can be called.</span></span> 
  
<span data-ttu-id="5d525-123">Cuando se están comprobando los archivos de registro de transacciones de base de datos de Exchange, algunos de los archivos de registro será necesario para incorporar las bases de datos en el grupo de almacenamiento a un estado de cierre limpio sin pérdida de datos, mientras que otros archivos de registro que no sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="5d525-123">When Exchange database transaction log files are being checked, some of the log files will be necessary to bring the databases in the storage group to a clean-shutdown state without data loss, whereas other log files might not be needed.</span></span> <span data-ttu-id="5d525-124">La función **ErrCheckLogs** determina el más antiguo y los archivos de registro más recientes que se necesitan para incorporar las bases de datos actualizados.</span><span class="sxs-lookup"><span data-stu-id="5d525-124">The **ErrCheckLogs** function determines both the oldest and the newest log files that are needed to bring the databases up to date.</span></span> 
  
<span data-ttu-id="5d525-125">La función **ErrCheckLogs** comprueba todos los archivos de registro de las rutas de acceso especificadas que también tienen el nombre de archivo de base de tres letras, tal y como se pasan a la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="5d525-125">The **ErrCheckLogs** function verifies all the log files in the specified paths that also have the specified three-letter base file name, as passed to the **ErrInit** function.</span></span> 
  
<span data-ttu-id="5d525-126">Si no se encontraron errores en los archivos de registro, **ErrCheckLogs** devuelve **errSuccess**.</span><span class="sxs-lookup"><span data-stu-id="5d525-126">If no errors are found in the log files, **ErrCheckLogs** returns **errSuccess**.</span></span> 
  
<span data-ttu-id="5d525-127">Si encuentra alguno de los archivos de registro necesarios que está dañado, **ErrCheckLogs** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="5d525-127">If any of the required log files are found to be corrupted, **ErrCheckLogs** returns an error.</span></span> 
  
<span data-ttu-id="5d525-128">Si se encuentran errores sólo en los archivos de registro que son anteriores a los que se necesitan más antigua, la función devuelve **errSuccess** y establece el parámetro de devolución **pfOnlyUnnecessaryLogCorrupt** en **true**.</span><span class="sxs-lookup"><span data-stu-id="5d525-128">If errors are found only in log files that are older than the earliest ones needed, the function returns **errSuccess** and sets the return parameter **pfOnlyUnnecessaryLogCorrupt** to **true**.</span></span> <span data-ttu-id="5d525-129">La aplicación debe reconocer que hay errores en algunos de los archivos de registro anterior y, si es así, posiblemente avisará al usuario.</span><span class="sxs-lookup"><span data-stu-id="5d525-129">The application should recognize that there are errors in some of those old log files, and if so, it will possibly alert the user.</span></span> <span data-ttu-id="5d525-130">En cualquier caso, esos errores no deberían afectar a la integridad de la base de datos general o afecta a si reproducir los registros hacia delante se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="5d525-130">In any case, those errors should not affect the overall integrity of the database or affect whether playing the logs forward will succeed.</span></span>
  
<span data-ttu-id="5d525-131">Si se encuentran errores en cualquier archivo de registro creado después de la fecha más temprana registro que determina **ErrCheckLogs** es necesario, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="5d525-131">If errors are found in any log file created after the earliest log that **ErrCheckLogs** determines is needed, the function returns an error.</span></span> <span data-ttu-id="5d525-132">Incluso si se encontró el error del archivo de registro en un archivo de registro que se generó más adelante a lo que es necesario para incorporar la base de datos actualizado se devolverá el error.</span><span class="sxs-lookup"><span data-stu-id="5d525-132">The error will be returned even if the log file error was found in a log file that was generated later than what is needed to bring the database up to date.</span></span> <span data-ttu-id="5d525-133">Si bien sería posible incorporar las bases de datos a un estado de cierre limpio mediante el uso de los archivos de registro identificada, no se aplicaría transacciones especificadas en los archivos de registro dañado más adelante, lo que resulta en pérdida de datos cuando se restaura la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5d525-133">Although it would be possible to bring the databases to a clean-shutdown state by using the identified log files, transactions specified in the later corrupted log files would not be applied, resulting in data loss when the database is restored.</span></span> 
  
<span data-ttu-id="5d525-134">El objeto **CChkSGFiles** determina si realmente se han comprobado todos los archivos de registro registrados con la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="5d525-134">The **CChkSGFiles** object determines whether all of the log files registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="5d525-135">Si no todos los registros de no correctamente comprobados, la función **ErrTerm** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="5d525-135">If not all of the logs were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="5d525-136">Si está utilizando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckLogs** en la parte de la aplicación multiproceso, pero se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="5d525-136">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckLogs** function in the multithreaded portion of the application, but you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="5d525-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d525-137">Requirements</span></span>

<span data-ttu-id="5d525-138">Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="5d525-138">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="5d525-139">La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="5d525-139">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

