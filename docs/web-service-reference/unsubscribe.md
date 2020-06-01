---
title: Cancelar suscripción
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 5584db5f-553a-47ce-85fb-f9902c9990ab
description: El elemento unsubscribe contiene las propiedades que se usan para cancelar la suscripción de una suscripción.
ms.openlocfilehash: d3d9c3bf9ad97cc0fdabf574c6505c797583838a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467217"
---
# <a name="unsubscribe"></a><span data-ttu-id="c5767-103">Cancelar suscripción</span><span class="sxs-lookup"><span data-stu-id="c5767-103">Unsubscribe</span></span>

<span data-ttu-id="c5767-104">El elemento **unsubscribe** contiene las propiedades que se usan para cancelar la suscripción de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="c5767-104">The **Unsubscribe** element contains the properties used to unsubscribe from a subscription.</span></span> 
  
[<span data-ttu-id="c5767-105">Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="c5767-105">Unsubscribe</span></span>](unsubscribe.md)
  
```xml
<Unsubscribe>
   <SubscriptionId/>
</Unsubscribe>
```

 <span data-ttu-id="c5767-106">**UnsubscribeType**</span><span class="sxs-lookup"><span data-stu-id="c5767-106">**UnsubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5767-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c5767-107">Attributes and elements</span></span>

<span data-ttu-id="c5767-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c5767-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5767-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5767-109">Attributes</span></span>

<span data-ttu-id="c5767-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c5767-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5767-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5767-111">Child elements</span></span>

|<span data-ttu-id="c5767-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c5767-112">**Element**</span></span>|<span data-ttu-id="c5767-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5767-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5767-114">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="c5767-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="c5767-115">Representa el identificador de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="c5767-115">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c5767-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c5767-116">Parent elements</span></span>

<span data-ttu-id="c5767-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c5767-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5767-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5767-118">Remarks</span></span>

<span data-ttu-id="c5767-119">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c5767-119">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5767-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c5767-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5767-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5767-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c5767-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c5767-122">Schema name</span></span>  <br/> |<span data-ttu-id="c5767-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c5767-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c5767-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c5767-124">Validation file</span></span>  <br/> |<span data-ttu-id="c5767-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c5767-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c5767-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c5767-126">Can be empty</span></span>  <br/> |<span data-ttu-id="c5767-127">Falso</span><span class="sxs-lookup"><span data-stu-id="c5767-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5767-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5767-128">See also</span></span>



[<span data-ttu-id="c5767-129">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="c5767-129">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="c5767-130">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="c5767-130">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="c5767-131">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="c5767-131">Unsubscribe operation</span></span>](unsubscribe-operation.md)

