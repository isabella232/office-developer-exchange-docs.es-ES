---
title: Estructura de CChkSGFiles.PAGE_INFO
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: fa66d253b4fc6bd5c29a39c5323f59bf323a906f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763917"
---
# <a name="cchksgfilespageinfo-struct"></a><span data-ttu-id="0096b-103">Estructura de CChkSGFiles.PAGE_INFO</span><span class="sxs-lookup"><span data-stu-id="0096b-103">CChkSGFiles.PAGE_INFO struct</span></span>

<span data-ttu-id="0096b-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="0096b-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="0096b-105">Contiene la información de una página de base de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0096b-105">Holds information for an Exchange database page.</span></span> <span data-ttu-id="0096b-106">Esta estructura se utiliza con la función **ErrCheckDbPages** .</span><span class="sxs-lookup"><span data-stu-id="0096b-106">This structure is used with the **ErrCheckDbPages** function.</span></span> 
  
```cs
Struct PAGE_INFO  
{
        ULONGulPgno;
        BOOLfPageIsInitialized : 1;
        BOOLfCorrectableError : 1;
        ULONGLONGchecksumActual;
        ULONGLONGchecksumExpected;
        ULONGLONGdbTime;
        ULONGLONGchecksumPageStructure;
        ULONGLONGulFlags;
}

```

## <a name="members"></a><span data-ttu-id="0096b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0096b-107">Members</span></span>

### <a name="ulpgno"></a><span data-ttu-id="0096b-108">ulPgNo</span><span class="sxs-lookup"><span data-stu-id="0096b-108">ulPgNo</span></span>
  
<span data-ttu-id="0096b-109">Unsigned Long.</span><span class="sxs-lookup"><span data-stu-id="0096b-109">Unsigned Long.</span></span> <span data-ttu-id="0096b-110">Número de página lógica de la página de la base de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="0096b-110">Logical page number of the database page to be checked.</span></span> <span data-ttu-id="0096b-111">Este valor debe establecerse antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="0096b-111">This value must be set before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="0096b-112">Si la aplicación está leyendo el archivo en función de los desplazamientos de archivo y, por lo tanto, debe asignar los desplazamientos de archivo a los números de página lógica, encontrará el método **PgnoFromFileOffset** útil para determinar el valor para este campo.</span><span class="sxs-lookup"><span data-stu-id="0096b-112">If the application is reading the file based on file offsets, and must therefore map those file offsets to logical page numbers, you will find the **PgnoFromFileOffset** method useful to determine the value for this field.</span></span> <span data-ttu-id="0096b-113">**ErrCheckDbPages** no modifique este valor.</span><span class="sxs-lookup"><span data-stu-id="0096b-113">**ErrCheckDbPages** does not modify this value.</span></span> 
    
### <a name="fpageisinitialized"></a><span data-ttu-id="0096b-114">fPageIsInitialized</span><span class="sxs-lookup"><span data-stu-id="0096b-114">fPageIsInitialized</span></span> 
  
<span data-ttu-id="0096b-115">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="0096b-115">Boolean.</span></span> <span data-ttu-id="0096b-116">Un valor de TRUE indica que la página de la base de datos contiene datos.</span><span class="sxs-lookup"><span data-stu-id="0096b-116">A value of TRUE indicates that the database page contains data.</span></span> <span data-ttu-id="0096b-117">Un valor de FALSE indica que la página contiene sólo ceros.</span><span class="sxs-lookup"><span data-stu-id="0096b-117">A value of FALSE indicates that the page contains only zeros.</span></span> <span data-ttu-id="0096b-118">**ErrCheckDbPages** establece este valor.</span><span class="sxs-lookup"><span data-stu-id="0096b-118">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="fcorrectableerror"></a><span data-ttu-id="0096b-119">fCorrectableError</span><span class="sxs-lookup"><span data-stu-id="0096b-119">fCorrectableError</span></span>
  
<span data-ttu-id="0096b-120">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="0096b-120">Boolean.</span></span> <span data-ttu-id="0096b-121">Un valor de TRUE indica que se ha producido un error de coincidencia de suma de comprobación detectado en la página de la base de datos, pero que es un error puede corregir.</span><span class="sxs-lookup"><span data-stu-id="0096b-121">A value of TRUE indicates that there was a checksum mismatch detected in the database page, but that it is a correctable error.</span></span> <span data-ttu-id="0096b-122">**ErrCheckDbPages** establece este valor.</span><span class="sxs-lookup"><span data-stu-id="0096b-122">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumactual"></a><span data-ttu-id="0096b-123">checksumActual</span><span class="sxs-lookup"><span data-stu-id="0096b-123">checksumActual</span></span>
  
