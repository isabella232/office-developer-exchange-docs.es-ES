---
title: Reproducir (servicios web Exchange)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 486612be-470c-4f99-929a-f2b283e055c1
description: El elemento reproducir representa una solicitud para leer un elemento en un teléfono.
ms.openlocfilehash: e2c09a67255106ad9afddb86fa19b7a4a5762ee5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466251"
---
# <a name="playonphone-exchange-web-services"></a><span data-ttu-id="78c63-103">Reproducir (servicios web Exchange)</span><span class="sxs-lookup"><span data-stu-id="78c63-103">PlayOnPhone (Exchange Web Services)</span></span>

<span data-ttu-id="78c63-104">El elemento **reproducir** representa una solicitud para leer un elemento en un teléfono.</span><span class="sxs-lookup"><span data-stu-id="78c63-104">The **PlayOnPhone** element represents a request to read an item on a phone.</span></span> 
  
```xml
<PlayOnPhone>   <ItemId/>   <DialString/></PlayOnPhone>
```

 <span data-ttu-id="78c63-105">**PlayOnPhoneType**</span><span class="sxs-lookup"><span data-stu-id="78c63-105">**PlayOnPhoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78c63-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="78c63-106">Attributes and elements</span></span>

<span data-ttu-id="78c63-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="78c63-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78c63-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="78c63-108">Attributes</span></span>

<span data-ttu-id="78c63-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="78c63-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78c63-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="78c63-110">Child elements</span></span>

|<span data-ttu-id="78c63-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="78c63-111">**Element**</span></span>|<span data-ttu-id="78c63-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="78c63-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78c63-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="78c63-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="78c63-114">Representa el identificador de un elemento que se va a reproducir en un teléfono.</span><span class="sxs-lookup"><span data-stu-id="78c63-114">Represents the identifier of an item to play on a phone.</span></span> <span data-ttu-id="78c63-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="78c63-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="78c63-116">DialString (servicios web Exchange)</span><span class="sxs-lookup"><span data-stu-id="78c63-116">DialString (Exchange Web Services)</span></span>](dialstring-exchange-web-services.md) <br/> |<span data-ttu-id="78c63-117">Representa la cadena de marcado del número de teléfono al que se llama para reproducir un elemento por teléfono.</span><span class="sxs-lookup"><span data-stu-id="78c63-117">Represents the dial string of the phone number that is called to play an item by phone.</span></span> <span data-ttu-id="78c63-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="78c63-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="78c63-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="78c63-119">Parent elements</span></span>

<span data-ttu-id="78c63-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="78c63-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78c63-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78c63-121">Remarks</span></span>

<span data-ttu-id="78c63-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="78c63-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78c63-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="78c63-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78c63-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="78c63-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="78c63-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="78c63-125">Schema Name</span></span>  <br/> |<span data-ttu-id="78c63-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="78c63-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="78c63-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="78c63-127">Validation File</span></span>  <br/> |<span data-ttu-id="78c63-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="78c63-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="78c63-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="78c63-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="78c63-130">Falso</span><span class="sxs-lookup"><span data-stu-id="78c63-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78c63-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="78c63-131">See also</span></span>



- [<span data-ttu-id="78c63-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="78c63-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

