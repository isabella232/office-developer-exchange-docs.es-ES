---
title: Función función cchksgfiles. ErrInit
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 'Última modificación: 3 de marzo de 2013'
ms.openlocfilehash: c881691e7c1ba83a396e659f6aac0328625e49a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457014"
---
# <a name="cchksgfileserrinit-function"></a><span data-ttu-id="85c1b-103">Función función cchksgfiles. ErrInit</span><span class="sxs-lookup"><span data-stu-id="85c1b-103">CChkSGFiles.ErrInit function</span></span>
  
<span data-ttu-id="85c1b-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="85c1b-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="85c1b-105">Inicializa el objeto **función cchksgfiles** especificando las bases de datos que se van a comprobar y la ruta de acceso y el nombre base de los archivos de registro de transacciones que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="85c1b-105">Initializes the **CChkSGFiles** object by specifying the databases to be checked and the path and base name of the transaction log files to be checked.</span></span> <span data-ttu-id="85c1b-106">Las aplicaciones deben llamar a esta función inmediatamente después de llamar correctamente a la **nueva** función.</span><span class="sxs-lookup"><span data-stu-id="85c1b-106">Applications should call this function immediately after successfully calling the **New** function.</span></span> 
  
```cs
Vitual ERRErrInit  
(
    Const WCHAR  * const rgwszDb[],
    Const ULONGcDB,
    __in_z const WCHAR  * const wszLogPath,
    __in_z const WCHAR  * const wszBaseName,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="85c1b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85c1b-107">Parameters</span></span>

### <a name="rgwszdb"></a><span data-ttu-id="85c1b-108">rgwszDb[]</span><span class="sxs-lookup"><span data-stu-id="85c1b-108">rgwszDb[]</span></span>
  
<span data-ttu-id="85c1b-109">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="85c1b-109">Input parameter.</span></span> <span data-ttu-id="85c1b-110">Matriz que especifica las bases de datos que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="85c1b-110">An array that specifies the databases to be checked.</span></span> <span data-ttu-id="85c1b-111">Cada elemento de matriz es una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre de archivo de la base de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="85c1b-111">Each array element is a null-terminated Unicode string that contains the path and file name of a database to be checked.</span></span>
    
### <a name="cdb"></a><span data-ttu-id="85c1b-112">cDB</span><span class="sxs-lookup"><span data-stu-id="85c1b-112">cDB</span></span>
  
<span data-ttu-id="85c1b-113">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="85c1b-113">Input parameter.</span></span> <span data-ttu-id="85c1b-114">El número de elementos de ruta de acceso de base de datos válidos en la matriz **rgwszDb** .</span><span class="sxs-lookup"><span data-stu-id="85c1b-114">The number of valid database path elements in the **rgwszDb** array.</span></span> 
    
#### <a name="wszlogpath"></a><span data-ttu-id="85c1b-115">wszLogPath</span><span class="sxs-lookup"><span data-stu-id="85c1b-115">wszLogPath</span></span>
  
<span data-ttu-id="85c1b-116">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="85c1b-116">Input parameter.</span></span> <span data-ttu-id="85c1b-117">Ruta de acceso completa de los archivos de registro de transacciones que se van a comprobar, en forma de una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="85c1b-117">The full path of the transaction log files to be checked, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="wszbasename"></a><span data-ttu-id="85c1b-118">wszBaseName</span><span class="sxs-lookup"><span data-stu-id="85c1b-118">wszBaseName</span></span>
  
<span data-ttu-id="85c1b-119">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="85c1b-119">Input parameter.</span></span> <span data-ttu-id="85c1b-120">Nombre base de tres letras de los archivos de registro de transacciones de Exchange, en forma de una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="85c1b-120">The three-letter base name of the Exchange transaction log files, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="ulflags"></a><span data-ttu-id="85c1b-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="85c1b-121">ulFlags</span></span>
  
<span data-ttu-id="85c1b-122">Parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="85c1b-122">Optional input parameter.</span></span> <span data-ttu-id="85c1b-123">Este valor se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="85c1b-123">This value is reserved for future use.</span></span> <span data-ttu-id="85c1b-124">El valor que pasa este parámetro debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="85c1b-124">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85c1b-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85c1b-125">Return value</span></span>

<span data-ttu-id="85c1b-126">Un código de error de la enumeración [Err](cchksgfiles-err-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="85c1b-126">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85c1b-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85c1b-127">Remarks</span></span>

<span data-ttu-id="85c1b-128">La función **ErrInit** registra las bases de datos y los archivos de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="85c1b-128">The **ErrInit** function registers the databases and log files that are to be checked.</span></span> <span data-ttu-id="85c1b-129">Se debe llamar a esta función después de llamar a la función **New** pero antes de llamar a cualquier otra función **ChkSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="85c1b-129">This function must be called after the **New** function is called but before any other **ChkSGFiles** function is called.</span></span> 
  
<span data-ttu-id="85c1b-130">Debe proporcionar todos los nombres de bases de datos, la ruta de acceso al archivo de registro y el nombre base como cadenas Unicode terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="85c1b-130">You must provide all the database names, the log file path, and the base name as null-terminated Unicode strings.</span></span>
  
<span data-ttu-id="85c1b-131">Puede comprobar sólo los archivos de base de datos, sólo los archivos de registro o los archivos de registro y de base de datos.</span><span class="sxs-lookup"><span data-stu-id="85c1b-131">You can check only the database files, only the log files, or both the database and log files.</span></span> <span data-ttu-id="85c1b-132">Sin embargo, al llamar a esta función, la aplicación debe especificar al menos una entidad que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="85c1b-132">However, when calling this function, the application must specify at least one entity to be checked.</span></span> <span data-ttu-id="85c1b-133">Si se pasa 0 (cero) para **cDB** y null para **wszLogPath** , se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="85c1b-133">Passing 0 (zero) for  **cDB**  and NULL for  **wszLogPath**  will return an error.</span></span> 
  
<span data-ttu-id="85c1b-134">Si el valor de **cDB** es distinto de 0 (cero) y se pasa null para **rgwszDb** , se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="85c1b-134">If the value of  **cDB**  is other than 0 (zero), passing NULL for  **rgwszDb**  will result in an error.</span></span> <span data-ttu-id="85c1b-135">Para comprobar los archivos de base de datos, la aplicación debe proporcionar los nombres de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="85c1b-135">To check the database files, the application must provide the database names.</span></span> 
  
<span data-ttu-id="85c1b-136">Si se pasa NULL para **wszBaseName** pero **WSZLOGPATH** no es null, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="85c1b-136">If NULL is passed for  **wszBaseName**  but  **wszLogPath**  is not NULL, an error will be returned.</span></span> <span data-ttu-id="85c1b-137">El nombre base de un archivo de registro siempre es necesario cuando se comprueban los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="85c1b-137">A log file base name is always required when checking log files.</span></span> 
  
<span data-ttu-id="85c1b-138">Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la función **ErrInit** en la parte de subproceso único de la aplicación y puede llamarla solo una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="85c1b-138">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrInit** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="85c1b-139">Requirements</span><span class="sxs-lookup"><span data-stu-id="85c1b-139">Requirements</span></span>

<span data-ttu-id="85c1b-140">Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="85c1b-140">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="85c1b-141">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="85c1b-141">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

