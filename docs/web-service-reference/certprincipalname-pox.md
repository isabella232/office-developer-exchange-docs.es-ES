---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: El elemento CertPrincipalName especifica el nombre de entidad de seguridad de certificado de capa de Sockets seguros (SSL) que es necesario para conectarse a la organización de Microsoft Exchange Server 2007 mediante el uso de SSL.
ms.openlocfilehash: d2766b16a3e8a1bcd013de332d9c07f709fcf949
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763734"
---
# <a name="certprincipalname-pox"></a><span data-ttu-id="e042c-103">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="e042c-103">CertPrincipalName (POX)</span></span>

<span data-ttu-id="e042c-104">El elemento **CertPrincipalName** especifica el nombre de entidad de seguridad de certificado de capa de Sockets seguros (SSL) que es necesario para conectarse a la organización de Microsoft Exchange Server 2007 mediante el uso de SSL.</span><span class="sxs-lookup"><span data-stu-id="e042c-104">The **CertPrincipalName** element specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange Server 2007 organization by using SSL.</span></span> 
  
[<span data-ttu-id="e042c-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="e042c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="e042c-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="e042c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="e042c-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="e042c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="e042c-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="e042c-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="e042c-109">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="e042c-109">CertPrincipalName (POX)</span></span>](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e042c-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e042c-110">Attributes and elements</span></span>

<span data-ttu-id="e042c-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e042c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e042c-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="e042c-112">Attributes</span></span>

<span data-ttu-id="e042c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e042c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e042c-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e042c-114">Child elements</span></span>

<span data-ttu-id="e042c-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e042c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e042c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e042c-116">Parent elements</span></span>

|<span data-ttu-id="e042c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e042c-117">**Element**</span></span>|<span data-ttu-id="e042c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e042c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e042c-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="e042c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="e042c-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Exchange 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e042c-120">Contains the specifications for connecting a client to the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e042c-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e042c-121">Text value</span></span>

<span data-ttu-id="e042c-122">El valor de texto especifica el nombre de entidad de seguridad de certificados SSL que se necesita para conectarse a la organización de Microsoft Exchange mediante el uso de SSL.</span><span class="sxs-lookup"><span data-stu-id="e042c-122">The text value specifies the SSL certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e042c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e042c-123">Remarks</span></span>

<span data-ttu-id="e042c-124">Si no se especifica el elemento **CertPrincipalName** , el valor predeterminado se establece en msstd:SERVER, donde servidor es el valor que se especifica en el elemento de [Servidor (POX)](server-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="e042c-124">If the **CertPrincipalName** element is not specified, the default is set to msstd:SERVER, where SERVER is the value that is specified in the [Server (POX)](server-pox.md) element.</span></span> <span data-ttu-id="e042c-125">Por ejemplo, si el servidor especificado como example.com y **CertPrincipalName** se deja en blanco con [SSL (POX)](ssl-pox.md) activado, el valor predeterminado de **CertPrincipalName** sería msstd:example.com.</span><span class="sxs-lookup"><span data-stu-id="e042c-125">For example, if SERVER is specified as example.com and **CertPrincipalName** is left blank with [SSL (POX)](ssl-pox.md) turned on, the default value of **CertPrincipalName** would be msstd:example.com.</span></span> 
  
<span data-ttu-id="e042c-126">Si no se especifica **ninguna** , Windows validará el nombre de entidad de seguridad del certificado según la información que se encuentra en el tema de [Los nombres de entidad de seguridad](http://go.microsoft.com/fwlink/?LinkId=93417) en MSDN.</span><span class="sxs-lookup"><span data-stu-id="e042c-126">If **none** is specified, Windows will validate the certificate principal name according to information found in the [Principal Names](http://go.microsoft.com/fwlink/?LinkId=93417) topic on MSDN.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e042c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e042c-127">See also</span></span>



[<span data-ttu-id="e042c-128">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="e042c-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

