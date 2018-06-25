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
description: El elemento UnresolvedEntry contiene el nombre de un contacto o lista de distribución para resolver.
ms.openlocfilehash: 98b447cd49685b49f73f75f12d921a65749be245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840788"
---
# <a name="unresolvedentry"></a><span data-ttu-id="02bde-103">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="02bde-103">UnresolvedEntry</span></span>

<span data-ttu-id="02bde-104">El elemento **UnresolvedEntry** contiene el nombre de un contacto o lista de distribución para resolver.</span><span class="sxs-lookup"><span data-stu-id="02bde-104">The **UnresolvedEntry** element contains the name of a contact or distribution list to resolve.</span></span> 
  
[<span data-ttu-id="02bde-105">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="02bde-105">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="02bde-106">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="02bde-106">UnresolvedEntry</span></span>](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 <span data-ttu-id="02bde-107">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="02bde-107">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02bde-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="02bde-108">Attributes and elements</span></span>

<span data-ttu-id="02bde-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="02bde-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02bde-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="02bde-110">Attributes</span></span>

<span data-ttu-id="02bde-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02bde-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02bde-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02bde-112">Child elements</span></span>

<span data-ttu-id="02bde-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02bde-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="02bde-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02bde-114">Parent elements</span></span>

|<span data-ttu-id="02bde-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="02bde-115">**Element**</span></span>|<span data-ttu-id="02bde-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02bde-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02bde-117">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="02bde-117">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="02bde-118">Define una solicitud para resolver nombres ambiguos.</span><span class="sxs-lookup"><span data-stu-id="02bde-118">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="02bde-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="02bde-119">Text value</span></span>

<span data-ttu-id="02bde-120">El valor de texto representa el nombre de una lista de contactos o de distribución pública.</span><span class="sxs-lookup"><span data-stu-id="02bde-120">The text value represents the name of a public contact or distribution list.</span></span> <span data-ttu-id="02bde-121">La longitud mínima de la cadena es un carácter.</span><span class="sxs-lookup"><span data-stu-id="02bde-121">The minimum length of the string is one character.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02bde-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02bde-122">Remarks</span></span>

<span data-ttu-id="02bde-123">El valor de texto de este elemento se utiliza para resolver nombres de los campos siguientes:</span><span class="sxs-lookup"><span data-stu-id="02bde-123">The text value of this element is used to resolve names against the following fields:</span></span>
  
- <span data-ttu-id="02bde-124">Nombre propio</span><span class="sxs-lookup"><span data-stu-id="02bde-124">First name</span></span>
    
- <span data-ttu-id="02bde-125">Apellido</span><span class="sxs-lookup"><span data-stu-id="02bde-125">Last name</span></span>
    
- <span data-ttu-id="02bde-126">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="02bde-126">Display name</span></span>
    
- <span data-ttu-id="02bde-127">Nombre completo</span><span class="sxs-lookup"><span data-stu-id="02bde-127">Full name</span></span>
    
- <span data-ttu-id="02bde-128">Office</span><span class="sxs-lookup"><span data-stu-id="02bde-128">Office</span></span>
    
- <span data-ttu-id="02bde-129">Alias</span><span class="sxs-lookup"><span data-stu-id="02bde-129">Alias</span></span>
    
- <span data-ttu-id="02bde-130">dirección SMTP</span><span class="sxs-lookup"><span data-stu-id="02bde-130">SMTP address</span></span>
    
<span data-ttu-id="02bde-131">Direcciones de correo electrónico con tipos de enrutamiento de prefijo, como smtp o sip, se guardan en una matriz con varios valores.</span><span class="sxs-lookup"><span data-stu-id="02bde-131">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="02bde-132">La [operación ResolveNames](resolvenames-operation.md) lleva a cabo a una coincidencia parcial con respecto a cada valor de dicha matriz al agregar el tipo de distribución al principio del nombre sin resolver, como "sip:User1@Contoso.com".</span><span class="sxs-lookup"><span data-stu-id="02bde-132">The [ResolveNames operation](resolvenames-operation.md) performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="02bde-133">Si no especifica un tipo de enrutamiento, la operación **ResolveNames** de forma predeterminada en el tipo de distribución de smtp, match a una propiedad de dirección SMTP principal y no buscar en la matriz con varios valores.</span><span class="sxs-lookup"><span data-stu-id="02bde-133">If you don't specify a routing type, the **ResolveNames** operation will default to the routing type of smtp, match it to a primary SMTP address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="02bde-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="02bde-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02bde-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="02bde-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02bde-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02bde-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="02bde-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="02bde-137">Schema Name</span></span>  <br/> |<span data-ttu-id="02bde-138">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="02bde-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="02bde-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="02bde-139">Validation File</span></span>  <br/> |<span data-ttu-id="02bde-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="02bde-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="02bde-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="02bde-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="02bde-142">False</span><span class="sxs-lookup"><span data-stu-id="02bde-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02bde-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="02bde-143">See also</span></span>



[<span data-ttu-id="02bde-144">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="02bde-144">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="02bde-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="02bde-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

