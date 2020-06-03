---
title: Función función cchksgfiles. ErrCheckDbPages
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: 78d2dbee6253096d597b4ec2de3878f40ee1b6d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526728"
---
# <a name="cchksgfileserrcheckdbpages-function"></a><span data-ttu-id="48f91-103">Función función cchksgfiles. ErrCheckDbPages</span><span class="sxs-lookup"><span data-stu-id="48f91-103">CChkSGFiles.ErrCheckDbPages function</span></span>

<span data-ttu-id="48f91-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="48f91-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="48f91-105">Valida un intervalo de páginas de una base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="48f91-105">Validates a range of pages in a specified database.</span></span> 
  
```cs
Vitual ERRErrCheckDbPages  
(
    Const ULONGiDb,
    Const VOID  * const pvPageBuffer,
    Const ULONGcbPageBuffer,
    PAGE_INFOrgPageInfo[],
    Const ULONGcPageInfo,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="48f91-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48f91-106">Parameters</span></span>

### <a name="idb"></a><span data-ttu-id="48f91-107">iDb</span><span class="sxs-lookup"><span data-stu-id="48f91-107">iDb</span></span>
  
<span data-ttu-id="48f91-108">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="48f91-108">Input parameter.</span></span> <span data-ttu-id="48f91-109">Un índice en la matriz de bases de datos especificado en el parámetro **rgwszDb []** para la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="48f91-109">An index into the array of databases specified in the **rgwszDb[]** parameter to the **ErrInit** function.</span></span> <span data-ttu-id="48f91-110">Se comprobará la base de datos indizada por este parámetro.</span><span class="sxs-lookup"><span data-stu-id="48f91-110">The database indexed by this parameter will be checked.</span></span> 
    
### <a name="pvpagebuffer"></a><span data-ttu-id="48f91-111">pvPageBuffer</span><span class="sxs-lookup"><span data-stu-id="48f91-111">pvPageBuffer</span></span> 
  
<span data-ttu-id="48f91-112">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="48f91-112">Input parameter.</span></span> <span data-ttu-id="48f91-113">Un puntero a un búfer que contiene una o más páginas de base de datos que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="48f91-113">A pointer to a buffer containing one or more database pages to be checked.</span></span> <span data-ttu-id="48f91-114">El tamaño del búfer debe ser un múltiplo del tamaño de página de la base de datos, tal como lo devuelve la función **ErrCheckDbHeaders** en el parámetro **pcbDbPageSize** .</span><span class="sxs-lookup"><span data-stu-id="48f91-114">The size of the buffer must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> <span data-ttu-id="48f91-115">La aplicación de llamada debe rellenar el búfer con el contenido de la página de base de datos antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="48f91-115">The calling application must fill the buffer with the database page contents before calling **ErrCheckDbPages**.</span></span>
    
### <a name="cbpagebuffer"></a><span data-ttu-id="48f91-116">cbPageBuffer</span><span class="sxs-lookup"><span data-stu-id="48f91-116">cbPageBuffer</span></span>
  
<span data-ttu-id="48f91-117">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="48f91-117">Input parameter.</span></span> <span data-ttu-id="48f91-118">El tamaño del parámetro **pvPageBuffer** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="48f91-118">The size of the **pvPageBuffer** parameter, in bytes.</span></span> <span data-ttu-id="48f91-119">Este valor debe ser un múltiplo del tamaño de página de la base de datos, tal como lo devuelve la función **ErrCheckDbHeaders** en el parámetro **pcbDbPageSize** .</span><span class="sxs-lookup"><span data-stu-id="48f91-119">This value must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> 
    
### <a name="rgpageinfo"></a><span data-ttu-id="48f91-120">rgPageInfo[]</span><span class="sxs-lookup"><span data-stu-id="48f91-120">rgPageInfo[]</span></span> 
  
<span data-ttu-id="48f91-121">Parámetro de entrada/salida.</span><span class="sxs-lookup"><span data-stu-id="48f91-121">Input/output parameter.</span></span> <span data-ttu-id="48f91-122">Matriz de estructuras **de \_ información de página** que **ErrCheckDbPages** rellena con los resultados detallados de cada página de base de datos que se comprueba.</span><span class="sxs-lookup"><span data-stu-id="48f91-122">An array of **PAGE\_INFO** structures that **ErrCheckDbPages** fills with detailed results of each database page that is checked.</span></span> <span data-ttu-id="48f91-123">La matriz debe tener un elemento por cada página de base de datos pasada en el parámetro **pvPageBuffer** , y el campo **ulPgno** de cada estructura de \*\* \_ información de página\*\* debe establecerse en el número de página lógica que corresponde a la página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="48f91-123">The array must have one element for each database page passed in the **pvPageBuffer** parameter, and the **ulPgno** field in each **PAGE\_INFO** structure must be set to the logical page number that corresponds to the database page.</span></span> <span data-ttu-id="48f91-124">Para obtener más información, vea la sección "Comentarios" más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="48f91-124">For more information, see "Remarks" later in this topic.</span></span> 
    
### <a name="cpageinfo"></a><span data-ttu-id="48f91-125">cPageInfo</span><span class="sxs-lookup"><span data-stu-id="48f91-125">cPageInfo</span></span>
  
<span data-ttu-id="48f91-126">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="48f91-126">Input parameter.</span></span> <span data-ttu-id="48f91-127">Número de entradas de la matriz **rgPageInfo []** .</span><span class="sxs-lookup"><span data-stu-id="48f91-127">The number of entries in the **rgPageInfo[]** array.</span></span> <span data-ttu-id="48f91-128">Este valor debe ser igual al número de páginas de base de datos pasadas en el parámetro **pvPageBuffer** .</span><span class="sxs-lookup"><span data-stu-id="48f91-128">This value must be equal to the number of database pages passed in the **pvPageBuffer** parameter.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="48f91-129">ulFlags</span><span class="sxs-lookup"><span data-stu-id="48f91-129">ulFlags</span></span> 
  
<span data-ttu-id="48f91-130">Parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="48f91-130">Optional input parameter.</span></span> <span data-ttu-id="48f91-131">Este valor se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="48f91-131">This value is reserved for future use.</span></span> <span data-ttu-id="48f91-132">El valor que se pasa en este parámetro debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="48f91-132">The value passed in this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="48f91-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48f91-133">Return value</span></span>

<span data-ttu-id="48f91-134">Un código de error de la enumeración [Err](cchksgfiles-err-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="48f91-134">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="48f91-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48f91-135">Remarks</span></span>

<span data-ttu-id="48f91-136">Tenga en cuenta que debe especificar la base de datos en la matriz de bases de datos que se ha pasado a la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="48f91-136">Note that you need to have specified the database in the array of databases passed to the **ErrInit** function.</span></span> <span data-ttu-id="48f91-137">Además, se debe llamar a **ErrCheckDbHeaders** antes de **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="48f91-137">Also, **ErrCheckDbHeaders** must be called before **ErrCheckDbPages**.</span></span>
  
<span data-ttu-id="48f91-138">La aplicación de llamada debe asignar un búfer de memoria lo suficientemente grande como para que las páginas de base de datos se comprueben.</span><span class="sxs-lookup"><span data-stu-id="48f91-138">The calling application must allocate a memory buffer that is large enough to hold the database pages to be checked.</span></span> <span data-ttu-id="48f91-139">La aplicación es responsable de rellenar el búfer con el contenido de una o varias páginas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="48f91-139">The application is responsible for filling the buffer with the contents of one or more such database pages.</span></span> 
  
<span data-ttu-id="48f91-140">La aplicación de llamada debe llamar a **ErrCheckDbHeaders** antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="48f91-140">The calling application must call **ErrCheckDbHeaders** before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="48f91-141">Se puede llamar a esta función tantas veces como sea necesario para cubrir todas las páginas de todos los archivos de base de datos que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="48f91-141">This function can be called as many times as necessary to cover all the pages in all database files that are to be checked.</span></span>
  
<span data-ttu-id="48f91-142">En el parámetro **rgPageInfo []** , cada elemento devuelto contiene información sobre la página de la base de datos en una estructura de \*\* \_ información de página\*\* .</span><span class="sxs-lookup"><span data-stu-id="48f91-142">In the **rgPageInfo[]** parameter, each element returned contains information about the database page in a **PAGE\_INFO** structure.</span></span> <span data-ttu-id="48f91-143">Si la función **ErrCheckDbPages** devuelve un error, la aplicación debe comprobar cada estructura de \*\* \_ información de página\*\* para determinar en qué página se encontró el error.</span><span class="sxs-lookup"><span data-stu-id="48f91-143">If the **ErrCheckDbPages** function returns an error, the application should check each **PAGE\_INFO** structure to determine on which page the error was found.</span></span> <span data-ttu-id="48f91-144">Por ejemplo, si se comparan los valores **checksumActual** y **checksumExpected** , se indicará si se ha detectado un error de suma de comprobación en esa página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="48f91-144">For example, comparing the **checksumActual** and **checksumExpected** values will indicate whether a checksum error was detected on that database page.</span></span> 
  
<span data-ttu-id="48f91-145">Si **ErrCheckDbPages** detecta algún error en el contenido de la base de datos, creará una entrada de registro de eventos de error de Windows.</span><span class="sxs-lookup"><span data-stu-id="48f91-145">If **ErrCheckDbPages** detects any errors in the database content, it will create a Windows Error event log entry.</span></span> 
  
<span data-ttu-id="48f91-146">El objeto **función cchksgfiles** determina si se han comprobado realmente todas las bases de datos registradas con la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="48f91-146">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="48f91-147">Concretamente, **función cchksgfiles** usa la función **ErrCheckDbPages** para determinar si se ha comprobado realmente el mismo número de páginas de base de datos que indica **ErrCheckDbHeaders** .</span><span class="sxs-lookup"><span data-stu-id="48f91-147">Specifically, **CChkSGFiles** uses the **ErrCheckDbPages** function to determine whether the same number of database pages indicated by **ErrCheckDbHeaders** were actually verified.</span></span> <span data-ttu-id="48f91-148">Si no se comprobó correctamente el número correcto de páginas en cada base de datos, la función **ErrTerm** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="48f91-148">If the correct number of pages in each database were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="48f91-149">Si está usando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckDbPages** en la parte multiproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="48f91-149">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckDbPages** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="48f91-150">Tenga en cuenta que se suele llamar a **ErrCheckDbPages** varias veces para cada base de datos que se comprueba.</span><span class="sxs-lookup"><span data-stu-id="48f91-150">Note that **ErrCheckDbPages** is typically called multiple times for each database that is checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="48f91-151">Requirements</span><span class="sxs-lookup"><span data-stu-id="48f91-151">Requirements</span></span>

<span data-ttu-id="48f91-152">Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="48f91-152">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="48f91-153">La cuenta con la que se ejecuta la aplicación debe tener permisos de lectura para los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="48f91-153">The account that the application is running under must have read permissions to the database and log files that are to be checked.</span></span>
  

