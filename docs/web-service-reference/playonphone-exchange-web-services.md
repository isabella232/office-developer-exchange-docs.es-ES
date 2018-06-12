---
title: PlayOnPhone (servicios Web de Exchange)
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
description: El elemento PlayOnPhone representa una solicitud para leer un elemento en un teléfono.
ms.openlocfilehash: 75493a31940ea609fd6cf454e91ca5881fb7e678
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836816"
---
# <a name="playonphone-exchange-web-services"></a><span data-ttu-id="54c06-103">PlayOnPhone (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="54c06-103">PlayOnPhone (Exchange Web Services)</span></span>

<span data-ttu-id="54c06-104">El elemento **PlayOnPhone** representa una solicitud para leer un elemento en un teléfono.</span><span class="sxs-lookup"><span data-stu-id="54c06-104">The **PlayOnPhone** element represents a request to read an item on a phone.</span></span> 
  
```xml
<PlayOnPhone>   <ItemId/>   <DialString/></PlayOnPhone>
```

 <span data-ttu-id="54c06-105">**PlayOnPhoneType**</span><span class="sxs-lookup"><span data-stu-id="54c06-105">**PlayOnPhoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54c06-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="54c06-106">Attributes and elements</span></span>

<span data-ttu-id="54c06-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="54c06-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54c06-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="54c06-108">Attributes</span></span>

<span data-ttu-id="54c06-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54c06-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54c06-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54c06-110">Child elements</span></span>

|<span data-ttu-id="54c06-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="54c06-111">**Element**</span></span>|<span data-ttu-id="54c06-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54c06-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54c06-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="54c06-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="54c06-114">Representa el identificador de un elemento que se reproducirán en un teléfono.</span><span class="sxs-lookup"><span data-stu-id="54c06-114">Represents the identifier of an item to play on a phone.</span></span> <span data-ttu-id="54c06-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="54c06-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="54c06-116">DialString (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="54c06-116">DialString (Exchange Web Services)</span></span>](dialstring-exchange-web-services.md) <br/> |<span data-ttu-id="54c06-117">Representa la cadena de marcado del número de teléfono que se llama para reproducir un elemento por teléfono.</span><span class="sxs-lookup"><span data-stu-id="54c06-117">Represents the dial string of the phone number that is called to play an item by phone.</span></span> <span data-ttu-id="54c06-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="54c06-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="54c06-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="54c06-119">Parent elements</span></span>

<span data-ttu-id="54c06-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54c06-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54c06-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54c06-121">Remarks</span></span>

<span data-ttu-id="54c06-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="54c06-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54c06-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="54c06-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54c06-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54c06-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="54c06-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="54c06-125">Schema Name</span></span>  <br/> |<span data-ttu-id="54c06-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="54c06-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="54c06-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="54c06-127">Validation File</span></span>  <br/> |<span data-ttu-id="54c06-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="54c06-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="54c06-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="54c06-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="54c06-130">False</span><span class="sxs-lookup"><span data-stu-id="54c06-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54c06-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="54c06-131">See also</span></span>



- [<span data-ttu-id="54c06-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="54c06-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

