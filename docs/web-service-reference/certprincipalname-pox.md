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
description: El elemento CertPrincipalName especifica el nombre principal del certificado de capa de sockets seguros (SSL) que se necesita para conectarse a la organización de Microsoft Exchange Server 2007 mediante SSL.
ms.openlocfilehash: fb2a1c8577bce41945b669be56f2a94a2c4dca26
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463345"
---
# <a name="certprincipalname-pox"></a><span data-ttu-id="eee0c-103">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="eee0c-103">CertPrincipalName (POX)</span></span>

<span data-ttu-id="eee0c-104">El elemento **CertPrincipalName** especifica el nombre principal del certificado de capa de sockets seguros (SSL) que se necesita para conectarse a la organización de Microsoft Exchange Server 2007 mediante SSL.</span><span class="sxs-lookup"><span data-stu-id="eee0c-104">The **CertPrincipalName** element specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange Server 2007 organization by using SSL.</span></span> 
  
[<span data-ttu-id="eee0c-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="eee0c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="eee0c-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="eee0c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="eee0c-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="eee0c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="eee0c-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="eee0c-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="eee0c-109">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="eee0c-109">CertPrincipalName (POX)</span></span>](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="eee0c-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eee0c-110">Attributes and elements</span></span>

<span data-ttu-id="eee0c-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eee0c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eee0c-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="eee0c-112">Attributes</span></span>

<span data-ttu-id="eee0c-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eee0c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eee0c-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eee0c-114">Child elements</span></span>

<span data-ttu-id="eee0c-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eee0c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eee0c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eee0c-116">Parent elements</span></span>

|<span data-ttu-id="eee0c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="eee0c-117">**Element**</span></span>|<span data-ttu-id="eee0c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eee0c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eee0c-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="eee0c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="eee0c-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Exchange 2007 y que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="eee0c-120">Contains the specifications for connecting a client to the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eee0c-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eee0c-121">Text value</span></span>

<span data-ttu-id="eee0c-122">El valor de texto especifica el nombre de entidad de certificación SSL necesario para conectarse a la organización de Microsoft Exchange mediante SSL.</span><span class="sxs-lookup"><span data-stu-id="eee0c-122">The text value specifies the SSL certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eee0c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eee0c-123">Remarks</span></span>

<span data-ttu-id="eee0c-124">Si no se especifica el elemento **CertPrincipalName** , se establece el valor predeterminado en MSSTD: Server, donde servidor es el valor que se especifica en el elemento [servidor (POX)](server-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="eee0c-124">If the **CertPrincipalName** element is not specified, the default is set to msstd:SERVER, where SERVER is the value that is specified in the [Server (POX)](server-pox.md) element.</span></span> <span data-ttu-id="eee0c-125">Por ejemplo, si el servidor se especifica como example.com y **CertPrincipalName** se deja en blanco con [SSL (POX)](ssl-pox.md) activado, el valor predeterminado de **CertPrincipalName** sería msstd:example. com.</span><span class="sxs-lookup"><span data-stu-id="eee0c-125">For example, if SERVER is specified as example.com and **CertPrincipalName** is left blank with [SSL (POX)](ssl-pox.md) turned on, the default value of **CertPrincipalName** would be msstd:example.com.</span></span> 
  
<span data-ttu-id="eee0c-126">Si no se especifica **ninguna** , Windows validará el nombre principal del certificado de acuerdo con la información que se encuentra en el tema [nombres principales](https://go.microsoft.com/fwlink/?LinkId=93417) de MSDN.</span><span class="sxs-lookup"><span data-stu-id="eee0c-126">If **none** is specified, Windows will validate the certificate principal name according to information found in the [Principal Names](https://go.microsoft.com/fwlink/?LinkId=93417) topic on MSDN.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eee0c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="eee0c-127">See also</span></span>



[<span data-ttu-id="eee0c-128">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="eee0c-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

