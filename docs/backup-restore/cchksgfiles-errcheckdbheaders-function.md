---
title: Función función cchksgfiles. ErrCheckDbHeaders
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: a62c5940322d3d7a71f2db93214f1e970fc6859b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455250"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a><span data-ttu-id="f18e1-103">Función función cchksgfiles. ErrCheckDbHeaders</span><span class="sxs-lookup"><span data-stu-id="f18e1-103">CChkSGFiles.ErrCheckDbHeaders function</span></span>

<span data-ttu-id="f18e1-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="f18e1-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span> 
  
<span data-ttu-id="f18e1-105">Valida los encabezados de los archivos de base de datos que especificó la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="f18e1-105">Validates the headers of the database files that were specified by the **ErrInit** function.</span></span> <span data-ttu-id="f18e1-106">Esta función también devuelve el tamaño de página y el número de páginas de cada una de las bases de datos especificadas.</span><span class="sxs-lookup"><span data-stu-id="f18e1-106">This function also returns the page size and number of pages in each of the specified databases.</span></span> 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="f18e1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f18e1-107">Parameters</span></span>

### <a name="pcbdbpagesize"></a><span data-ttu-id="f18e1-108">pcbDbPageSize</span><span class="sxs-lookup"><span data-stu-id="f18e1-108">pcbDbPageSize</span></span> 
  
<span data-ttu-id="f18e1-109">Parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="f18e1-109">Output parameter.</span></span> <span data-ttu-id="f18e1-110">El tamaño de página de cada una de las bases de datos especificadas, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f18e1-110">The page size of each of the specified databases, in bytes.</span></span>
    
### <a name="pcheaderpagesperdb"></a><span data-ttu-id="f18e1-111">pcHeaderPagesPerDb</span><span class="sxs-lookup"><span data-stu-id="f18e1-111">pcHeaderPagesPerDb</span></span> 
  
<span data-ttu-id="f18e1-112">Parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="f18e1-112">Output parameter.</span></span> <span data-ttu-id="f18e1-113">Número de páginas al principio de cada base de datos especificada que están reservadas por el motor de base de datos para uso interno.</span><span class="sxs-lookup"><span data-stu-id="f18e1-113">The number of pages at the beginning of each specified database that are reserved by the database engine for internal use.</span></span> <span data-ttu-id="f18e1-114">Tenga en cuenta que *no* debe pasar páginas de encabezado a la función **ErrCheckDbPages** para la validación.</span><span class="sxs-lookup"><span data-stu-id="f18e1-114">Note that you should *not* pass header pages to the **ErrCheckDbPages** function for validation.</span></span> 
    
### <a name="pidberrorencountered"></a><span data-ttu-id="f18e1-115">piDbErrorEncountered</span><span class="sxs-lookup"><span data-stu-id="f18e1-115">piDbErrorEncountered</span></span>
  
<span data-ttu-id="f18e1-116">Parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="f18e1-116">Output parameter.</span></span> <span data-ttu-id="f18e1-117">Si el valor devuelto de la función indica un error, este parámetro será un índice en la matriz **rgwszDb []** pasada a la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="f18e1-117">If the return value of the function indicates an error, this parameter will be an index into the **rgwszDb[]** array passed to the **ErrInit** function.</span></span> <span data-ttu-id="f18e1-118">El elemento de matriz indizada representa la base de datos en la que se encontró el error.</span><span class="sxs-lookup"><span data-stu-id="f18e1-118">The indexed array element represents the database in which the error was encountered.</span></span> <span data-ttu-id="f18e1-119">Si la función no devuelve un valor de error, este valor de parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="f18e1-119">If the function does not return an error value, this parameter value is invalid.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="f18e1-120">ulFlags</span><span class="sxs-lookup"><span data-stu-id="f18e1-120">ulFlags</span></span> 
  
<span data-ttu-id="f18e1-121">Parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="f18e1-121">Optional input parameter.</span></span> <span data-ttu-id="f18e1-122">Este valor se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f18e1-122">This value is reserved for future use.</span></span> <span data-ttu-id="f18e1-123">El valor pasado debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="f18e1-123">The value passed should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f18e1-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f18e1-124">Return value</span></span>

<span data-ttu-id="f18e1-125">Esta función devuelve un código de error de la [enumeración función cchksgfiles. err](cchksgfiles-err-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f18e1-125">This function returns an error code from the [CChkSGFiles.ERR enumeration](cchksgfiles-err-enumeration.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f18e1-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f18e1-126">Remarks</span></span>

<span data-ttu-id="f18e1-127">**ErrCheckDbHeaders** comprueba que todas las bases de datos registradas con **ErrInit** tienen la misma firma de registro y tamaño de página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f18e1-127">**ErrCheckDbHeaders** verifies that all databases registered with **ErrInit** have the same log signature and database page size.</span></span> <span data-ttu-id="f18e1-128">También puede usar el valor del parámetro **genMin** más bajo y el valor del parámetro más alto **genMax** para determinar el conjunto de archivos de registro que son necesarios para poner todas las bases de datos registradas en un estado de cierre limpio.</span><span class="sxs-lookup"><span data-stu-id="f18e1-128">You can also use the lowest **genMin** parameter value and the highest **genMax** parameter value to determine the set of log files that are necessary to bring all of the registered databases to a clean-shutdown state.</span></span> 
  
<span data-ttu-id="f18e1-129">El parámetro **piDbErrorEncountered** se establece únicamente cuando se detecta un error, tal como lo indica un valor devuelto distinto de cero **ErrCheckDbHeaders** .</span><span class="sxs-lookup"><span data-stu-id="f18e1-129">The **piDbErrorEncountered** parameter is set only when an error is detected, as indicated by a non-zero **ErrCheckDbHeaders** return value.</span></span> 
  
<span data-ttu-id="f18e1-130">Cuando se produce un error en esta función, se agrega un evento de error al registro de eventos de error de Windows.</span><span class="sxs-lookup"><span data-stu-id="f18e1-130">When an error occurs in this function, an error event will be added to the Windows Error event log.</span></span>
  
<span data-ttu-id="f18e1-131">Puede llamar a **ErrCheckDbHeaders** solo después de llamar a **ErrInit**y debe llamarlo antes de llamar a **ErrCheckDbPages** y **ErrCheckLogs**.</span><span class="sxs-lookup"><span data-stu-id="f18e1-131">You can call **ErrCheckDbHeaders** only after calling **ErrInit**, and you must call it before calling **ErrCheckDbPages** and **ErrCheckLogs**.</span></span>
  
<span data-ttu-id="f18e1-132">Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la función **ErrCheckDbHeaders** en la parte de subproceso único y puede llamarla solo una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="f18e1-132">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrCheckDbHeaders** function in the single-threaded portion, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="f18e1-133">Requirements</span><span class="sxs-lookup"><span data-stu-id="f18e1-133">Requirements</span></span>

<span data-ttu-id="f18e1-134">Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="f18e1-134">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="f18e1-135">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="f18e1-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

