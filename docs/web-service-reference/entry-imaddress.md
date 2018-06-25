---
title: Entrada (IMAddress)
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
ms.assetid: ee444170-7353-4e86-86c6-d7300a2f1777
description: El elemento de entrada representa una dirección (IM) para un contacto de mensajería instantánea.
ms.openlocfilehash: 77de059cef470dde90ab0b929845cb260b4b867c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764441"
---
# <a name="entry-imaddress"></a><span data-ttu-id="43b42-103">Entrada (IMAddress)</span><span class="sxs-lookup"><span data-stu-id="43b42-103">Entry (IMAddress)</span></span>

<span data-ttu-id="43b42-104">El elemento de **entrada** representa una dirección (IM) para un contacto de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="43b42-104">The **Entry** element represents an instant messaging (IM) address for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="43b42-105">**ImAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="43b42-105">**ImAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43b42-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="43b42-106">Attributes and elements</span></span>

<span data-ttu-id="43b42-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="43b42-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43b42-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="43b42-108">Attributes</span></span>

|<span data-ttu-id="43b42-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="43b42-109">**Attribute**</span></span>|<span data-ttu-id="43b42-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43b42-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="43b42-111">**Clave**</span><span class="sxs-lookup"><span data-stu-id="43b42-111">**Key**</span></span> <br/> | <span data-ttu-id="43b42-112">Identifica la dirección de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="43b42-112">Identifies the IM address.</span></span><br/><br/><span data-ttu-id="43b42-113">Los siguientes son los valores posibles para este atributo:</span><span class="sxs-lookup"><span data-stu-id="43b42-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="43b42-114">-ImAddress1</span><span class="sxs-lookup"><span data-stu-id="43b42-114">-  ImAddress1</span></span>  <br/><span data-ttu-id="43b42-115">-ImAddress2</span><span class="sxs-lookup"><span data-stu-id="43b42-115">-  ImAddress2</span></span>  <br/><span data-ttu-id="43b42-116">-ImAddress3</span><span class="sxs-lookup"><span data-stu-id="43b42-116">-  ImAddress3</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="43b42-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="43b42-117">Child elements</span></span>

<span data-ttu-id="43b42-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="43b42-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43b42-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="43b42-119">Parent elements</span></span>

|<span data-ttu-id="43b42-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="43b42-120">**Element**</span></span>|<span data-ttu-id="43b42-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43b42-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43b42-122">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="43b42-122">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="43b42-123">Representa una colección de direcciones de mensajería instantánea para un contacto.</span><span class="sxs-lookup"><span data-stu-id="43b42-123">Represents a collection of IM addresses for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43b42-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="43b42-124">Text value</span></span>

<span data-ttu-id="43b42-125">Si se usa este elemento, es necesario un valor de texto que representa la dirección de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="43b42-125">A text value that represents the IM address is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43b42-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43b42-126">Remarks</span></span>

<span data-ttu-id="43b42-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="43b42-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43b42-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="43b42-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43b42-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="43b42-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43b42-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="43b42-130">Schema name</span></span>  <br/> |<span data-ttu-id="43b42-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="43b42-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="43b42-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="43b42-132">Validation file</span></span>  <br/> |<span data-ttu-id="43b42-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="43b42-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43b42-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="43b42-134">Can be empty</span></span>  <br/> |<span data-ttu-id="43b42-135">False</span><span class="sxs-lookup"><span data-stu-id="43b42-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43b42-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="43b42-136">See also</span></span>

- [<span data-ttu-id="43b42-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="43b42-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="43b42-138">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="43b42-138">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="43b42-139">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="43b42-139">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="43b42-140">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="43b42-140">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

