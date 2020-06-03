---
title: Función función cchksgfiles. ErrCheckLogs
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
ms.openlocfilehash: 71e21bb3a748a532f9e3167e0b36898acde71b02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526721"
---
# <a name="cchksgfileserrchecklogs-function"></a><span data-ttu-id="1e999-103">Función función cchksgfiles. ErrCheckLogs</span><span class="sxs-lookup"><span data-stu-id="1e999-103">CChkSGFiles.ErrCheckLogs function</span></span>

<span data-ttu-id="1e999-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="1e999-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="1e999-105">Valida los archivos de registro de todos los archivos de base de datos especificados en la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="1e999-105">Validates the log files of all the database files that were specified in the **ErrInit** function.</span></span> <span data-ttu-id="1e999-106">Los registros validados son los que existen en la ruta de acceso y que tienen el nombre del archivo de registro base de tres letras pasado a **ErrInit**.</span><span class="sxs-lookup"><span data-stu-id="1e999-106">The validated logs are those that exist in the path, and that have the three-letter base log file name passed to **ErrInit**.</span></span>
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="1e999-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e999-107">Parameters</span></span>

### <a name="pfonlyunnecessarylogscorrupt"></a><span data-ttu-id="1e999-108">pfOnlyUnnecessaryLogsCorrupt</span><span class="sxs-lookup"><span data-stu-id="1e999-108">pfOnlyUnnecessaryLogsCorrupt</span></span> 
  
<span data-ttu-id="1e999-109">Parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="1e999-109">Output parameter.</span></span> <span data-ttu-id="1e999-110">Cuando **es true**, este parámetro indica que se encontraron errores en los archivos de registro de transacciones, pero estos errores se encontraron en los archivos de registro que no son necesarios para poner la base de datos en un estado de cierre limpio sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="1e999-110">When **true**, this parameter indicates that errors were found in the transaction log files, but those errors were all found in log files that are not needed to bring the database to a clean-shutdown state without data loss.</span></span> <span data-ttu-id="1e999-111">Un valor **true** devuelto en este parámetro es válido sólo cuando **ErrCheckLogs** devuelve **errSuccess**.</span><span class="sxs-lookup"><span data-stu-id="1e999-111">A **true** value returned in this parameter is valid only when **ErrCheckLogs** returns **errSuccess**.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="1e999-112">ulFlags</span><span class="sxs-lookup"><span data-stu-id="1e999-112">ulFlags</span></span>
  
<span data-ttu-id="1e999-113">Parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="1e999-113">Optional input parameter.</span></span> <span data-ttu-id="1e999-114">Este valor se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1e999-114">This value is reserved for future use.</span></span> <span data-ttu-id="1e999-115">El valor que pasa este parámetro debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="1e999-115">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e999-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e999-116">Return value</span></span>

