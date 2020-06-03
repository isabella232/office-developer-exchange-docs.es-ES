---
title: Struct función cchksgfiles. PAGE_INFO
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
ms.openlocfilehash: 5ec9f4303b26ea95b125adac6943945ae1276439
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456342"
---
# <a name="cchksgfilespage_info-struct"></a><span data-ttu-id="50b83-103">Struct función cchksgfiles. PAGE_INFO</span><span class="sxs-lookup"><span data-stu-id="50b83-103">CChkSGFiles.PAGE_INFO struct</span></span>

<span data-ttu-id="50b83-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b83-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="50b83-105">Contiene información para una página de base de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="50b83-105">Holds information for an Exchange database page.</span></span> <span data-ttu-id="50b83-106">Esta estructura se usa con la función **ErrCheckDbPages** .</span><span class="sxs-lookup"><span data-stu-id="50b83-106">This structure is used with the **ErrCheckDbPages** function.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="50b83-107">Members</span><span class="sxs-lookup"><span data-stu-id="50b83-107">Members</span></span>

### <a name="ulpgno"></a><span data-ttu-id="50b83-108">ulPgNo</span><span class="sxs-lookup"><span data-stu-id="50b83-108">ulPgNo</span></span>
  
<span data-ttu-id="50b83-109">Unsigned Long.</span><span class="sxs-lookup"><span data-stu-id="50b83-109">Unsigned Long.</span></span> <span data-ttu-id="50b83-110">Número de página lógica de la página de base de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="50b83-110">Logical page number of the database page to be checked.</span></span> <span data-ttu-id="50b83-111">Este valor debe establecerse antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="50b83-111">This value must be set before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="50b83-112">Si la aplicación está leyendo el archivo en función de los desplazamientos de los archivos y, por tanto, debe asignar los desplazamientos de estos archivos a los números de página lógica, el método **PgnoFromFileOffset** le resultará útil para determinar el valor de este campo.</span><span class="sxs-lookup"><span data-stu-id="50b83-112">If the application is reading the file based on file offsets, and must therefore map those file offsets to logical page numbers, you will find the **PgnoFromFileOffset** method useful to determine the value for this field.</span></span> <span data-ttu-id="50b83-113">**ErrCheckDbPages** no modifica este valor.</span><span class="sxs-lookup"><span data-stu-id="50b83-113">**ErrCheckDbPages** does not modify this value.</span></span> 
    
### <a name="fpageisinitialized"></a><span data-ttu-id="50b83-114">fPageIsInitialized</span><span class="sxs-lookup"><span data-stu-id="50b83-114">fPageIsInitialized</span></span> 
  
<span data-ttu-id="50b83-115">Tipo.</span><span class="sxs-lookup"><span data-stu-id="50b83-115">Boolean.</span></span> <span data-ttu-id="50b83-116">Un valor de TRUE indica que la página de base de datos contiene datos.</span><span class="sxs-lookup"><span data-stu-id="50b83-116">A value of TRUE indicates that the database page contains data.</span></span> <span data-ttu-id="50b83-117">Un valor de FALSE indica que la página contiene solo ceros.</span><span class="sxs-lookup"><span data-stu-id="50b83-117">A value of FALSE indicates that the page contains only zeros.</span></span> <span data-ttu-id="50b83-118">**ErrCheckDbPages** establece este valor.</span><span class="sxs-lookup"><span data-stu-id="50b83-118">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="fcorrectableerror"></a><span data-ttu-id="50b83-119">fCorrectableError</span><span class="sxs-lookup"><span data-stu-id="50b83-119">fCorrectableError</span></span>
  
<span data-ttu-id="50b83-120">Tipo.</span><span class="sxs-lookup"><span data-stu-id="50b83-120">Boolean.</span></span> <span data-ttu-id="50b83-121">Un valor de TRUE indica que se detectó un error de coincidencia de suma de comprobación en la página de la base de datos, pero es un error corregible.</span><span class="sxs-lookup"><span data-stu-id="50b83-121">A value of TRUE indicates that there was a checksum mismatch detected in the database page, but that it is a correctable error.</span></span> <span data-ttu-id="50b83-122">**ErrCheckDbPages** establece este valor.</span><span class="sxs-lookup"><span data-stu-id="50b83-122">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumactual"></a><span data-ttu-id="50b83-123">checksumActual</span><span class="sxs-lookup"><span data-stu-id="50b83-123">checksumActual</span></span>
  
<span data-ttu-id="50b83-124">Entero de bit de bit 64 sin signo.</span><span class="sxs-lookup"><span data-stu-id="50b83-124">Unsigned 64-bit integer.</span></span> <span data-ttu-id="50b83-125">Indica el valor de la suma de comprobación que se almacena en la base de datos para esta página lógica.</span><span class="sxs-lookup"><span data-stu-id="50b83-125">Indicates the checksum value stored in the database for this logical page.</span></span> <span data-ttu-id="50b83-126">**ErrCheckDbPages** establece este valor.</span><span class="sxs-lookup"><span data-stu-id="50b83-126">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumexpected"></a><span data-ttu-id="50b83-127">checksumExpected</span><span class="sxs-lookup"><span data-stu-id="50b83-127">checksumExpected</span></span>
  
