---
title: PhysicalAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhysicalAddresses
api_type:
- schema
ms.assetid: 5276c5f2-9e08-43af-a0b2-da4ff1dcae2d
description: El elemento PhysicalAddresses contiene una colección de direcciones físicas que están asociadas a un contacto.
ms.openlocfilehash: b609abed481359fa6562f41a551645eb613ddfa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468883"
---
# <a name="physicaladdresses"></a><span data-ttu-id="13de4-103">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="13de4-103">PhysicalAddresses</span></span>

<span data-ttu-id="13de4-104">El elemento **PhysicalAddresses** contiene una colección de direcciones físicas que están asociadas a un contacto.</span><span class="sxs-lookup"><span data-stu-id="13de4-104">The **PhysicalAddresses** element contains a collection of physical addresses that are associated with a contact.</span></span> 
  
```xml
<PhysicalAddresses>
   <Entry/>
</PhysicalAddresses>
```

 <span data-ttu-id="13de4-105">**PhysicalAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="13de4-105">**PhysicalAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13de4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="13de4-106">Attributes and elements</span></span>

<span data-ttu-id="13de4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="13de4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13de4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="13de4-108">Attributes</span></span>

<span data-ttu-id="13de4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="13de4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13de4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13de4-110">Child elements</span></span>

|<span data-ttu-id="13de4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="13de4-111">**Element**</span></span>|<span data-ttu-id="13de4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13de4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13de4-113">Entrada (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="13de4-113">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md) <br/> |<span data-ttu-id="13de4-114">Describe una dirección física única para un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="13de4-114">Describes a single physical address for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13de4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="13de4-115">Parent elements</span></span>

|<span data-ttu-id="13de4-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="13de4-116">**Element**</span></span>|<span data-ttu-id="13de4-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13de4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13de4-118">Contacto</span><span class="sxs-lookup"><span data-stu-id="13de4-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="13de4-119">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="13de4-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13de4-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13de4-120">Remarks</span></span>

<span data-ttu-id="13de4-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="13de4-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13de4-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="13de4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13de4-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="13de4-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13de4-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="13de4-124">Schema name</span></span>  <br/> |<span data-ttu-id="13de4-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="13de4-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="13de4-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="13de4-126">Validation file</span></span>  <br/> |<span data-ttu-id="13de4-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="13de4-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="13de4-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="13de4-128">Can be empty</span></span>  <br/> |<span data-ttu-id="13de4-129">Falso</span><span class="sxs-lookup"><span data-stu-id="13de4-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13de4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="13de4-130">See also</span></span>



- [<span data-ttu-id="13de4-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="13de4-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="13de4-132">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="13de4-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="13de4-133">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="13de4-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="13de4-134">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="13de4-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

