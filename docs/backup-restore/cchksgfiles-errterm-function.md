---
title: Función función cchksgfiles. ErrTerm
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 'Última modificación: 25 de febrero de 2013'
ms.openlocfilehash: 12b07fba69054d327c7250bbf83e4c77016e8b3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466202"
---
# <a name="cchksgfileserrterm-function"></a><span data-ttu-id="680d7-103">Función función cchksgfiles. ErrTerm</span><span class="sxs-lookup"><span data-stu-id="680d7-103">CChkSGFiles.ErrTerm function</span></span>
  
<span data-ttu-id="680d7-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="680d7-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="680d7-105">Proporciona un estado general de la comprobación de registro y base de datos, que indica si se han comprobado correctamente todas las páginas de base de datos y los registros.</span><span class="sxs-lookup"><span data-stu-id="680d7-105">Provides an overall status of the database and log verification, which indicates whether all the database pages and logs were successfully verified.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="680d7-106">Los grupos de almacenamiento no están disponibles en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="680d7-106">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="680d7-107">Para la compatibilidad con bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange Server 2010, la API CHKSGFILES permite especificar grupos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="680d7-107">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange Server 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="680d7-108">Cuando ejecuta CHKSGFILES en bases de datos de Exchange 2013, debe establecer los parámetros que especifican un identificador de grupo de almacenamiento en una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="680d7-108">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="680d7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="680d7-109">Parameters</span></span>

### <a name="ulflags"></a><span data-ttu-id="680d7-110">ulFlags</span><span class="sxs-lookup"><span data-stu-id="680d7-110">ulFlags</span></span>
  
<span data-ttu-id="680d7-111">Parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="680d7-111">Optional input parameter.</span></span> <span data-ttu-id="680d7-112">Este valor se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="680d7-112">This value is reserved for future use.</span></span> <span data-ttu-id="680d7-113">El valor que pasa este parámetro debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="680d7-113">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="680d7-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="680d7-114">Return value</span></span>

<span data-ttu-id="680d7-115">Un código de error de la enumeración [Err](cchksgfiles-err-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="680d7-115">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="680d7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="680d7-116">Remarks</span></span>

<span data-ttu-id="680d7-117">El objeto **función cchksgfiles** determina si se han comprobado realmente todas las bases de datos registradas con la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="680d7-117">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="680d7-118">Este objeto usa la función **ErrCheckDbPages** para comprobar que se ha comprobado realmente el mismo número de páginas de base de datos identificadas por la función **ErrCheckDbHeaders** .</span><span class="sxs-lookup"><span data-stu-id="680d7-118">This object uses the **ErrCheckDbPages** function to verify that the same number of database pages identified by the **ErrCheckDbHeaders** function were actually verified.</span></span> <span data-ttu-id="680d7-119">Si el número correcto de páginas de cada base de datos no se comprueba correctamente, la función **ErrTerm** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="680d7-119">If the correct number of pages in each database are not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="680d7-120">Si el número de páginas de base de datos que se comprueba con **ErrCheckDbPages** es menor que el indicado por **ErrCheckDbHeaders**, esta función genera un error en el registro de eventos de Windows y **ErrTerm** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="680d7-120">If the number of database pages checked with **ErrCheckDbPages** is less than that indicated by **ErrCheckDbHeaders**, this function creates an error in the Windows Event log, and **ErrTerm** returns an error.</span></span> 
  
<span data-ttu-id="680d7-121">Si el número de páginas de base de datos que se comprueba con **ErrCheckDbPages** es superior al indicado por **ErrCheckDbHeaders**, esta función crea una advertencia en el registro de eventos de Windows para indicar que es posible que la aplicación no Compruebe innecesariamente algunas páginas de base de datos más de una vez.</span><span class="sxs-lookup"><span data-stu-id="680d7-121">If the number of database pages checked with **ErrCheckDbPages** is greater than that indicated by **ErrCheckDbHeaders**, this function creates a warning in the Windows Event log to indicate that the application might be unnecessarily checking some database pages more than once.</span></span> <span data-ttu-id="680d7-122">En este caso, sin embargo, la función **ErrTerm** se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="680d7-122">In this case, however, the **ErrTerm** function succeeds.</span></span> 
  
<span data-ttu-id="680d7-123">El objeto **función cchksgfiles** también determina si se han comprobado realmente los archivos de registro registrados con **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="680d7-123">The **CChkSGFiles** object also determines whether the log files registered with **ErrInit** were actually checked.</span></span> <span data-ttu-id="680d7-124">Si no todos los registros se comprobó correctamente, la función **ErrTerm** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="680d7-124">If not all the logs were successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="680d7-125">Cuando **ErrTerm** devuelve un error, será el primer error que encuentre, aunque comprueba el estado de comprobación de todas las bases de datos registradas con **ErrInit**.</span><span class="sxs-lookup"><span data-stu-id="680d7-125">When **ErrTerm** returns an error, it will be the first error it finds, even though it checks the verification status for all databases registered with **ErrInit**.</span></span>
  
<span data-ttu-id="680d7-126">Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la función **ErrTerm** en la parte de subproceso único de la aplicación y puede llamarla no más de una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="680d7-126">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrTerm** function in the single-threaded portion of the application, and you can call it no more than once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="680d7-127">Requirements</span><span class="sxs-lookup"><span data-stu-id="680d7-127">Requirements</span></span>

<span data-ttu-id="680d7-128">Exchange 2013 solo incluye una versión de 64 bits de CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="680d7-128">Exchange 2013 only includes a 64-bit version of CHKSGFILES.</span></span>
  
<span data-ttu-id="680d7-129">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="680d7-129">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

