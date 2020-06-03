---
title: Dominio
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Domain
api_type:
- schema
ms.assetid: 7e45a061-856f-4b44-b053-a7c4d5ad569e
description: El elemento Domain identifica un solo dominio SMTP.
ms.openlocfilehash: 3bf8e132b5fa588171ac4f3c095692bc68394663
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461334"
---
# <a name="domain"></a><span data-ttu-id="1b49c-103">Dominio</span><span class="sxs-lookup"><span data-stu-id="1b49c-103">Domain</span></span>

<span data-ttu-id="1b49c-104">El elemento **Domain** identifica un solo dominio SMTP.</span><span class="sxs-lookup"><span data-stu-id="1b49c-104">The **Domain** element identifies a single SMTP domain.</span></span> 
  
```xml
<Domain Name="" IncludeSubdomains="" />
```

 <span data-ttu-id="1b49c-105">**StmpDomain**</span><span class="sxs-lookup"><span data-stu-id="1b49c-105">**StmpDomain**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b49c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1b49c-106">Attributes and elements</span></span>

<span data-ttu-id="1b49c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1b49c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b49c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b49c-108">Attributes</span></span>

|<span data-ttu-id="1b49c-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1b49c-109">**Attribute**</span></span>|<span data-ttu-id="1b49c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b49c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b49c-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b49c-111">Name</span></span>  <br/> |<span data-ttu-id="1b49c-112">Identifica el nombre de un dominio.</span><span class="sxs-lookup"><span data-stu-id="1b49c-112">Identifies the name of a domain.</span></span> <span data-ttu-id="1b49c-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1b49c-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="1b49c-114">IncludeSubdomains</span><span class="sxs-lookup"><span data-stu-id="1b49c-114">IncludeSubdomains</span></span>  <br/> |<span data-ttu-id="1b49c-115">Indica si los subdominios del dominio identificado por el atributo **Name** se consideran internos.</span><span class="sxs-lookup"><span data-stu-id="1b49c-115">Indicates whether subdomains of the domain identified by the **Name** attribute are considered internal.</span></span> <span data-ttu-id="1b49c-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="1b49c-116">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1b49c-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1b49c-117">Child elements</span></span>

<span data-ttu-id="1b49c-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1b49c-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1b49c-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1b49c-119">Parent elements</span></span>

|<span data-ttu-id="1b49c-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b49c-120">**Element**</span></span>|<span data-ttu-id="1b49c-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b49c-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b49c-122">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="1b49c-122">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="1b49c-123">Identifica la lista de dominios SMTP internos de la organización.</span><span class="sxs-lookup"><span data-stu-id="1b49c-123">Identifies the list of internal SMTP domains of the organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1b49c-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1b49c-124">Text value</span></span>

<span data-ttu-id="1b49c-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1b49c-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b49c-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b49c-126">Remarks</span></span>

<span data-ttu-id="1b49c-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1b49c-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b49c-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1b49c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b49c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b49c-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1b49c-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1b49c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="1b49c-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1b49c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="1b49c-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1b49c-132">Validation File</span></span>  <br/> |<span data-ttu-id="1b49c-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1b49c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1b49c-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1b49c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="1b49c-135">Falso</span><span class="sxs-lookup"><span data-stu-id="1b49c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b49c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b49c-136">See also</span></span>

- [<span data-ttu-id="1b49c-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1b49c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

