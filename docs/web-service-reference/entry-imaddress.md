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
description: El elemento entry representa una dirección de mensajería instantánea (mi) de un contacto.
ms.openlocfilehash: b6cc37447eb0f231e9e852a6c3cd64d6e1f3a89f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460704"
---
# <a name="entry-imaddress"></a><span data-ttu-id="005a4-103">Entrada (IMAddress)</span><span class="sxs-lookup"><span data-stu-id="005a4-103">Entry (IMAddress)</span></span>

<span data-ttu-id="005a4-104">El elemento **entry** representa una dirección de mensajería instantánea (mi) de un contacto.</span><span class="sxs-lookup"><span data-stu-id="005a4-104">The **Entry** element represents an instant messaging (IM) address for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="005a4-105">**ImAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="005a4-105">**ImAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="005a4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="005a4-106">Attributes and elements</span></span>

<span data-ttu-id="005a4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="005a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="005a4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="005a4-108">Attributes</span></span>

|<span data-ttu-id="005a4-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="005a4-109">**Attribute**</span></span>|<span data-ttu-id="005a4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="005a4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="005a4-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="005a4-111">**Key**</span></span> <br/> | <span data-ttu-id="005a4-112">Identifica la dirección de mi.</span><span class="sxs-lookup"><span data-stu-id="005a4-112">Identifies the IM address.</span></span><br/><br/><span data-ttu-id="005a4-113">A continuación se muestran los valores posibles para este atributo:</span><span class="sxs-lookup"><span data-stu-id="005a4-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="005a4-114">- ImAddress1</span><span class="sxs-lookup"><span data-stu-id="005a4-114">-  ImAddress1</span></span>  <br/><span data-ttu-id="005a4-115">- ImAddress2</span><span class="sxs-lookup"><span data-stu-id="005a4-115">-  ImAddress2</span></span>  <br/><span data-ttu-id="005a4-116">- ImAddress3</span><span class="sxs-lookup"><span data-stu-id="005a4-116">-  ImAddress3</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="005a4-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="005a4-117">Child elements</span></span>

<span data-ttu-id="005a4-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="005a4-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="005a4-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="005a4-119">Parent elements</span></span>

|<span data-ttu-id="005a4-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="005a4-120">**Element**</span></span>|<span data-ttu-id="005a4-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="005a4-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="005a4-122">Indirecciones</span><span class="sxs-lookup"><span data-stu-id="005a4-122">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="005a4-123">Representa una colección de direcciones de mensajería instantánea de un contacto.</span><span class="sxs-lookup"><span data-stu-id="005a4-123">Represents a collection of IM addresses for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="005a4-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="005a4-124">Text value</span></span>

<span data-ttu-id="005a4-125">Si se usa este elemento, se requiere un valor de texto que represente la dirección de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="005a4-125">A text value that represents the IM address is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="005a4-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="005a4-126">Remarks</span></span>

<span data-ttu-id="005a4-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="005a4-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="005a4-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="005a4-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="005a4-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="005a4-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="005a4-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="005a4-130">Schema name</span></span>  <br/> |<span data-ttu-id="005a4-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="005a4-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="005a4-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="005a4-132">Validation file</span></span>  <br/> |<span data-ttu-id="005a4-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="005a4-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="005a4-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="005a4-134">Can be empty</span></span>  <br/> |<span data-ttu-id="005a4-135">Falso</span><span class="sxs-lookup"><span data-stu-id="005a4-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="005a4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="005a4-136">See also</span></span>

- [<span data-ttu-id="005a4-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="005a4-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="005a4-138">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="005a4-138">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="005a4-139">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="005a4-139">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="005a4-140">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="005a4-140">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

