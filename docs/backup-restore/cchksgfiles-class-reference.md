---
title: Referencia de clase función cchksgfiles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Busque información de referencia para la API de CHKSGFILES en Exchange 2013.
ms.openlocfilehash: 38b1f2c900767c22594636f0c6ddf4855961aec4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526735"
---
# <a name="cchksgfiles-class-reference"></a><span data-ttu-id="c296b-103">Referencia de clase función cchksgfiles</span><span class="sxs-lookup"><span data-stu-id="c296b-103">CChkSGFiles class reference</span></span>

<span data-ttu-id="c296b-104">Busque información de referencia para la API de CHKSGFILES en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c296b-104">Find reference information for the CHKSGFILES API in Exchange 2013.</span></span>
  
<span data-ttu-id="c296b-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c296b-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="c296b-106">La API CHKSGFILES permite que las aplicaciones de copia de seguridad y restauración comprueben la integridad de las bases de datos y los archivos de registro de transacciones de Exchange Server 2013 mediante programación.</span><span class="sxs-lookup"><span data-stu-id="c296b-106">The CHKSGFILES API enables backup and restore applications to verify the integrity of Exchange Server 2013 transaction log files and databases programmatically.</span></span> <span data-ttu-id="c296b-107">Puede usar esta API en las aplicaciones de copia de seguridad y restauración que usan el servicio de instantáneas de volumen (VSS).</span><span class="sxs-lookup"><span data-stu-id="c296b-107">You can use this API in backup and restore applications that use the Volume Shadow Copy Service (VSS).</span></span>
  
> [!NOTE]
> <span data-ttu-id="c296b-108">Los grupos de almacenamiento no están disponibles en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c296b-108">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="c296b-109">La compatibilidad con grupos de almacenamiento se ha quitado de las versiones de Exchange a partir de Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c296b-109">Support for storage groups was removed from versions of Exchange starting with Exchange Server 2010.</span></span> <span data-ttu-id="c296b-110">Para la compatibilidad con bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange 2010, la API CHKSGFILES permite especificar grupos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c296b-110">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="c296b-111">Cuando ejecuta CHKSGFILES en bases de datos de Exchange 2013, debe establecer los parámetros que especifican un identificador de grupo de almacenamiento en una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c296b-111">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
## <a name="file-location"></a><span data-ttu-id="c296b-112">Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="c296b-112">File location</span></span>
<span data-ttu-id="c296b-113"><a name="bk_fileslocation"> </a></span><span class="sxs-lookup"><span data-stu-id="c296b-113"><a name="bk_fileslocation"> </a></span></span>

<span data-ttu-id="c296b-114">La API CHKSGFILES se incluye como parte de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c296b-114">The CHKSGFILES API ships as part of Exchange 2013.</span></span> <span data-ttu-id="c296b-115">Puede usar esta API en un equipo que tenga instalado el rol de servidor buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c296b-115">You can use this API on a computer that has the Mailbox server role installed.</span></span> 
  
<span data-ttu-id="c296b-116">De forma predeterminada, la DLL CHKSGFILES se instala en el directorio C:\Program Files\Microsoft\Exchange\V15\Bin.</span><span class="sxs-lookup"><span data-stu-id="c296b-116">By default, the CHKSGFILES DLL is installed in the C:\Program Files\Microsoft\Exchange\V15\Bin directory.</span></span>
  
<span data-ttu-id="c296b-117">Exchange 2013 incluye solo una versión de 64 bits (amd64) de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="c296b-117">Exchange 2013 includes only a 64-bit (amd64) version of the CHKSGFILES API.</span></span> 
  
<span data-ttu-id="c296b-118">Puede descargar un archivo. zip que incluya la biblioteca CHKSGFILE. lib y los archivos de encabezado CHKSGFILES. HXX para usarlos en la aplicación personalizada desde el [centro de descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=36802).</span><span class="sxs-lookup"><span data-stu-id="c296b-118">You can download a .zip file that includes the CHKSGFILE.lib library and CHKSGFILES.hxx header files for use in your custom application from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802).</span></span>
  
## <a name="development-languages"></a><span data-ttu-id="c296b-119">Lenguajes de desarrollo</span><span class="sxs-lookup"><span data-stu-id="c296b-119">Development languages</span></span>
<span data-ttu-id="c296b-120"><a name="bk_developmentlanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="c296b-120"><a name="bk_developmentlanguages"> </a></span></span>

