---
title: FileAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAs
api_type:
- schema
ms.assetid: df50524e-471c-49d2-89fe-b2d0f61a1365
description: El elemento Fileas representa cómo se archiva un contacto o una lista de distribución en la carpeta contactos.
ms.openlocfilehash: be756d86d7608fcb758dd54f2ada9f03a04343e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461201"
---
# <a name="fileas"></a><span data-ttu-id="e3569-103">FileAs</span><span class="sxs-lookup"><span data-stu-id="e3569-103">FileAs</span></span>

<span data-ttu-id="e3569-104">El elemento **fileas** representa cómo se archiva un contacto o una lista de distribución en la carpeta contactos.</span><span class="sxs-lookup"><span data-stu-id="e3569-104">The **FileAs** element represents how a contact or distribution list is filed in the Contacts folder.</span></span> 
  
```xml
<FileAs/>
```

 <span data-ttu-id="e3569-105">**string**</span><span class="sxs-lookup"><span data-stu-id="e3569-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3569-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e3569-106">Attributes and elements</span></span>

<span data-ttu-id="e3569-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e3569-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3569-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e3569-108">Attributes</span></span>

<span data-ttu-id="e3569-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e3569-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3569-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e3569-110">Child elements</span></span>

<span data-ttu-id="e3569-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e3569-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3569-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e3569-112">Parent elements</span></span>

|<span data-ttu-id="e3569-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e3569-113">**Element**</span></span>|<span data-ttu-id="e3569-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e3569-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3569-115">DistributionList</span><span class="sxs-lookup"><span data-stu-id="e3569-115">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="e3569-116">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="e3569-116">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="e3569-117">Contacto</span><span class="sxs-lookup"><span data-stu-id="e3569-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e3569-118">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3569-118">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3569-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e3569-119">Text value</span></span>

<span data-ttu-id="e3569-120">Si se usa este elemento, se necesita un valor de texto que represente una cadena.</span><span class="sxs-lookup"><span data-stu-id="e3569-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3569-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3569-121">Remarks</span></span>

<span data-ttu-id="e3569-122">El elemento **fileas** se usa para ordenar los contactos y las listas de distribución por un nombre que no sea el nombre completo o el nombre de la compañía.</span><span class="sxs-lookup"><span data-stu-id="e3569-122">The **FileAs** element is used to sort contacts and distribution lists by a name other than a full name or company name.</span></span> 
  
<span data-ttu-id="e3569-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e3569-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3569-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e3569-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3569-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3569-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e3569-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e3569-126">Schema name</span></span>  <br/> |<span data-ttu-id="e3569-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e3569-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="e3569-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e3569-128">Validation file</span></span>  <br/> |<span data-ttu-id="e3569-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e3569-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e3569-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e3569-130">Can be empty</span></span>  <br/> |<span data-ttu-id="e3569-131">Falso</span><span class="sxs-lookup"><span data-stu-id="e3569-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3569-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3569-132">See also</span></span>



- [<span data-ttu-id="e3569-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e3569-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

