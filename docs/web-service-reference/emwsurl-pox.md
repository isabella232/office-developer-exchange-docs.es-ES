---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: El elemento EmwsUrl especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo.
ms.openlocfilehash: 19e1078ae8d08513e85d75d87e960a910986f727
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530673"
---
# <a name="emwsurl-pox"></a><span data-ttu-id="fcaff-103">EmwsUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="fcaff-103">EmwsUrl (POX)</span></span>

<span data-ttu-id="fcaff-104">El elemento **EmwsUrl** especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="fcaff-104">The **EmwsUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
- [<span data-ttu-id="fcaff-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="fcaff-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="fcaff-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="fcaff-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="fcaff-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="fcaff-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="fcaff-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="fcaff-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="fcaff-109">EmwsUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="fcaff-109">EmwsUrl (POX)</span></span>](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="fcaff-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fcaff-110">Attributes and elements</span></span>

<span data-ttu-id="fcaff-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fcaff-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fcaff-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="fcaff-112">Attributes</span></span>

<span data-ttu-id="fcaff-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fcaff-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fcaff-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fcaff-114">Child elements</span></span>

<span data-ttu-id="fcaff-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fcaff-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fcaff-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fcaff-116">Parent elements</span></span>

|<span data-ttu-id="fcaff-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fcaff-117">**Element**</span></span>|<span data-ttu-id="fcaff-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fcaff-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fcaff-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="fcaff-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="fcaff-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="fcaff-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fcaff-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fcaff-121">Text value</span></span>

<span data-ttu-id="fcaff-122">El valor de texto representa la dirección URL del extremo de EWS para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fcaff-122">The text value represents the URL of the EWS endpoint for the user.</span></span> <span data-ttu-id="fcaff-123">Es equivalente al elemento [EwsUrl (POX)](ewsurl-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="fcaff-123">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fcaff-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcaff-124">Remarks</span></span>

<span data-ttu-id="fcaff-125">El elemento **EmwsUrl** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="fcaff-125">The **EmwsUrl** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fcaff-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcaff-126">See also</span></span>

- [<span data-ttu-id="fcaff-127">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="fcaff-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