<span data-ttu-id="c296b-121">La API de CHKSGFILES está pensada para usarse con versiones de Visual Studio que comienzan con Visual Studio 2005 en C/C++ nativo.</span><span class="sxs-lookup"><span data-stu-id="c296b-121">The CHKSGFILES API is intended for use with versions of Visual Studio starting with Visual Studio 2005 in native C/C++.</span></span> <span data-ttu-id="c296b-122">La API de CHKSGFILES no está pensada para su uso en código administrado.</span><span class="sxs-lookup"><span data-stu-id="c296b-122">The CHKSGFILES API is not intended for use in managed code.</span></span> <span data-ttu-id="c296b-123">Aunque se puede crear un ensamblado de interoperabilidad COM con CHKSGFILES, no se incluye un ensamblado de interoperabilidad COM compatible con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c296b-123">Although you can create a COM Interop assembly with CHKSGFILES, we do not ship a supported COM Interop assembly with Exchange 2013.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="c296b-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c296b-124">In this section</span></span>
<span data-ttu-id="c296b-125"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="c296b-125"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="c296b-126">Función función cchksgfiles. CMaxDbPerSG</span><span class="sxs-lookup"><span data-stu-id="c296b-126">CChkSGFiles.CMaxDbPerSG function</span></span>](cchksgfiles-cmaxdbpersg-function.md)
    
- [<span data-ttu-id="c296b-127">Función función cchksgfiles. Delete</span><span class="sxs-lookup"><span data-stu-id="c296b-127">CChkSGFiles.Delete function</span></span>](cchksgfiles-delete-function.md)
    
- [<span data-ttu-id="c296b-128">Enumeración función cchksgfiles. ERR</span><span class="sxs-lookup"><span data-stu-id="c296b-128">CChkSGFiles.ERR enumeration</span></span>](cchksgfiles-err-enumeration.md)
    
- [<span data-ttu-id="c296b-129">Función función cchksgfiles. ErrCheckDbHeaders</span><span class="sxs-lookup"><span data-stu-id="c296b-129">CChkSGFiles.ErrCheckDbHeaders function</span></span>](cchksgfiles-errcheckdbheaders-function.md)
    
- [<span data-ttu-id="c296b-130">Función función cchksgfiles. ErrCheckDbPages</span><span class="sxs-lookup"><span data-stu-id="c296b-130">CChkSGFiles.ErrCheckDbPages function</span></span>](cchksgfiles-errcheckdbpages-function.md)
    
- [<span data-ttu-id="c296b-131">Función función cchksgfiles. ErrCheckLogs</span><span class="sxs-lookup"><span data-stu-id="c296b-131">CChkSGFiles.ErrCheckLogs function</span></span>](cchksgfiles-errchecklogs-function.md)
    
- [<span data-ttu-id="c296b-132">Función función cchksgfiles. ErrGetHeader (reservada)</span><span class="sxs-lookup"><span data-stu-id="c296b-132">CChkSGFiles.ErrGetHeader function (reserved)</span></span>](cchksgfiles-errgetheader-function-reserved.md)
    
- [<span data-ttu-id="c296b-133">Función función cchksgfiles. ErrInit</span><span class="sxs-lookup"><span data-stu-id="c296b-133">CChkSGFiles.ErrInit function</span></span>](cchksgfiles-errinit-function.md)
    
- [<span data-ttu-id="c296b-134">Función función cchksgfiles. ErrTerm</span><span class="sxs-lookup"><span data-stu-id="c296b-134">CChkSGFiles.ErrTerm function</span></span>](cchksgfiles-errterm-function.md)
    
- [<span data-ttu-id="c296b-135">Enumeración función cchksgfiles. iDbInvalid</span><span class="sxs-lookup"><span data-stu-id="c296b-135">CChkSGFiles.iDbInvalid enumeration</span></span>](cchksgfiles-idbinvalid-enumeration.md)
    
- [<span data-ttu-id="c296b-136">Función función cchksgfiles. New</span><span class="sxs-lookup"><span data-stu-id="c296b-136">CChkSGFiles.New function</span></span>](cchksgfiles-new-function.md)
    
- [<span data-ttu-id="c296b-137">Enumeración función cchksgfiles. NO_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c296b-137">CChkSGFiles.NO_FLAGS enumeration</span></span>](cchksgfiles-no_flags-enumeration.md)
    
- [<span data-ttu-id="c296b-138">Struct función cchksgfiles. PAGE_INFO</span><span class="sxs-lookup"><span data-stu-id="c296b-138">CChkSGFiles.PAGE_INFO struct</span></span>](cchksgfiles-page_info-struct.md)
    
- [<span data-ttu-id="c296b-139">Función función cchksgfiles. PgnoFromFileOffset</span><span class="sxs-lookup"><span data-stu-id="c296b-139">CChkSGFiles.PgnoFromFileOffset function</span></span>](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a><span data-ttu-id="c296b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c296b-140">See also</span></span>

- [<span data-ttu-id="c296b-141">Desarrollo de Exchange y Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c296b-141">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)
- [<span data-ttu-id="c296b-142">Copia de seguridad, restauración y recuperación ante desastres</span><span class="sxs-lookup"><span data-stu-id="c296b-142">Backup, Restore, and Disaster Recovery</span></span>](https://technet.microsoft.com/library/dd876874)
    

