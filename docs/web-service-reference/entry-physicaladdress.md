---
title: Entrada (PhysicalAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: 9e5b6515-453e-4f4c-b55e-6ffefe23c31b
description: El elemento entry describe una única dirección física para un elemento de contacto.
ms.openlocfilehash: 5e8343e9abebeeff8c2b81327b2e0f4ddcf45364
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459633"
---
# <a name="entry-physicaladdress"></a><span data-ttu-id="8d0f4-103">Entrada (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="8d0f4-103">Entry (PhysicalAddress)</span></span>

<span data-ttu-id="8d0f4-104">El elemento **entry** describe una única dirección física para un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-104">The **Entry** element describes a single physical address for a contact item.</span></span> 
  
```xml
<Entry Key="">
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
</Entry>
```

 <span data-ttu-id="8d0f4-105">**PhysicalAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-105">**PhysicalAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d0f4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8d0f4-106">Attributes and elements</span></span>

<span data-ttu-id="8d0f4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d0f4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d0f4-108">Attributes</span></span>

|<span data-ttu-id="8d0f4-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-109">**Attribute**</span></span>|<span data-ttu-id="8d0f4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d0f4-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-111">**Key**</span></span> <br/> | <span data-ttu-id="8d0f4-112">Identifica una dirección física.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-112">Identifies a physical address.</span></span><br/><br/> <span data-ttu-id="8d0f4-113">A continuación se muestran los valores posibles para este atributo:</span><span class="sxs-lookup"><span data-stu-id="8d0f4-113">The following are the possible values for this attribute:</span></span><br/>  <br/><span data-ttu-id="8d0f4-114">-Business</span><span class="sxs-lookup"><span data-stu-id="8d0f4-114">-  Business</span></span>  <br/><span data-ttu-id="8d0f4-115">-Inicio</span><span class="sxs-lookup"><span data-stu-id="8d0f4-115">-  Home</span></span>  <br/><span data-ttu-id="8d0f4-116">-Otros</span><span class="sxs-lookup"><span data-stu-id="8d0f4-116">-  Other</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8d0f4-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d0f4-117">Child elements</span></span>

|<span data-ttu-id="8d0f4-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-118">**Element**</span></span>|<span data-ttu-id="8d0f4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d0f4-120">Drogas</span><span class="sxs-lookup"><span data-stu-id="8d0f4-120">Street</span></span>](street.md) <br/> |<span data-ttu-id="8d0f4-121">Representa la dirección postal de un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-121">Represents a street address for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="8d0f4-122">Ciudad</span><span class="sxs-lookup"><span data-stu-id="8d0f4-122">City</span></span>](city.md) <br/> |<span data-ttu-id="8d0f4-123">Representa el nombre de la ciudad que está asociado a un contacto.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-123">Represents the city name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="8d0f4-124">State</span><span class="sxs-lookup"><span data-stu-id="8d0f4-124">State</span></span>](state-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8d0f4-125">Representa el estado de residencia de un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-125">Represents the state of residence for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="8d0f4-126">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="8d0f4-126">CountryOrRegion</span></span>](countryorregion.md) <br/> |<span data-ttu-id="8d0f4-127">Representa el país o la región de una dirección física determinada.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-127">Represents the country or region for a given physical address.</span></span>  <br/> |
|[<span data-ttu-id="8d0f4-128">PostalCode</span><span class="sxs-lookup"><span data-stu-id="8d0f4-128">PostalCode</span></span>](postalcode.md) <br/> |<span data-ttu-id="8d0f4-129">Representa el código postal de un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-129">Represents the postal code for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8d0f4-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8d0f4-130">Parent elements</span></span>

|<span data-ttu-id="8d0f4-131">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-131">**Element**</span></span>|<span data-ttu-id="8d0f4-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d0f4-133">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="8d0f4-133">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="8d0f4-134">Contiene una colección de direcciones físicas que están asociadas a un contacto.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-134">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d0f4-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d0f4-135">Remarks</span></span>

<span data-ttu-id="8d0f4-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d0f4-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8d0f4-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d0f4-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d0f4-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d0f4-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8d0f4-139">Schema Name</span></span>  <br/> |<span data-ttu-id="8d0f4-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8d0f4-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d0f4-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8d0f4-141">Validation File</span></span>  <br/> |<span data-ttu-id="8d0f4-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8d0f4-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d0f4-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8d0f4-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="8d0f4-144">Falso</span><span class="sxs-lookup"><span data-stu-id="8d0f4-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d0f4-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d0f4-145">See also</span></span>

- [<span data-ttu-id="8d0f4-146">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8d0f4-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="8d0f4-147">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="8d0f4-147">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="8d0f4-148">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="8d0f4-148">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="8d0f4-149">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="8d0f4-149">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

