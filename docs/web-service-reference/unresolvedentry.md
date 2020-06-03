---
title: UnresolvedEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: El elemento UnresolvedEntry contiene el nombre de un contacto o una lista de distribución para resolverlos.
ms.openlocfilehash: 0f157c1be6c327187456a795c4c1000b8c35b620
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459843"
---
# <a name="unresolvedentry"></a><span data-ttu-id="7343f-103">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="7343f-103">UnresolvedEntry</span></span>

<span data-ttu-id="7343f-104">El elemento **UnresolvedEntry** contiene el nombre de un contacto o una lista de distribución para resolverlos.</span><span class="sxs-lookup"><span data-stu-id="7343f-104">The **UnresolvedEntry** element contains the name of a contact or distribution list to resolve.</span></span> 
  
[<span data-ttu-id="7343f-105">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="7343f-105">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="7343f-106">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="7343f-106">UnresolvedEntry</span></span>](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 <span data-ttu-id="7343f-107">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="7343f-107">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7343f-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7343f-108">Attributes and elements</span></span>

<span data-ttu-id="7343f-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7343f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7343f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7343f-110">Attributes</span></span>

<span data-ttu-id="7343f-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7343f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7343f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7343f-112">Child elements</span></span>

<span data-ttu-id="7343f-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7343f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7343f-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7343f-114">Parent elements</span></span>

|<span data-ttu-id="7343f-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7343f-115">**Element**</span></span>|<span data-ttu-id="7343f-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7343f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7343f-117">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="7343f-117">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="7343f-118">Define una solicitud para resolver nombres ambiguos.</span><span class="sxs-lookup"><span data-stu-id="7343f-118">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7343f-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7343f-119">Text value</span></span>

<span data-ttu-id="7343f-120">El valor de texto representa el nombre de un contacto público o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="7343f-120">The text value represents the name of a public contact or distribution list.</span></span> <span data-ttu-id="7343f-121">La longitud mínima de la cadena es un carácter.</span><span class="sxs-lookup"><span data-stu-id="7343f-121">The minimum length of the string is one character.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7343f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7343f-122">Remarks</span></span>

<span data-ttu-id="7343f-123">El valor de texto de este elemento se usa para resolver nombres con los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="7343f-123">The text value of this element is used to resolve names against the following fields:</span></span>
  
- <span data-ttu-id="7343f-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="7343f-124">First name</span></span>
    
- <span data-ttu-id="7343f-125">Apellidos</span><span class="sxs-lookup"><span data-stu-id="7343f-125">Last name</span></span>
    
- <span data-ttu-id="7343f-126">Nombre completo (DN)</span><span class="sxs-lookup"><span data-stu-id="7343f-126">Display name</span></span>
    
- <span data-ttu-id="7343f-127">Nombre completo</span><span class="sxs-lookup"><span data-stu-id="7343f-127">Full name</span></span>
    
- <span data-ttu-id="7343f-128">Office</span><span class="sxs-lookup"><span data-stu-id="7343f-128">Office</span></span>
    
- <span data-ttu-id="7343f-129">Alias</span><span class="sxs-lookup"><span data-stu-id="7343f-129">Alias</span></span>
    
- <span data-ttu-id="7343f-130">Dirección SMTP</span><span class="sxs-lookup"><span data-stu-id="7343f-130">SMTP address</span></span>
    
<span data-ttu-id="7343f-131">Las direcciones de correo electrónico con tipos de enrutamiento prefijados, como SMTP o SIP, se guardan en una matriz de varios valores.</span><span class="sxs-lookup"><span data-stu-id="7343f-131">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="7343f-132">La [operación ResolveNames](resolvenames-operation.md) realiza una coincidencia parcial con cada valor de la matriz cuando se agrega el tipo de enrutamiento al principio del nombre sin resolver, como "SIP:user1@Contoso.com".</span><span class="sxs-lookup"><span data-stu-id="7343f-132">The [ResolveNames operation](resolvenames-operation.md) performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="7343f-133">Si no especifica un tipo de enrutamiento, la operación **ResolveNames** se establecerá de forma predeterminada en el tipo de enrutamiento de SMTP, lo hará coincidir con una propiedad de dirección SMTP principal y no buscará en la matriz de varios valores.</span><span class="sxs-lookup"><span data-stu-id="7343f-133">If you don't specify a routing type, the **ResolveNames** operation will default to the routing type of smtp, match it to a primary SMTP address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="7343f-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7343f-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7343f-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7343f-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7343f-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="7343f-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7343f-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7343f-137">Schema Name</span></span>  <br/> |<span data-ttu-id="7343f-138">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7343f-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7343f-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7343f-139">Validation File</span></span>  <br/> |<span data-ttu-id="7343f-140">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7343f-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7343f-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7343f-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="7343f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7343f-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7343f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="7343f-143">See also</span></span>



[<span data-ttu-id="7343f-144">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="7343f-144">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="7343f-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7343f-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

