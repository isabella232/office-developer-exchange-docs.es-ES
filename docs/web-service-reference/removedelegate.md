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
ms.openlocfilehash: eca357ad1ed2dc692f9f192b97abd3a5d765fafb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465523"
---
# <a name="removedelegate"></a><span data-ttu-id="943d1-104">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="943d1-104">RemoveDelegate</span></span>

<span data-ttu-id="943d1-105">El elemento **RemoveDelegate** define una solicitud para quitar delegados de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="943d1-105">The **RemoveDelegate** element defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="943d1-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="943d1-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<RemoveDelegate>
      <Mailbox/>
   <UserIds/>
</RemoveDelegate>
```

 <span data-ttu-id="943d1-107">**RemoveDelegateType**</span><span class="sxs-lookup"><span data-stu-id="943d1-107">**RemoveDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="943d1-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="943d1-108">Attributes and elements</span></span>

<span data-ttu-id="943d1-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="943d1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="943d1-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="943d1-110">Attributes</span></span>

<span data-ttu-id="943d1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="943d1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="943d1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="943d1-112">Child elements</span></span>

|<span data-ttu-id="943d1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="943d1-113">**Element**</span></span>|<span data-ttu-id="943d1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="943d1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="943d1-115">Buzón</span><span class="sxs-lookup"><span data-stu-id="943d1-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="943d1-116">Identifica el buzón de la entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="943d1-116">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="943d1-117">UserIds</span><span class="sxs-lookup"><span data-stu-id="943d1-117">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="943d1-118">Contiene una matriz de usuarios delegados para quitar del buzón de una entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="943d1-118">Contains an array of delegate users to remove from a principal's mailbox.</span></span> <span data-ttu-id="943d1-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="943d1-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="943d1-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="943d1-120">Parent elements</span></span>

<span data-ttu-id="943d1-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="943d1-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="943d1-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="943d1-122">Remarks</span></span>

<span data-ttu-id="943d1-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="943d1-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="943d1-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="943d1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="943d1-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="943d1-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="943d1-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="943d1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="943d1-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="943d1-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="943d1-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="943d1-128">Validation File</span></span>  <br/> |<span data-ttu-id="943d1-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="943d1-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="943d1-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="943d1-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="943d1-131">Falso</span><span class="sxs-lookup"><span data-stu-id="943d1-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="943d1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="943d1-132">See also</span></span>



[<span data-ttu-id="943d1-133">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="943d1-133">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="943d1-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="943d1-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

