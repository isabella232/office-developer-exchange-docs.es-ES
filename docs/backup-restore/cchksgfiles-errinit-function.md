---
title: CChkSGFiles.ErrInit (función)
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
description: 'Última modificación: 03 de marzo de 2013'
ms.openlocfilehash: d4b76933a747fe4bf084061cf080bc68264132ed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762976"
---
# <a name="cchksgfileserrinit-function"></a><span data-ttu-id="c4eca-103">CChkSGFiles.ErrInit (función)</span><span class="sxs-lookup"><span data-stu-id="c4eca-103">CChkSGFiles.ErrInit function</span></span>
  
<span data-ttu-id="c4eca-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4eca-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="c4eca-105">Inicializa el objeto **CChkSGFiles** mediante la especificación de las bases de datos que se va a comprobar y la ruta de acceso y el nombre de base de los archivos de registro de transacciones que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="c4eca-105">Initializes the **CChkSGFiles** object by specifying the databases to be checked and the path and base name of the transaction log files to be checked.</span></span> <span data-ttu-id="c4eca-106">Las aplicaciones deben llamar a esta función inmediatamente después de llamar correctamente a la función de **nuevo** .</span><span class="sxs-lookup"><span data-stu-id="c4eca-106">Applications should call this function immediately after successfully calling the **New** function.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="c4eca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4eca-107">Parameters</span></span>

### <a name="rgwszdb"></a><span data-ttu-id="c4eca-108">[] rgwszDb</span><span class="sxs-lookup"><span data-stu-id="c4eca-108">rgwszDb[]</span></span>
  
<span data-ttu-id="c4eca-109">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4eca-109">Input parameter.</span></span> <span data-ttu-id="c4eca-110">Una matriz que especifica las bases de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="c4eca-110">An array that specifies the databases to be checked.</span></span> <span data-ttu-id="c4eca-111">Cada elemento de la matriz es una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre de una base de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="c4eca-111">Each array element is a null-terminated Unicode string that contains the path and file name of a database to be checked.</span></span>
    
### <a name="cdb"></a><span data-ttu-id="c4eca-112">cDB</span><span class="sxs-lookup"><span data-stu-id="c4eca-112">cDB</span></span>
  
<span data-ttu-id="c4eca-113">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4eca-113">Input parameter.</span></span> <span data-ttu-id="c4eca-114">El número de elementos de la ruta de acceso de base de datos válido en la matriz **rgwszDb** .</span><span class="sxs-lookup"><span data-stu-id="c4eca-114">The number of valid database path elements in the **rgwszDb** array.</span></span> 
    
#### <a name="wszlogpath"></a><span data-ttu-id="c4eca-115">wszLogPath</span><span class="sxs-lookup"><span data-stu-id="c4eca-115">wszLogPath</span></span>
  
<span data-ttu-id="c4eca-116">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4eca-116">Input parameter.</span></span> <span data-ttu-id="c4eca-117">La ruta de acceso completa de los archivos de registro de transacciones a comprobarse, con el formato de una cadena Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="c4eca-117">The full path of the transaction log files to be checked, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="wszbasename"></a><span data-ttu-id="c4eca-118">wszBaseName</span><span class="sxs-lookup"><span data-stu-id="c4eca-118">wszBaseName</span></span>
  
<span data-ttu-id="c4eca-119">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4eca-119">Input parameter.</span></span> <span data-ttu-id="c4eca-120">El nombre de base de tres letras de los archivos de registro de transacciones de Exchange, en el formulario de una cadena Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="c4eca-120">The three-letter base name of the Exchange transaction log files, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="ulflags"></a><span data-ttu-id="c4eca-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="c4eca-121">ulFlags</span></span>
  
<span data-ttu-id="c4eca-122">Parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="c4eca-122">Optional input parameter.</span></span> <span data-ttu-id="c4eca-123">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c4eca-123">This value is reserved for future use.</span></span> <span data-ttu-id="c4eca-124">El valor pasado por este parámetro debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="c4eca-124">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4eca-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4eca-125">Return value</span></span>

<span data-ttu-id="c4eca-126">Un código de error de la enumeración [ERR](cchksgfiles-err-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="c4eca-126">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c4eca-127">Notas</span><span class="sxs-lookup"><span data-stu-id="c4eca-127">Remarks</span></span>

<span data-ttu-id="c4eca-128">La función **ErrInit** registra las bases de datos y los archivos de registro que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="c4eca-128">The **ErrInit** function registers the databases and log files that are to be checked.</span></span> <span data-ttu-id="c4eca-129">Después de llamar a la función de **nuevo** , pero antes de cualquier otro **ChkSGFiles** se denomina función, se debe llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="c4eca-129">This function must be called after the **New** function is called but before any other **ChkSGFiles** function is called.</span></span> 
  
<span data-ttu-id="c4eca-130">Debe proporcionar todos los nombres de base de datos, la ruta de acceso del archivo de registro y el nombre base como cadenas de Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="c4eca-130">You must provide all the database names, the log file path, and the base name as null-terminated Unicode strings.</span></span>
  
<span data-ttu-id="c4eca-131">Puede comprobar los archivos de base de datos, sólo los archivos de registro o los archivos de registro y base de datos.</span><span class="sxs-lookup"><span data-stu-id="c4eca-131">You can check only the database files, only the log files, or both the database and log files.</span></span> <span data-ttu-id="c4eca-132">Sin embargo, cuando se llama a esta función, la aplicación debe especificar al menos una entidad que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="c4eca-132">However, when calling this function, the application must specify at least one entity to be checked.</span></span> <span data-ttu-id="c4eca-133">Pasar un valor 0 (cero) para **cDB** y NULL para **wszLogPath** devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="c4eca-133">Passing 0 (zero) for  **cDB**  and NULL for  **wszLogPath**  will return an error.</span></span> 
  
<span data-ttu-id="c4eca-134">Si el valor de **cDB** es distinto de 0 (cero), pasando NULL para **rgwszDb** dará como resultado un error.</span><span class="sxs-lookup"><span data-stu-id="c4eca-134">If the value of  **cDB**  is other than 0 (zero), passing NULL for  **rgwszDb**  will result in an error.</span></span> <span data-ttu-id="c4eca-135">Para comprobar los archivos de base de datos, la aplicación debe proporcionar los nombres de base de datos.</span><span class="sxs-lookup"><span data-stu-id="c4eca-135">To check the database files, the application must provide the database names.</span></span> 
  
<span data-ttu-id="c4eca-136">Si se pasa NULL para **wszBaseName** , pero **wszLogPath** no es NULL, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="c4eca-136">If NULL is passed for  **wszBaseName**  but  **wszLogPath**  is not NULL, an error will be returned.</span></span> <span data-ttu-id="c4eca-137">Siempre se requiere un nombre base del archivo de registro durante la comprobación de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="c4eca-137">A log file base name is always required when checking log files.</span></span> 
  
<span data-ttu-id="c4eca-138">Si utiliza en una aplicación multiproceso CHKSGFILES, debe llamar a la función **ErrInit** en la parte de un único subproceso de la aplicación y se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="c4eca-138">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrInit** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="c4eca-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4eca-139">Requirements</span></span>

<span data-ttu-id="c4eca-140">Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="c4eca-140">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="c4eca-141">La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="c4eca-141">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

