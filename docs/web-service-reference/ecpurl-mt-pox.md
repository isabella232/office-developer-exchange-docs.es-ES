---
title: EcpUrl-MT (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: El elemento EcpUrl-MT especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de mensajes de correo electrónico para un usuario habilitado para correo.
ms.openlocfilehash: 097811add5635bca14c659814652bca244a1398d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458715"
---
# <a name="ecpurl-mt-pox"></a><span data-ttu-id="41c6c-103">EcpUrl-MT (POX)</span><span class="sxs-lookup"><span data-stu-id="41c6c-103">EcpUrl-mt (POX)</span></span>

<span data-ttu-id="41c6c-104">El elemento **EcpUrl-MT** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de mensajes de correo electrónico para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="41c6c-104">The **EcpUrl-mt** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="41c6c-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="41c6c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="41c6c-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="41c6c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="41c6c-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="41c6c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="41c6c-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="41c6c-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="41c6c-109">EcpUrl-MT (POX)</span><span class="sxs-lookup"><span data-stu-id="41c6c-109">EcpUrl-mt (POX)</span></span>](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="41c6c-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="41c6c-110">Attributes and elements</span></span>

<span data-ttu-id="41c6c-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="41c6c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41c6c-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="41c6c-112">Attributes</span></span>

<span data-ttu-id="41c6c-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="41c6c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41c6c-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="41c6c-114">Child elements</span></span>

<span data-ttu-id="41c6c-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="41c6c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41c6c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="41c6c-116">Parent elements</span></span>

|<span data-ttu-id="41c6c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="41c6c-117">**Element**</span></span>|<span data-ttu-id="41c6c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41c6c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41c6c-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="41c6c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="41c6c-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="41c6c-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41c6c-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="41c6c-121">Text value</span></span>

<span data-ttu-id="41c6c-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración del seguimiento de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="41c6c-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email tracking settings for the user.</span></span> <span data-ttu-id="41c6c-123">El valor del elemento **EcpUrl-MT** contiene los parámetros contenidos dentro de los caracteres ' < ' y ' > ' que el cliente sustituye, tal como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="41c6c-123">The value of the **EcpUrl-mt** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="41c6c-124">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="41c6c-124">**Parameter**</span></span>|<span data-ttu-id="41c6c-125">**Sustituto con**</span><span class="sxs-lookup"><span data-stu-id="41c6c-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="41c6c-126">_IsOwa_</span><span class="sxs-lookup"><span data-stu-id="41c6c-126">_IsOwa_</span></span> <br/> |<span data-ttu-id="41c6c-127">n</span><span class="sxs-lookup"><span data-stu-id="41c6c-127">n</span></span>  <br/> |
| <span data-ttu-id="41c6c-128">_MsgID_</span><span class="sxs-lookup"><span data-stu-id="41c6c-128">_MsgID_</span></span> <br/> |<span data-ttu-id="41c6c-129">Identificador del mensaje de Internet del mensaje que se va a realizar un seguimiento según lo especificado por el encabezado del identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="41c6c-129">Internet message identifier of the message to be tracked as specified by the Message-ID header.</span></span>  <br/> |
| <span data-ttu-id="41c6c-130">_MBX_</span><span class="sxs-lookup"><span data-stu-id="41c6c-130">_Mbx_</span></span> <br/> |<span data-ttu-id="41c6c-131">La dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="41c6c-131">The SMTP address of the mailbox owner.</span></span>  <br/> |
| <span data-ttu-id="41c6c-132">_Sender_</span><span class="sxs-lookup"><span data-stu-id="41c6c-132">_Sender_</span></span> <br/> |<span data-ttu-id="41c6c-133">La dirección SMTP del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="41c6c-133">The SMTP address of the message's sender.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41c6c-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41c6c-134">Remarks</span></span>

<span data-ttu-id="41c6c-135">El elemento **EcpUrl-MT** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="41c6c-135">The **EcpUrl-mt** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41c6c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="41c6c-136">See also</span></span>



[<span data-ttu-id="41c6c-137">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="41c6c-137">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

