---
title: Enumeración función cchksgfiles. ERR
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dbc76601a808f79ce3ed5b5dc9fbe4cf92efb015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455257"
---
# <a name="cchksgfileserr-enumeration"></a><span data-ttu-id="2cc2d-103">Enumeración función cchksgfiles. ERR</span><span class="sxs-lookup"><span data-stu-id="2cc2d-103">CChkSGFiles.ERR enumeration</span></span> 
  
<span data-ttu-id="2cc2d-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="2cc2d-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="2cc2d-105">Indica los resultados de la función llamada.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-105">Indicates the results of the called function.</span></span> <span data-ttu-id="2cc2d-106">Esta enumeración es devuelta por muchas funciones de la clase **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="2cc2d-106">This enumeration is returned by many functions of the **CCheckSGFiles** class.</span></span> 
  
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

## <a name="values"></a><span data-ttu-id="2cc2d-107">Valores</span><span class="sxs-lookup"><span data-stu-id="2cc2d-107">Values</span></span>

|<span data-ttu-id="2cc2d-108">**Nombre del miembro**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-108">**Member name**</span></span>|<span data-ttu-id="2cc2d-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-109">**Value**</span></span>|<span data-ttu-id="2cc2d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2cc2d-111">errSuccess</span><span class="sxs-lookup"><span data-stu-id="2cc2d-111">errSuccess</span></span>  <br/> |<span data-ttu-id="2cc2d-112">comprendi</span><span class="sxs-lookup"><span data-stu-id="2cc2d-112">0</span></span>  <br/> |<span data-ttu-id="2cc2d-113">La función se completó sin errores.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-113">The function completed without any errors.</span></span>  <br/> |
|<span data-ttu-id="2cc2d-114">errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="2cc2d-114">errTaskDropped</span></span>  <br/> |<span data-ttu-id="2cc2d-115">-106</span><span class="sxs-lookup"><span data-stu-id="2cc2d-115">-106</span></span>  <br/> |<span data-ttu-id="2cc2d-116">Devuelto por la función **ErrTerm** para indicar que no se comprobaron todas las páginas de base de datos y los archivos de registro de transacciones, o que se detectaron errores durante la comprobación.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-116">Returned by the **ErrTerm** function to indicate that not all database pages and transaction log files were checked, or that errors were encountered during the verification.</span></span>  <br/> |
|<span data-ttu-id="2cc2d-117">errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="2cc2d-117">errRequiredLogFilesMissing</span></span>  <br/> |<span data-ttu-id="2cc2d-118">-543</span><span class="sxs-lookup"><span data-stu-id="2cc2d-118">-543</span></span>  <br/> |<span data-ttu-id="2cc2d-119">No se encontró en la ruta del archivo de registro uno o varios archivos de registro que son necesarios para poner la base de datos en un estado de cierre limpio, o bien no tenían el nombre base de tres letras especificado.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-119">One or more log files that are required to bring the database to a clean-shutdown state was not found in the log file path, or did not have the specified three-letter base name.</span></span>  <br/> |
|<span data-ttu-id="2cc2d-120">errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2cc2d-120">errInvalidParameter</span></span>  <br/> |<span data-ttu-id="2cc2d-121">-1003</span><span class="sxs-lookup"><span data-stu-id="2cc2d-121">-1003</span></span>  <br/> |<span data-ttu-id="2cc2d-122">Uno o más parámetros que se pasaron a la función no son válidos.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-122">One or more parameters that were passed to the function were invalid.</span></span>  <br/> |
|<span data-ttu-id="2cc2d-123">errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="2cc2d-123">errOutOfMemory</span></span>  <br/> |<span data-ttu-id="2cc2d-124">-1011</span><span class="sxs-lookup"><span data-stu-id="2cc2d-124">-1011</span></span>  <br/> |<span data-ttu-id="2cc2d-125">Memoria insuficiente para completar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-125">Insufficient memory was available to complete the requested operation.</span></span>  <br/> |
|<span data-ttu-id="2cc2d-126">errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="2cc2d-126">errReadVerifyFailure</span></span>  <br/> |<span data-ttu-id="2cc2d-127">-1018</span><span class="sxs-lookup"><span data-stu-id="2cc2d-127">-1018</span></span>  <br/> |<span data-ttu-id="2cc2d-128">La suma de comprobación que se almacena en una página de base de datos no coincide con la suma de comprobación esperada.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-128">The checksum that is stored on a database page does not match its expected checksum.</span></span>  <br/> |
|<span data-ttu-id="2cc2d-129">errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="2cc2d-129">errTooManyActiveUsers</span></span>  <br/> |<span data-ttu-id="2cc2d-130">-1059</span><span class="sxs-lookup"><span data-stu-id="2cc2d-130">-1059</span></span>  <br/> |<span data-ttu-id="2cc2d-131">Se llamó a la función **ErrTerm** mientras el objeto se usaba todavía.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-131">The **ErrTerm** function was called while the object was still being used.</span></span> <span data-ttu-id="2cc2d-132">Esto puede ocurrir si se llama a **ErrTerm** antes de que se devuelva **ErrCheckDbPages** o **ErrCheckLogFiles** .</span><span class="sxs-lookup"><span data-stu-id="2cc2d-132">This can occur if **ErrTerm** is called before **ErrCheckDbPages** or **ErrCheckLogFiles** has returned.</span></span>  <br/> |
   
## <a name="requirements"></a><span data-ttu-id="2cc2d-133">Requirements</span><span class="sxs-lookup"><span data-stu-id="2cc2d-133">Requirements</span></span>

<span data-ttu-id="2cc2d-134">Exchange Server 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-134">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="2cc2d-135">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

