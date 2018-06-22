---
title: ImAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ImAddresses
api_type:
- schema
ms.assetid: 29f614a7-7fe6-47fa-b5f2-8feff106aa99
description: El elemento ImAddresses representa una colección de direcciones de mensajería instantáneas para un contacto.
ms.openlocfilehash: e8c7a22e8537a4526594042905f7bb8454238bf1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835861"
---
# <a name="imaddresses"></a><span data-ttu-id="2dce3-103">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="2dce3-103">ImAddresses</span></span>

<span data-ttu-id="2dce3-104">El elemento **ImAddresses** representa una colección de direcciones de mensajería instantáneas para un contacto.</span><span class="sxs-lookup"><span data-stu-id="2dce3-104">The **ImAddresses** element represents a collection of instant messaging addresses for a contact.</span></span> 
  
```xml
<ImAddresses>
   <Entry/>
</ImAddresses>
```

 <span data-ttu-id="2dce3-105">**ImAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="2dce3-105">**ImAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2dce3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2dce3-106">Attributes and elements</span></span>

<span data-ttu-id="2dce3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2dce3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2dce3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2dce3-108">Attributes</span></span>

<span data-ttu-id="2dce3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2dce3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2dce3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2dce3-110">Child elements</span></span>

|<span data-ttu-id="2dce3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2dce3-111">**Element**</span></span>|<span data-ttu-id="2dce3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dce3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dce3-113">Entrada (IMAddress)</span><span class="sxs-lookup"><span data-stu-id="2dce3-113">Entry (IMAddress)</span></span>](entry-imaddress.md) <br/> |<span data-ttu-id="2dce3-114">Representa una dirección para un contacto de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="2dce3-114">Represents an instant messaging address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2dce3-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2dce3-115">Parent elements</span></span>

|<span data-ttu-id="2dce3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2dce3-116">**Element**</span></span>|<span data-ttu-id="2dce3-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dce3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dce3-118">Contact</span><span class="sxs-lookup"><span data-stu-id="2dce3-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="2dce3-119">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2dce3-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dce3-120">Notas</span><span class="sxs-lookup"><span data-stu-id="2dce3-120">Remarks</span></span>

<span data-ttu-id="2dce3-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2dce3-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2dce3-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2dce3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2dce3-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2dce3-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2dce3-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2dce3-124">Schema name</span></span>  <br/> |<span data-ttu-id="2dce3-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2dce3-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="2dce3-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2dce3-126">Validation file</span></span>  <br/> |<span data-ttu-id="2dce3-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2dce3-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2dce3-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2dce3-128">Can be empty</span></span>  <br/> |<span data-ttu-id="2dce3-129">False</span><span class="sxs-lookup"><span data-stu-id="2dce3-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2dce3-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="2dce3-130">See also</span></span>



- [<span data-ttu-id="2dce3-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2dce3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