<span data-ttu-id="1e999-117">Un código de error de la enumeración [Err](cchksgfiles-err-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="1e999-117">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
<span data-ttu-id="1e999-118">Es importante recordar que esta función puede devolver **errSuccess** incluso cuando se encuentran errores en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="1e999-118">It's important to remember that this function can return **errSuccess** even when errors are found in the log files.</span></span> <span data-ttu-id="1e999-119">Por lo tanto, cuando **ErrCheckLogs** devuelve **errSuccess**, la aplicación también debe comprobar el parámetro **pfOnlyUnnecessaryLogsCorrupt** Return.</span><span class="sxs-lookup"><span data-stu-id="1e999-119">Therefore, when **ErrCheckLogs** returns **errSuccess**, the application should also check the  **pfOnlyUnnecessaryLogsCorrupt** return parameter.</span></span> <span data-ttu-id="1e999-120">Si **pfOnlyUnnecessaryLogsCorrupts** es **true** cuando **ErrCheckLogs** devuelve **errSuccess**, esto indica que se encontraron uno o varios errores, pero solo en los archivos de registro no se necesitan para actualizar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1e999-120">If **pfOnlyUnnecessaryLogsCorrupts** is **true** when **ErrCheckLogs** returns **errSuccess**, this indicates that one or more errors were found, but only in log files not needed to bring the database up-to-date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e999-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e999-121">Remarks</span></span>

<span data-ttu-id="1e999-122">Se debe llamar a la función **ErrCheckDbHeaders** antes de que se pueda llamar a la función **ErrCheckLogs** .</span><span class="sxs-lookup"><span data-stu-id="1e999-122">The **ErrCheckDbHeaders** function must be called before the **ErrCheckLogs** function can be called.</span></span> 
  
<span data-ttu-id="1e999-123">Cuando se comprueban los archivos de registro de transacciones de base de datos de Exchange, algunos de los archivos de registro serán necesarios para traer las bases de datos del grupo de almacenamiento a un estado de cierre limpio sin pérdida de datos, mientras que otros archivos de registro podrían no ser necesarios.</span><span class="sxs-lookup"><span data-stu-id="1e999-123">When Exchange database transaction log files are being checked, some of the log files will be necessary to bring the databases in the storage group to a clean-shutdown state without data loss, whereas other log files might not be needed.</span></span> <span data-ttu-id="1e999-124">La función **ErrCheckLogs** determina los archivos de registro más antiguos y los más recientes que se necesitan para actualizar las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="1e999-124">The **ErrCheckLogs** function determines both the oldest and the newest log files that are needed to bring the databases up to date.</span></span> 
  
<span data-ttu-id="1e999-125">La función **ErrCheckLogs** comprueba todos los archivos de registro en las rutas de acceso especificadas que también tienen el nombre de archivo base de tres letras especificado, como se pasan a la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="1e999-125">The **ErrCheckLogs** function verifies all the log files in the specified paths that also have the specified three-letter base file name, as passed to the **ErrInit** function.</span></span> 
  
<span data-ttu-id="1e999-126">Si no se encuentran errores en los archivos de registro, **ErrCheckLogs** devuelve **errSuccess**.</span><span class="sxs-lookup"><span data-stu-id="1e999-126">If no errors are found in the log files, **ErrCheckLogs** returns **errSuccess**.</span></span> 
  
<span data-ttu-id="1e999-127">Si alguno de los archivos de registro necesarios se encuentra dañado, **ErrCheckLogs** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1e999-127">If any of the required log files are found to be corrupted, **ErrCheckLogs** returns an error.</span></span> 
  
<span data-ttu-id="1e999-128">Si se encuentran errores sólo en los archivos de registro más antiguos que los que se necesitan antes, la función devuelve **errSuccess** y establece el parámetro de devolución **pfOnlyUnnecessaryLogCorrupt** en **true**.</span><span class="sxs-lookup"><span data-stu-id="1e999-128">If errors are found only in log files that are older than the earliest ones needed, the function returns **errSuccess** and sets the return parameter **pfOnlyUnnecessaryLogCorrupt** to **true**.</span></span> <span data-ttu-id="1e999-129">La aplicación debe reconocer que hay errores en algunos de los archivos de registro antiguos y, si es así, se alerta al usuario.</span><span class="sxs-lookup"><span data-stu-id="1e999-129">The application should recognize that there are errors in some of those old log files, and if so, it will possibly alert the user.</span></span> <span data-ttu-id="1e999-130">En cualquier caso, estos errores no deberían afectar a la integridad general de la base de datos ni influir en que la reproducción de los registros reenvío se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="1e999-130">In any case, those errors should not affect the overall integrity of the database or affect whether playing the logs forward will succeed.</span></span>
  
<span data-ttu-id="1e999-131">Si se encuentran errores en cualquier archivo de registro que se crea después del registro más antiguo que **ErrCheckLogs** determina que es necesario, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1e999-131">If errors are found in any log file created after the earliest log that **ErrCheckLogs** determines is needed, the function returns an error.</span></span> <span data-ttu-id="1e999-132">El error se devolverá incluso si se encuentra el error del archivo de registro en un archivo de registro que se generó después de lo necesario para poner la base de datos actualizada.</span><span class="sxs-lookup"><span data-stu-id="1e999-132">The error will be returned even if the log file error was found in a log file that was generated later than what is needed to bring the database up to date.</span></span> <span data-ttu-id="1e999-133">Si bien sería posible traer las bases de datos a un estado de cierre limpio mediante el uso de los archivos de registro identificados, las transacciones especificadas en los archivos de registro dañados más adelante no se aplicarían, lo que daría como resultado una pérdida de datos cuando se restaure la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1e999-133">Although it would be possible to bring the databases to a clean-shutdown state by using the identified log files, transactions specified in the later corrupted log files would not be applied, resulting in data loss when the database is restored.</span></span> 
  
<span data-ttu-id="1e999-134">El objeto **función cchksgfiles** determina si todos los archivos de registro registrados con la función **ErrInit** se han comprobado realmente.</span><span class="sxs-lookup"><span data-stu-id="1e999-134">The **CChkSGFiles** object determines whether all of the log files registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="1e999-135">Si no todos los registros no se comprobaron correctamente, la función **ErrTerm** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1e999-135">If not all of the logs were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="1e999-136">Si está usando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckLogs** en la parte multiproceso de la aplicación, pero sólo puede llamar una vez por cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="1e999-136">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckLogs** function in the multithreaded portion of the application, but you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="1e999-137">Requirements</span><span class="sxs-lookup"><span data-stu-id="1e999-137">Requirements</span></span>

<span data-ttu-id="1e999-138">Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="1e999-138">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="1e999-139">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="1e999-139">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