<span data-ttu-id="0096b-124">Entero sin signo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0096b-124">Unsigned 64-bit integer.</span></span> <span data-ttu-id="0096b-125">Indica el valor de suma de comprobación almacenado en la base de datos para esta página lógica.</span><span class="sxs-lookup"><span data-stu-id="0096b-125">Indicates the checksum value stored in the database for this logical page.</span></span> <span data-ttu-id="0096b-126">**ErrCheckDbPages** establece este valor.</span><span class="sxs-lookup"><span data-stu-id="0096b-126">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumexpected"></a><span data-ttu-id="0096b-127">checksumExpected</span><span class="sxs-lookup"><span data-stu-id="0096b-127">checksumExpected</span></span>
  
<span data-ttu-id="0096b-128">Entero sin signo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0096b-128">Unsigned 64-bit integer.</span></span> <span data-ttu-id="0096b-129">Éste es el valor de suma de comprobación esperada que se calcula para la página de la base de datos; se establece mediante **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="0096b-129">This is the expected checksum value that is calculated for the database page; it is set by **ErrCheckDbPages**.</span></span> <span data-ttu-id="0096b-130">Si este valor es diferente de la que se almacenan en la página de la base de datos (es decir, el valor devuelto en **checksumActual**), **ErrCheckDbPages** que le indicará que se ha encontrado un error en esta página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0096b-130">If this value is different from that stored on the database page (that is, the value returned in **checksumActual**), **ErrCheckDbPages** will indicate that an error was found on this database page.</span></span> 
    
### <a name="dbtime"></a><span data-ttu-id="0096b-131">dbTime</span><span class="sxs-lookup"><span data-stu-id="0096b-131">dbTime</span></span>
  
<span data-ttu-id="0096b-132">Entero sin signo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0096b-132">Unsigned 64-bit integer.</span></span> <span data-ttu-id="0096b-133">**ErrCheckDbPages** establece a este miembro en la marca de tiempo en la página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0096b-133">**ErrCheckDbPages** sets this member to the timestamp on the database page.</span></span> 
    
### <a name="checksumpagestructure"></a><span data-ttu-id="0096b-134">checksumPageStructure</span><span class="sxs-lookup"><span data-stu-id="0096b-134">checksumPageStructure</span></span> 
  
<span data-ttu-id="0096b-135">Entero sin signo de 64-bt.</span><span class="sxs-lookup"><span data-stu-id="0096b-135">Unsigned 64-bt integer.</span></span> <span data-ttu-id="0096b-136">**ErrCheckDbPages** establece a este miembro en el valor calculado de la suma de comprobación del contenido de la página excluidos los datos que no es necesarios cuando la determinación de la equivalencia de página lógica.</span><span class="sxs-lookup"><span data-stu-id="0096b-136">**ErrCheckDbPages** sets this member to the calculated checksum value of the contents of the page excluding data which is unnecessary when determining the logical page equivalence.</span></span> <span data-ttu-id="0096b-137">Por ejemplo, es necesario tener en cuenta los valores de datos en el espacio de página de base de datos no usados.</span><span class="sxs-lookup"><span data-stu-id="0096b-137">For example, it is unnecessary to consider the data values in unused database page space.</span></span> <span data-ttu-id="0096b-138">Este miembro sólo es válida si los valores de **checksumActual** y **checksumExpected** son iguales a los otros.</span><span class="sxs-lookup"><span data-stu-id="0096b-138">This member is only valid if the **checksumActual**  and  **checksumExpected**  values are equal to each other.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="0096b-139">ulFlags</span><span class="sxs-lookup"><span data-stu-id="0096b-139">ulFlags</span></span>
  
<span data-ttu-id="0096b-140">Entero sin signo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0096b-140">Unsigned 64-bit integer.</span></span> <span data-ttu-id="0096b-141">Reservado para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="0096b-141">Reserved for future use.</span></span> <span data-ttu-id="0096b-142">El valor de este campo debe establecerse en 0 (cero) antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="0096b-142">The value of this field must be set to 0 (zero) before calling **ErrCheckDbPages**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0096b-143">Notas</span><span class="sxs-lookup"><span data-stu-id="0096b-143">Remarks</span></span>

<span data-ttu-id="0096b-144">Cuando se llama a la función **ErrCheckDbPages** , el parámetro **rgPageInfo** es una matriz de **página\_INFO** estructuras.</span><span class="sxs-lookup"><span data-stu-id="0096b-144">When calling the **ErrCheckDbPages** function, the **rgPageInfo**  parameter is an array of **PAGE\_INFO** structures.</span></span> <span data-ttu-id="0096b-145">Debe ser uno **página\_INFO** estructura para cada página de la base de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="0096b-145">There must be one **PAGE\_INFO** structure for each database page to be checked.</span></span> 
  
<span data-ttu-id="0096b-146">La aplicación debe establecer al miembro **ulPgno** en el valor correcto y también debe establecer la del miembro **ulFlags** en 0 (cero) antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="0096b-146">The application must set the **ulPgno**  member to the proper value, and must also set the  **ulFlags**  member to 0 (zero) before calling **ErrCheckDbPages**.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="0096b-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0096b-147">Requirements</span></span>

<span data-ttu-id="0096b-148">Exchange Server 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="0096b-148">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="0096b-149">La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="0096b-149">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

