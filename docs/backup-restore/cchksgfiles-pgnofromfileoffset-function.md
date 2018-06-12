---
title: CChkSGFiles.PgnoFromFileOffset (función)
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: d42ba7c8178c6fccdddec0b5da88a972f51184c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762985"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a><span data-ttu-id="81ebb-103">CChkSGFiles.PgnoFromFileOffset (función)</span><span class="sxs-lookup"><span data-stu-id="81ebb-103">CChkSGFiles.PgnoFromFileOffset function</span></span>

<span data-ttu-id="81ebb-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="81ebb-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="81ebb-105">Devuelve el número de página de base de datos lógica que corresponde al índice especificado de bytes en el archivo de base de datos físico.</span><span class="sxs-lookup"><span data-stu-id="81ebb-105">Returns the logical database page number that corresponds to the specified byte index in the physical database file.</span></span> <span data-ttu-id="81ebb-106">Si el desplazamiento de archivo no es válido, o si no se ha llamado a la función **ErrCheckDbHeaders** para las bases de datos, esta función devuelve 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="81ebb-106">If the file offset is invalid, or if the **ErrCheckDbHeaders** function has not been called for the databases, this function returns 0 (zero).</span></span> 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a><span data-ttu-id="81ebb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81ebb-107">Parameters</span></span>

### <a name="ibfileoffset"></a><span data-ttu-id="81ebb-108">ibFileOffset</span><span class="sxs-lookup"><span data-stu-id="81ebb-108">ibFileOffset</span></span>
  
<span data-ttu-id="81ebb-109">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="81ebb-109">Input parameter.</span></span> <span data-ttu-id="81ebb-110">Especifica el desplazamiento en un archivo de base de datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="81ebb-110">The offset into a database file, in bytes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81ebb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81ebb-111">Return value</span></span>

<span data-ttu-id="81ebb-112">Número de página lógica del archivo de base de datos que incluye el desplazamiento especificado.</span><span class="sxs-lookup"><span data-stu-id="81ebb-112">The database file's logical page number that includes the specified offset.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81ebb-113">Notas</span><span class="sxs-lookup"><span data-stu-id="81ebb-113">Remarks</span></span>

<span data-ttu-id="81ebb-114">Si el parámetro **ibFileOffset** no es válido, la función **PgnoFromFileOffset** devuelve 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="81ebb-114">If the **ibFileOffset** parameter is invalid, the **PgnoFromFileOffset** function returns 0 (zero).</span></span> 
  
<span data-ttu-id="81ebb-115">**PgnoFromFileOffset** también devuelve 0 (cero) si no ha llamado a la función **ErrCheckDbHeaders** en la instancia de **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="81ebb-115">**PgnoFromFileOffset** also returns 0 (zero) if you haven't called the **ErrCheckDbHeaders** function on the **CCheckSGFiles** instance.</span></span> <span data-ttu-id="81ebb-116">Se debe llamar a **ErrCheckDbHeaders** para inicializar el tamaño de página de la base de datos y el número de páginas asignadas a los encabezados de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="81ebb-116">You must call **ErrCheckDbHeaders** to initialize the database page size and number of pages allocated to database headers.</span></span> 
  
<span data-ttu-id="81ebb-117">Debe usar **PgnoFromFileOffset** para rellenar la **página\_INFO** elementos en la preparación para llamar a **ErrCheckDbPages**de estructura.</span><span class="sxs-lookup"><span data-stu-id="81ebb-117">You should use **PgnoFromFileOffset** to fill in the **PAGE\_INFO** structure elements in preparation for calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="81ebb-118">El parámetro **rgPageInfo** para **ErrCheckDbPages** requiere que cada elemento de la matriz sea una estructura **PAGE_INFO** , con los valores de miembro **ulPgno** inicializado correctamente.</span><span class="sxs-lookup"><span data-stu-id="81ebb-118">The **rgPageInfo** parameter to **ErrCheckDbPages** requires that each element in the array be a **PAGE_INFO** structure, with the **ulPgno** member values correctly initialized.</span></span> 
  
<span data-ttu-id="81ebb-119">Si está utilizando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **PgnoFromFileOffset** en la parte de la aplicación multiproceso.</span><span class="sxs-lookup"><span data-stu-id="81ebb-119">If you're using CHKSGFILES in a multithreaded application, you can call the **PgnoFromFileOffset** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="81ebb-120">Tenga en cuenta que se haría normalmente llamar a esta función varias veces para cada base de datos está activado.</span><span class="sxs-lookup"><span data-stu-id="81ebb-120">Note that you would typically call this function multiple times for each database being checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="81ebb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81ebb-121">Requirements</span></span>

<span data-ttu-id="81ebb-122">Exchange Server 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="81ebb-122">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="81ebb-123">La cuenta que se ejecuta la aplicación debe tener permiso para los archivos de registro y base de datos que se va a revisar de lectura.</span><span class="sxs-lookup"><span data-stu-id="81ebb-123">The account that the application is running under must have read permission to the database and log files that are to be checked.</span></span>
  

