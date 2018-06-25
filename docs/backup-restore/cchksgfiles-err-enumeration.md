---
title: CChkSGFiles.ERR (enumeración)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 20f10c43e3b92604bb51e1aa5f896a8bd7c4b335
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763923"
---
# <a name="cchksgfileserr-enumeration"></a><span data-ttu-id="45675-103">CChkSGFiles.ERR (enumeración)</span><span class="sxs-lookup"><span data-stu-id="45675-103">CChkSGFiles.ERR enumeration</span></span> 
  
<span data-ttu-id="45675-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="45675-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="45675-105">Indica el resultado de la función llamada.</span><span class="sxs-lookup"><span data-stu-id="45675-105">Indicates the results of the called function.</span></span> <span data-ttu-id="45675-106">Esta enumeración es devuelto por muchas funciones de la clase **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="45675-106">This enumeration is returned by many functions of the **CCheckSGFiles** class.</span></span> 
  
```cs
Enum ERR  
{
        errSuccess = 0,
        errTaskDropped = -106,
        errRequiredLogFilesMissing = -543,
        errInvalidParameter = -1003,
        errOutOfMemory = -1011,
        errReadVerifyFailure = -1018,
        errTooManyActiveUsers = -1059,
        errDatabaseCorrupted = -1206
}

```

## <a name="values"></a><span data-ttu-id="45675-107">Valores</span><span class="sxs-lookup"><span data-stu-id="45675-107">Values</span></span>

|<span data-ttu-id="45675-108">**Nombre del miembro**</span><span class="sxs-lookup"><span data-stu-id="45675-108">**Member name**</span></span>|<span data-ttu-id="45675-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="45675-109">**Value**</span></span>|<span data-ttu-id="45675-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45675-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45675-111">errSuccess</span><span class="sxs-lookup"><span data-stu-id="45675-111">errSuccess</span></span>  <br/> |<span data-ttu-id="45675-112">0</span><span class="sxs-lookup"><span data-stu-id="45675-112">0</span></span>  <br/> |<span data-ttu-id="45675-113">La función que se completó sin errores.</span><span class="sxs-lookup"><span data-stu-id="45675-113">The function completed without any errors.</span></span>  <br/> |
|<span data-ttu-id="45675-114">errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="45675-114">errTaskDropped</span></span>  <br/> |<span data-ttu-id="45675-115">-106</span><span class="sxs-lookup"><span data-stu-id="45675-115">-106</span></span>  <br/> |<span data-ttu-id="45675-116">Devuelto por la función **ErrTerm** para indicar que no todas las páginas de la base de datos y los archivos de registro de transacciones se protegieron o que se produjeron errores durante la comprobación.</span><span class="sxs-lookup"><span data-stu-id="45675-116">Returned by the **ErrTerm** function to indicate that not all database pages and transaction log files were checked, or that errors were encountered during the verification.</span></span>  <br/> |
|<span data-ttu-id="45675-117">errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="45675-117">errRequiredLogFilesMissing</span></span>  <br/> |<span data-ttu-id="45675-118">-543</span><span class="sxs-lookup"><span data-stu-id="45675-118">-543</span></span>  <br/> |<span data-ttu-id="45675-119">Uno o varios archivos de registro que se requieren para poner la base de datos a un estado de cierre limpio no se encontró en la ruta de acceso del archivo de registro o no tiene el nombre de base de tres letras especificado.</span><span class="sxs-lookup"><span data-stu-id="45675-119">One or more log files that are required to bring the database to a clean-shutdown state was not found in the log file path, or did not have the specified three-letter base name.</span></span>  <br/> |
|<span data-ttu-id="45675-120">errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="45675-120">errInvalidParameter</span></span>  <br/> |<span data-ttu-id="45675-121">-1003</span><span class="sxs-lookup"><span data-stu-id="45675-121">-1003</span></span>  <br/> |<span data-ttu-id="45675-122">Uno o más parámetros que se han pasado a la función no son válidos.</span><span class="sxs-lookup"><span data-stu-id="45675-122">One or more parameters that were passed to the function were invalid.</span></span>  <br/> |
|<span data-ttu-id="45675-123">errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="45675-123">errOutOfMemory</span></span>  <br/> |<span data-ttu-id="45675-124">-1011</span><span class="sxs-lookup"><span data-stu-id="45675-124">-1011</span></span>  <br/> |<span data-ttu-id="45675-125">Memoria insuficiente estaba disponible para completar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="45675-125">Insufficient memory was available to complete the requested operation.</span></span>  <br/> |
|<span data-ttu-id="45675-126">errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="45675-126">errReadVerifyFailure</span></span>  <br/> |<span data-ttu-id="45675-127">-1018</span><span class="sxs-lookup"><span data-stu-id="45675-127">-1018</span></span>  <br/> |<span data-ttu-id="45675-128">La suma de comprobación que se almacena en una página de base de datos no coincide con su suma de comprobación esperada.</span><span class="sxs-lookup"><span data-stu-id="45675-128">The checksum that is stored on a database page does not match its expected checksum.</span></span>  <br/> |
|<span data-ttu-id="45675-129">errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="45675-129">errTooManyActiveUsers</span></span>  <br/> |<span data-ttu-id="45675-130">-1059</span><span class="sxs-lookup"><span data-stu-id="45675-130">-1059</span></span>  <br/> |<span data-ttu-id="45675-131">La función **ErrTerm** se ha llamado mientras estaba utilizando el objeto.</span><span class="sxs-lookup"><span data-stu-id="45675-131">The **ErrTerm** function was called while the object was still being used.</span></span> <span data-ttu-id="45675-132">Esto puede ocurrir si se llama a **ErrTerm** antes de **ErrCheckDbPages** o **ErrCheckLogFiles** ha devuelto.</span><span class="sxs-lookup"><span data-stu-id="45675-132">This can occur if **ErrTerm** is called before **ErrCheckDbPages** or **ErrCheckLogFiles** has returned.</span></span>  <br/> |
   
## <a name="requirements"></a><span data-ttu-id="45675-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45675-133">Requirements</span></span>

<span data-ttu-id="45675-134">Exchange Server 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="45675-134">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="45675-135">La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="45675-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

