---
title: ProtocolConnection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: El elemento ProtocolConnection representa la conexión de protocolo del cliente de servidor Web.
ms.openlocfilehash: 8b5396821cd959e41d24fcf7a94c519f9c634a1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836915"
---
# <a name="protocolconnection-soap"></a><span data-ttu-id="0317a-103">ProtocolConnection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0317a-103">ProtocolConnection (SOAP)</span></span>

<span data-ttu-id="0317a-104">El elemento **ProtocolConnection** representa la conexión de protocolo del cliente de servidor Web.</span><span class="sxs-lookup"><span data-stu-id="0317a-104">The **ProtocolConnection** element represents the protocol connection of the server Web client.</span></span> 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 <span data-ttu-id="0317a-105">**ProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="0317a-105">**ProtocolConnection**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0317a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0317a-106">Attributes and elements</span></span>

<span data-ttu-id="0317a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0317a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0317a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0317a-108">Attributes</span></span>

<span data-ttu-id="0317a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0317a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0317a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0317a-110">Child elements</span></span>

|<span data-ttu-id="0317a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0317a-111">**Element**</span></span>|<span data-ttu-id="0317a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0317a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0317a-113">Nombre de host (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0317a-113">Hostname (SOAP)</span></span>](hostname-soap.md) <br/> |<span data-ttu-id="0317a-114">Representa la parte del nombre completo del equipo del equipo en el nombre de host.</span><span class="sxs-lookup"><span data-stu-id="0317a-114">Represents the host name portion of the full computer name of the computer.</span></span>  <br/> |
|[<span data-ttu-id="0317a-115">Puerto (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0317a-115">Port (SOAP)</span></span>](port-soap.md) <br/> |<span data-ttu-id="0317a-116">Representa el número de puerto que se usará para el protocolo.</span><span class="sxs-lookup"><span data-stu-id="0317a-116">Represents the port number to use for the protocol.</span></span>  <br/> |
|[<span data-ttu-id="0317a-117">EncryptionMethod (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0317a-117">EncryptionMethod (SOAP)</span></span>](encryptionmethod-soap.md) <br/> |<span data-ttu-id="0317a-118">Representa el método de cifrado que se usa para los protocolos POP, IMAP y SMTP.</span><span class="sxs-lookup"><span data-stu-id="0317a-118">Represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0317a-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0317a-119">Parent elements</span></span>

|<span data-ttu-id="0317a-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="0317a-120">**Element**</span></span>|<span data-ttu-id="0317a-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0317a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0317a-122">ProtocolConnections (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0317a-122">ProtocolConnections (SOAP)</span></span>](protocolconnections-soap.md) <br/> |<span data-ttu-id="0317a-123">Contiene cero o más conexiones de protocolo.</span><span class="sxs-lookup"><span data-stu-id="0317a-123">Contains zero or more protocol connections.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0317a-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0317a-124">Text value</span></span>

<span data-ttu-id="0317a-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0317a-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0317a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0317a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0317a-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0317a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0317a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0317a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0317a-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="0317a-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0317a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0317a-130">Validation File</span></span>  <br/> |<span data-ttu-id="0317a-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0317a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0317a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0317a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0317a-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0317a-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0317a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0317a-134">See also</span></span>



[<span data-ttu-id="0317a-135">ProtocolConnectionCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0317a-135">ProtocolConnectionCollectionSetting (SOAP)</span></span>](protocolconnectioncollectionsetting-soap.md)

