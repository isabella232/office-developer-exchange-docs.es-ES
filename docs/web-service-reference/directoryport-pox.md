---
title: DirectoryPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: El elemento DirectoryPort especifica el puerto que se usa para conectarse al directorio cuando se usa el protocolo de interfaz de proveedor de servicio de nombres (NSPI).
ms.openlocfilehash: 1b73b9cd1d21c73f4e897684371993312f741322
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764167"
---
# <a name="directoryport-pox"></a><span data-ttu-id="b6207-103">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="b6207-103">DirectoryPort (POX)</span></span>

<span data-ttu-id="b6207-104">El elemento **DirectoryPort** especifica el puerto que se usa para conectarse al directorio cuando se usa el protocolo de interfaz de proveedor de servicio de nombres (NSPI).</span><span class="sxs-lookup"><span data-stu-id="b6207-104">The **DirectoryPort** element specifies the port that is used to connect to the directory when the Name Service Provider Interface (NSPI) protocol is used.</span></span> 
  
- [<span data-ttu-id="b6207-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="b6207-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="b6207-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="b6207-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="b6207-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="b6207-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="b6207-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="b6207-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="b6207-109">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="b6207-109">DirectoryPort (POX)</span></span>](directoryport-pox.md)
  
```xml
<DirectoryPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b6207-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b6207-110">Attributes and elements</span></span>

<span data-ttu-id="b6207-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b6207-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6207-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6207-112">Attributes</span></span>

<span data-ttu-id="b6207-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b6207-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6207-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b6207-114">Child elements</span></span>

<span data-ttu-id="b6207-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b6207-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b6207-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b6207-116">Parent elements</span></span>

|<span data-ttu-id="b6207-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6207-117">**Element**</span></span>|<span data-ttu-id="b6207-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6207-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6207-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="b6207-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="b6207-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b6207-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b6207-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b6207-121">Text value</span></span>

<span data-ttu-id="b6207-122">El valor de texto representa el puerto que se usa para tener acceso al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6207-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6207-123">Notas</span><span class="sxs-lookup"><span data-stu-id="b6207-123">Remarks</span></span>

<span data-ttu-id="b6207-124">El elemento **DirectoryPort** solo se usa cuando el elemento de [Tipo (POX)](type-pox.md) es igual a EXCH o EXPR.</span><span class="sxs-lookup"><span data-stu-id="b6207-124">The **DirectoryPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6207-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="b6207-125">See also</span></span>

- [<span data-ttu-id="b6207-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b6207-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