<span data-ttu-id="50b83-128">Entero de bit de bit 64 sin signo.</span><span class="sxs-lookup"><span data-stu-id="50b83-128">Unsigned 64-bit integer.</span></span> <span data-ttu-id="50b83-129">Se trata del valor de suma de comprobación esperado que se calcula para la página de la base de datos; se establece en **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="50b83-129">This is the expected checksum value that is calculated for the database page; it is set by **ErrCheckDbPages**.</span></span> <span data-ttu-id="50b83-130">Si este valor es distinto del que se almacena en la página de la base de datos (es decir, el valor devuelto en **checksumActual**), **ErrCheckDbPages** indicará que se encontró un error en esta página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="50b83-130">If this value is different from that stored on the database page (that is, the value returned in **checksumActual**), **ErrCheckDbPages** will indicate that an error was found on this database page.</span></span> 
    
### <a name="dbtime"></a><span data-ttu-id="50b83-131">dbTime</span><span class="sxs-lookup"><span data-stu-id="50b83-131">dbTime</span></span>
  
<span data-ttu-id="50b83-132">Entero de bit de bit 64 sin signo.</span><span class="sxs-lookup"><span data-stu-id="50b83-132">Unsigned 64-bit integer.</span></span> <span data-ttu-id="50b83-133">**ErrCheckDbPages** establece este miembro en la marca de hora de la página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="50b83-133">**ErrCheckDbPages** sets this member to the timestamp on the database page.</span></span> 
    
### <a name="checksumpagestructure"></a><span data-ttu-id="50b83-134">checksumPageStructure</span><span class="sxs-lookup"><span data-stu-id="50b83-134">checksumPageStructure</span></span> 
  
<span data-ttu-id="50b83-135">Entero de 64-BT sin signo.</span><span class="sxs-lookup"><span data-stu-id="50b83-135">Unsigned 64-bt integer.</span></span> <span data-ttu-id="50b83-136">**ErrCheckDbPages** establece este miembro en el valor de suma de comprobación calculado del contenido de la página, excepto los datos que no son necesarios para determinar la equivalencia de página lógica.</span><span class="sxs-lookup"><span data-stu-id="50b83-136">**ErrCheckDbPages** sets this member to the calculated checksum value of the contents of the page excluding data which is unnecessary when determining the logical page equivalence.</span></span> <span data-ttu-id="50b83-137">Por ejemplo, no es necesario tener en cuenta los valores de datos en un espacio de páginas de base de datos sin usar.</span><span class="sxs-lookup"><span data-stu-id="50b83-137">For example, it is unnecessary to consider the data values in unused database page space.</span></span> <span data-ttu-id="50b83-138">Este miembro sólo es válido si los valores **checksumActual** y **checksumExpected** son iguales entre sí.</span><span class="sxs-lookup"><span data-stu-id="50b83-138">This member is only valid if the **checksumActual**  and  **checksumExpected**  values are equal to each other.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="50b83-139">ulFlags</span><span class="sxs-lookup"><span data-stu-id="50b83-139">ulFlags</span></span>
  
<span data-ttu-id="50b83-140">Entero de bit de bit 64 sin signo.</span><span class="sxs-lookup"><span data-stu-id="50b83-140">Unsigned 64-bit integer.</span></span> <span data-ttu-id="50b83-141">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="50b83-141">Reserved for future use.</span></span> <span data-ttu-id="50b83-142">El valor de este campo debe establecerse en 0 (cero) antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="50b83-142">The value of this field must be set to 0 (zero) before calling **ErrCheckDbPages**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50b83-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50b83-143">Remarks</span></span>

<span data-ttu-id="50b83-144">Cuando se llama a la función **ErrCheckDbPages** , el parámetro **rgPageInfo** es una matriz de las estructuras de \*\* \_ información de página\*\* .</span><span class="sxs-lookup"><span data-stu-id="50b83-144">When calling the **ErrCheckDbPages** function, the **rgPageInfo**  parameter is an array of **PAGE\_INFO** structures.</span></span> <span data-ttu-id="50b83-145">Debe haber una estructura **de \_ información de página** por cada página de base de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="50b83-145">There must be one **PAGE\_INFO** structure for each database page to be checked.</span></span> 
  
<span data-ttu-id="50b83-146">La aplicación debe establecer el miembro **ulPgno** en el valor correcto y también debe establecer el miembro **ulFlags** en 0 (cero) antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="50b83-146">The application must set the **ulPgno**  member to the proper value, and must also set the  **ulFlags**  member to 0 (zero) before calling **ErrCheckDbPages**.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="50b83-147">Requirements</span><span class="sxs-lookup"><span data-stu-id="50b83-147">Requirements</span></span>

<span data-ttu-id="50b83-148">Exchange Server 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="50b83-148">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="50b83-149">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="50b83-149">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

