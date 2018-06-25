---
title: RemoveDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegate
api_type:
- schema
ms.assetid: f21c5171-62e7-47c8-99b1-22e1ff5883bb
description: El elemento RemoveDelegate define una solicitud para quitar delegados de un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 27618b1767c99b26a5f4c06e97a20e063b598d9d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837085"
---
# <a name="removedelegate"></a><span data-ttu-id="95e1c-104">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="95e1c-104">RemoveDelegate</span></span>

<span data-ttu-id="95e1c-105">El elemento **RemoveDelegate** define una solicitud para quitar delegados de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="95e1c-105">The **RemoveDelegate** element defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="95e1c-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="95e1c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<RemoveDelegate>
      <Mailbox/>
   <UserIds/>
</RemoveDelegate>
```

 <span data-ttu-id="95e1c-107">**RemoveDelegateType**</span><span class="sxs-lookup"><span data-stu-id="95e1c-107">**RemoveDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95e1c-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="95e1c-108">Attributes and elements</span></span>

<span data-ttu-id="95e1c-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="95e1c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95e1c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="95e1c-110">Attributes</span></span>

<span data-ttu-id="95e1c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95e1c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95e1c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95e1c-112">Child elements</span></span>

|<span data-ttu-id="95e1c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="95e1c-113">**Element**</span></span>|<span data-ttu-id="95e1c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95e1c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95e1c-115">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="95e1c-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="95e1c-116">Identifica el buzón de correo de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="95e1c-116">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="95e1c-117">Identificadores de usuario</span><span class="sxs-lookup"><span data-stu-id="95e1c-117">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="95e1c-118">Contiene una matriz de delegado a los usuarios quitar de buzón de correo de una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="95e1c-118">Contains an array of delegate users to remove from a principal's mailbox.</span></span> <span data-ttu-id="95e1c-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="95e1c-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95e1c-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95e1c-120">Parent elements</span></span>

<span data-ttu-id="95e1c-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95e1c-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95e1c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95e1c-122">Remarks</span></span>

<span data-ttu-id="95e1c-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="95e1c-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95e1c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95e1c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95e1c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95e1c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="95e1c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="95e1c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="95e1c-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="95e1c-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="95e1c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="95e1c-128">Validation File</span></span>  <br/> |<span data-ttu-id="95e1c-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="95e1c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="95e1c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="95e1c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="95e1c-131">False</span><span class="sxs-lookup"><span data-stu-id="95e1c-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95e1c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="95e1c-132">See also</span></span>



[<span data-ttu-id="95e1c-133">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="95e1c-133">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="95e1c-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="95e1c-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

