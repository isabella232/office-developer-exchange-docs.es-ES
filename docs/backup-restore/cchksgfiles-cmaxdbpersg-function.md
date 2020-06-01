---
title: Función función cchksgfiles. CMaxDbPerSG
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: b7c3517779eb07ef053c1dd4fa25544310fb3343
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455264"
---
# <a name="cchksgfilescmaxdbpersg-function"></a><span data-ttu-id="ba6ce-103">Función función cchksgfiles. CMaxDbPerSG</span><span class="sxs-lookup"><span data-stu-id="ba6ce-103">CChkSGFiles.CMaxDbPerSG function</span></span>

<span data-ttu-id="ba6ce-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba6ce-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="ba6ce-105">Devuelve el número máximo de bases de datos permitidas en un único grupo de almacenamiento de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ba6ce-105">Returns the maximum number of databases allowed in a single Exchange server storage group.</span></span>
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a><span data-ttu-id="ba6ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba6ce-106">Parameters</span></span>

<span data-ttu-id="ba6ce-107">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba6ce-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="ba6ce-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba6ce-108">Return value</span></span>

<span data-ttu-id="ba6ce-109">El número máximo de bases de datos que el servidor de Exchange especificado permite por grupo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="ba6ce-109">The maximum number of databases that the specified Exchange server allows per storage group.</span></span> <span data-ttu-id="ba6ce-110">Como los grupos de almacenamiento no forman parte de Exchange 2013, esta función devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="ba6ce-110">Because storage groups are not part of Exchange 2013, this function returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ba6ce-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba6ce-111">Remarks</span></span>

<span data-ttu-id="ba6ce-112">Puede usar el objeto **CCheckSGFiles** para validar las bases de datos (y los archivos de registro de transacciones) en un solo grupo de almacenamiento, por lo que el valor devuelto por la función **CMaxDbPerSG** también representa el número máximo de bases de datos que puede comprobar mediante una instancia de la clase **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="ba6ce-112">You can use the **CCheckSGFiles** object to validate databases (and transaction log files) in only one storage group, so the value returned by the **CMaxDbPerSG** function also represents the maximum number of databases that you can check by using an instance of the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="ba6ce-113">Tenga en cuenta que, de forma predeterminada, Exchange Server 2003 y Exchange Server 2007 permiten un máximo de cinco bases de datos por grupo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="ba6ce-113">Note that by default, Exchange Server 2003 and Exchange Server 2007 allow a maximum of five databases per storage group.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="ba6ce-114">Requirements</span><span class="sxs-lookup"><span data-stu-id="ba6ce-114">Requirements</span></span>

<span data-ttu-id="ba6ce-115">Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="ba6ce-115">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="ba6ce-116">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="ba6ce-116">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

