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
description: El elemento DirectoryPort especifica el puerto que se usa para conectarse al directorio cuando se usa el protocolo de interfaz del proveedor de servicio de nombres (NSPI).
ms.openlocfilehash: 2ba0a15cea0b4eb9b6069fab384edb3d9747a360
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462090"
---
# <a name="directoryport-pox"></a><span data-ttu-id="5f7e4-103">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7e4-103">DirectoryPort (POX)</span></span>

<span data-ttu-id="5f7e4-104">El elemento **DirectoryPort** especifica el puerto que se usa para conectarse al directorio cuando se usa el protocolo de interfaz del proveedor de servicio de nombres (NSPI).</span><span class="sxs-lookup"><span data-stu-id="5f7e4-104">The **DirectoryPort** element specifies the port that is used to connect to the directory when the Name Service Provider Interface (NSPI) protocol is used.</span></span> 
  
- [<span data-ttu-id="5f7e4-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7e4-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="5f7e4-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7e4-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="5f7e4-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7e4-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="5f7e4-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7e4-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="5f7e4-109">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7e4-109">DirectoryPort (POX)</span></span>](directoryport-pox.md)
  
```xml
<DirectoryPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5f7e4-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f7e4-110">Attributes and elements</span></span>

<span data-ttu-id="5f7e4-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f7e4-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f7e4-112">Attributes</span></span>

<span data-ttu-id="5f7e4-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f7e4-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f7e4-114">Child elements</span></span>

<span data-ttu-id="5f7e4-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f7e4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f7e4-116">Parent elements</span></span>

|<span data-ttu-id="5f7e4-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f7e4-117">**Element**</span></span>|<span data-ttu-id="5f7e4-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f7e4-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f7e4-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7e4-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5f7e4-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f7e4-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5f7e4-121">Text value</span></span>

<span data-ttu-id="5f7e4-122">El valor de texto representa el puerto que se usa para obtener acceso al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f7e4-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f7e4-123">Remarks</span></span>

<span data-ttu-id="5f7e4-124">El elemento **DirectoryPort** solo se usa cuando el elemento [Type (POX)](type-pox.md) es igual a EXCH o a expr.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-124">The **DirectoryPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f7e4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f7e4-125">See also</span></span>

- [<span data-ttu-id="5f7e4-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="5f7e4-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

