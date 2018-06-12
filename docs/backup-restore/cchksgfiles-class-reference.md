---
title: Referencia de clase CChkSGFiles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Busque información de referencia para la API CHKSGFILES en Exchange 2013.
ms.openlocfilehash: 583ac5e16ab60d119c3028bf81123e9f60a58ff4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762979"
---
# <a name="cchksgfiles-class-reference"></a><span data-ttu-id="c8125-103">Referencia de clase CChkSGFiles</span><span class="sxs-lookup"><span data-stu-id="c8125-103">CChkSGFiles class reference</span></span>

<span data-ttu-id="c8125-104">Busque información de referencia para la API CHKSGFILES en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c8125-104">Find reference information for the CHKSGFILES API in Exchange 2013.</span></span>
  
<span data-ttu-id="c8125-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8125-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="c8125-106">La API de CHKSGFILES permite a las aplicaciones de copia de seguridad y restauración comprobar la integridad de los archivos de registro de transacciones de Exchange Server 2013 y las bases de datos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="c8125-106">The CHKSGFILES API enables backup and restore applications to verify the integrity of Exchange Server 2013 transaction log files and databases programmatically.</span></span> <span data-ttu-id="c8125-107">Puede usar esta API en copia de seguridad y restauración de las aplicaciones que usan el servicio de instantáneas de volumen (VSS).</span><span class="sxs-lookup"><span data-stu-id="c8125-107">You can use this API in backup and restore applications that use the Volume Shadow Copy Service (VSS).</span></span>
  
> [!NOTE]
> <span data-ttu-id="c8125-108">Grupos de almacenamiento no están disponibles en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c8125-108">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="c8125-109">Compatibilidad con grupos de almacenamiento se ha quitado de las versiones de Exchange a partir de Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c8125-109">Support for storage groups was removed from versions of Exchange starting with Exchange Server 2010.</span></span> <span data-ttu-id="c8125-110">Para la compatibilidad con versiones anteriores con las bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange 2010, la API de CHKSGFILES permite especificar grupos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c8125-110">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="c8125-111">Cuando ejecuta CHKSGFILES frente a las bases de datos de Exchange 2013, debe establecer los parámetros que especifican un identificador de grupo de almacenamiento de información en una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c8125-111">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
## <a name="file-location"></a><span data-ttu-id="c8125-112">Ubicación de archivo</span><span class="sxs-lookup"><span data-stu-id="c8125-112">File location</span></span>
<span data-ttu-id="c8125-113"><a name="bk_fileslocation"> </a></span><span class="sxs-lookup"><span data-stu-id="c8125-113"></span></span>

<span data-ttu-id="c8125-114">La API CHKSGFILES se distribuye como parte de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c8125-114">The CHKSGFILES API ships as part of Exchange 2013.</span></span> <span data-ttu-id="c8125-115">Puede usar esta API en un equipo que tenga instalado el rol de servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c8125-115">You can use this API on a computer that has the Mailbox server role installed.</span></span> 
  
<span data-ttu-id="c8125-116">De forma predeterminada, la DLL de CHKSGFILES está instalada en el directorio C:\Program Files\Microsoft\Exchange\V15\Bin.</span><span class="sxs-lookup"><span data-stu-id="c8125-116">By default, the CHKSGFILES DLL is installed in the C:\Program Files\Microsoft\Exchange\V15\Bin directory.</span></span>
  
<span data-ttu-id="c8125-117">Exchange 2013 incluye sólo una versión de 64 bits (amd64) de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="c8125-117">Exchange 2013 includes only a 64-bit (amd64) version of the CHKSGFILES API.</span></span> 
  
