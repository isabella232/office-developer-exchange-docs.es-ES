---
title: Entrada (PhoneNumber)
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
ms.assetid: e3d0a4d5-8af8-4607-aa2e-ef3111b63b55
description: El elemento entry representa un número de teléfono de un contacto.
ms.openlocfilehash: 62f7091bb750dc7ca74b1e5637a437e2cdad4f1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459640"
---
# <a name="entry-phonenumber"></a><span data-ttu-id="20e48-103">Entrada (PhoneNumber)</span><span class="sxs-lookup"><span data-stu-id="20e48-103">Entry (PhoneNumber)</span></span>

<span data-ttu-id="20e48-104">El elemento **entry** representa un número de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="20e48-104">The **Entry** element represents a telephone number for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="20e48-105">**PhoneNumberDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="20e48-105">**PhoneNumberDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20e48-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="20e48-106">Attributes and elements</span></span>

<span data-ttu-id="20e48-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="20e48-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20e48-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="20e48-108">Attributes</span></span>

|<span data-ttu-id="20e48-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="20e48-109">**Attribute**</span></span>|<span data-ttu-id="20e48-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20e48-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20e48-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="20e48-111">**Key**</span></span> <br/> | <span data-ttu-id="20e48-112">Identifica el número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="20e48-112">Identifies the telephone number.</span></span> <span data-ttu-id="20e48-113">El atributo key es del tipo **PhoneNumberKeyType**.</span><span class="sxs-lookup"><span data-stu-id="20e48-113">The Key attribute is of type **PhoneNumberKeyType**.</span></span><br/><br/> <span data-ttu-id="20e48-114">A continuación se muestran los valores posibles para este atributo:</span><span class="sxs-lookup"><span data-stu-id="20e48-114">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="20e48-115">- AssistantPhone</span><span class="sxs-lookup"><span data-stu-id="20e48-115">-  AssistantPhone</span></span>  <br/><span data-ttu-id="20e48-116">- BusinessFax</span><span class="sxs-lookup"><span data-stu-id="20e48-116">-  BusinessFax</span></span>  <br/><span data-ttu-id="20e48-117">- BusinessPhone</span><span class="sxs-lookup"><span data-stu-id="20e48-117">-  BusinessPhone</span></span>  <br/><span data-ttu-id="20e48-118">- BusinessPhone2</span><span class="sxs-lookup"><span data-stu-id="20e48-118">-  BusinessPhone2</span></span>  <br/><span data-ttu-id="20e48-119">-Callback</span><span class="sxs-lookup"><span data-stu-id="20e48-119">-  Callback</span></span>  <br/><span data-ttu-id="20e48-120">- CarPhone</span><span class="sxs-lookup"><span data-stu-id="20e48-120">-  CarPhone</span></span>  <br/><span data-ttu-id="20e48-121">- CompanyMainPhone</span><span class="sxs-lookup"><span data-stu-id="20e48-121">-  CompanyMainPhone</span></span>  <br/><span data-ttu-id="20e48-122">- HomeFax</span><span class="sxs-lookup"><span data-stu-id="20e48-122">-  HomeFax</span></span>  <br/><span data-ttu-id="20e48-123">-HomePhone</span><span class="sxs-lookup"><span data-stu-id="20e48-123">-  HomePhone</span></span>  <br/><span data-ttu-id="20e48-124">- HomePhone2</span><span class="sxs-lookup"><span data-stu-id="20e48-124">-  HomePhone2</span></span>  <br/><span data-ttu-id="20e48-125">ISDN (RDSI)</span><span class="sxs-lookup"><span data-stu-id="20e48-125">-  Isdn</span></span>  <br/><span data-ttu-id="20e48-126">-MobilePhone</span><span class="sxs-lookup"><span data-stu-id="20e48-126">-  MobilePhone</span></span>  <br/><span data-ttu-id="20e48-127">-OtherFax</span><span class="sxs-lookup"><span data-stu-id="20e48-127">-  OtherFax</span></span>  <br/><span data-ttu-id="20e48-128">-OtherTelephone</span><span class="sxs-lookup"><span data-stu-id="20e48-128">-  OtherTelephone</span></span>  <br/><span data-ttu-id="20e48-129">-Buscapersonas</span><span class="sxs-lookup"><span data-stu-id="20e48-129">-  Pager</span></span>  <br/><span data-ttu-id="20e48-130">- PrimaryPhone</span><span class="sxs-lookup"><span data-stu-id="20e48-130">-  PrimaryPhone</span></span>  <br/><span data-ttu-id="20e48-131">-Radioteléfono</span><span class="sxs-lookup"><span data-stu-id="20e48-131">-  RadioPhone</span></span>  <br/><span data-ttu-id="20e48-132">-Télex</span><span class="sxs-lookup"><span data-stu-id="20e48-132">-  Telex</span></span>  <br/><span data-ttu-id="20e48-133">- TtyTddPhone</span><span class="sxs-lookup"><span data-stu-id="20e48-133">-  TtyTddPhone</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="20e48-134">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="20e48-134">Child elements</span></span>

<span data-ttu-id="20e48-135">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="20e48-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20e48-136">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="20e48-136">Parent elements</span></span>

|<span data-ttu-id="20e48-137">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="20e48-137">**Element**</span></span>|<span data-ttu-id="20e48-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20e48-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20e48-139">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="20e48-139">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="20e48-140">Representa una colección de números de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="20e48-140">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="20e48-141">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="20e48-141">Text value</span></span>

<span data-ttu-id="20e48-142">Si se usa este elemento, es necesario un valor de texto que representa un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="20e48-142">A text value that represents a telephone number is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20e48-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20e48-143">Remarks</span></span>

<span data-ttu-id="20e48-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="20e48-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20e48-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="20e48-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20e48-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="20e48-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="20e48-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="20e48-147">Schema name</span></span>  <br/> |<span data-ttu-id="20e48-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="20e48-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="20e48-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="20e48-149">Validation file</span></span>  <br/> |<span data-ttu-id="20e48-150">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="20e48-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="20e48-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="20e48-151">Can be empty</span></span>  <br/> |<span data-ttu-id="20e48-152">Falso</span><span class="sxs-lookup"><span data-stu-id="20e48-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20e48-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="20e48-153">See also</span></span>

- [<span data-ttu-id="20e48-154">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="20e48-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="20e48-155">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="20e48-155">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="20e48-156">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="20e48-156">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="20e48-157">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="20e48-157">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