<span data-ttu-id="c8125-118">Puede descargar un archivo .zip que incluye la biblioteca de CHKSGFILE.lib y los archivos de encabezado de CHKSGFILES.hxx para su uso en la aplicación personalizada desde el [Centro de descarga de Microsoft](http://www.microsoft.com/en-us/download/details.aspx?id=36802).</span><span class="sxs-lookup"><span data-stu-id="c8125-118">You can download a .zip file that includes the CHKSGFILE.lib library and CHKSGFILES.hxx header files for use in your custom application from the [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802).</span></span>
  
## <a name="development-languages"></a><span data-ttu-id="c8125-119">Lenguajes de desarrollo</span><span class="sxs-lookup"><span data-stu-id="c8125-119">Development languages</span></span>
<span data-ttu-id="c8125-120"><a name="bk_developmentlanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="c8125-120"></span></span>

<span data-ttu-id="c8125-121">La API CHKSGFILES está pensada para su uso con las versiones de Visual Studio desde Visual Studio 2005 en C o C++ nativo.</span><span class="sxs-lookup"><span data-stu-id="c8125-121">The CHKSGFILES API is intended for use with versions of Visual Studio starting with Visual Studio 2005 in native C/C++.</span></span> <span data-ttu-id="c8125-122">La API CHKSGFILES no está pensada para su uso en código administrado.</span><span class="sxs-lookup"><span data-stu-id="c8125-122">The CHKSGFILES API is not intended for use in managed code.</span></span> <span data-ttu-id="c8125-123">Aunque se puede crear un ensamblado de interoperabilidad COM con CHKSGFILES, no ofrecemos un ensamblado de interoperabilidad COM compatible con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c8125-123">Although you can create a COM Interop assembly with CHKSGFILES, we do not ship a supported COM Interop assembly with Exchange 2013.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="c8125-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c8125-124">In this section</span></span>
<span data-ttu-id="c8125-125"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="c8125-125"></span></span>

- [<span data-ttu-id="c8125-126">CChkSGFiles.CMaxDbPerSG (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-126">CChkSGFiles.CMaxDbPerSG function</span></span>](cchksgfiles-cmaxdbpersg-function.md)
    
- [<span data-ttu-id="c8125-127">CChkSGFiles.Delete (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-127">CChkSGFiles.Delete function</span></span>](cchksgfiles-delete-function.md)
    
- [<span data-ttu-id="c8125-128">CChkSGFiles.ERR (enumeración)</span><span class="sxs-lookup"><span data-stu-id="c8125-128">CChkSGFiles.ERR enumeration</span></span>](cchksgfiles-err-enumeration.md)
    
- [<span data-ttu-id="c8125-129">CChkSGFiles.ErrCheckDbHeaders (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-129">CChkSGFiles.ErrCheckDbHeaders function</span></span>](cchksgfiles-errcheckdbheaders-function.md)
    
- [<span data-ttu-id="c8125-130">CChkSGFiles.ErrCheckDbPages (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-130">CChkSGFiles.ErrCheckDbPages function</span></span>](cchksgfiles-errcheckdbpages-function.md)
    
- [<span data-ttu-id="c8125-131">CChkSGFiles.ErrCheckLogs (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-131">CChkSGFiles.ErrCheckLogs function</span></span>](cchksgfiles-errchecklogs-function.md)
    
- [<span data-ttu-id="c8125-132">Función CChkSGFiles.ErrGetHeader (reservado)</span><span class="sxs-lookup"><span data-stu-id="c8125-132">CChkSGFiles.ErrGetHeader function (reserved)</span></span>](cchksgfiles-errgetheader-function-reserved.md)
    
- [<span data-ttu-id="c8125-133">CChkSGFiles.ErrInit (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-133">CChkSGFiles.ErrInit function</span></span>](cchksgfiles-errinit-function.md)
    
- [<span data-ttu-id="c8125-134">CChkSGFiles.ErrTerm (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-134">CChkSGFiles.ErrTerm function</span></span>](cchksgfiles-errterm-function.md)
    
- [<span data-ttu-id="c8125-135">CChkSGFiles.iDbInvalid (enumeración)</span><span class="sxs-lookup"><span data-stu-id="c8125-135">CChkSGFiles.iDbInvalid enumeration</span></span>](cchksgfiles-idbinvalid-enumeration.md)
    
- [<span data-ttu-id="c8125-136">CChkSGFiles.New (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-136">CChkSGFiles.New function</span></span>](cchksgfiles-new-function.md)
    
- [<span data-ttu-id="c8125-137">CChkSGFiles.NO_FLAGS (enumeración)</span><span class="sxs-lookup"><span data-stu-id="c8125-137">CChkSGFiles.NO_FLAGS enumeration</span></span>](cchksgfiles-no_flags-enumeration.md)
    
- [<span data-ttu-id="c8125-138">Estructura de CChkSGFiles.PAGE_INFO</span><span class="sxs-lookup"><span data-stu-id="c8125-138">CChkSGFiles.PAGE_INFO struct</span></span>](cchksgfiles-page_info-struct.md)
    
- [<span data-ttu-id="c8125-139">CChkSGFiles.PgnoFromFileOffset (función)</span><span class="sxs-lookup"><span data-stu-id="c8125-139">CChkSGFiles.PgnoFromFileOffset function</span></span>](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a><span data-ttu-id="c8125-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="c8125-140">See also</span></span>

- [<span data-ttu-id="c8125-141">Desarrollo de Exchange y Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c8125-141">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)
- [<span data-ttu-id="c8125-142">Copia de seguridad, restauración y recuperación ante desastres</span><span class="sxs-lookup"><span data-stu-id="c8125-142">Backup, Restore, and Disaster Recovery</span></span>](http://technet.microsoft.com/en-us/library/dd876874)
    

