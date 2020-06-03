---
title: Children
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Children
api_type:
- schema
ms.assetid: ceaffddd-f9bc-43ea-b348-a20fdade738f
description: El elemento Children contiene los nombres de los elementos secundarios de un contacto.
ms.openlocfilehash: de398c93590a4a9ae93b6aa46994c9295d051b84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460228"
---
# <a name="children"></a><span data-ttu-id="5f2ca-103">Children</span><span class="sxs-lookup"><span data-stu-id="5f2ca-103">Children</span></span>

<span data-ttu-id="5f2ca-104">El elemento **Children** contiene los nombres de los elementos secundarios de un contacto.</span><span class="sxs-lookup"><span data-stu-id="5f2ca-104">The **Children** element contains the names of a contact's children.</span></span> 
  
```xml
<Children>
   <String/>
</Children>
```

 <span data-ttu-id="5f2ca-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="5f2ca-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f2ca-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f2ca-106">Attributes and elements</span></span>

<span data-ttu-id="5f2ca-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f2ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f2ca-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f2ca-108">Attributes</span></span>

<span data-ttu-id="5f2ca-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5f2ca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f2ca-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f2ca-110">Child elements</span></span>

|<span data-ttu-id="5f2ca-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f2ca-111">**Element**</span></span>|<span data-ttu-id="5f2ca-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f2ca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f2ca-113">String</span><span class="sxs-lookup"><span data-stu-id="5f2ca-113">String</span></span>](string.md) <br/> |<span data-ttu-id="5f2ca-114">Contiene el nombre del elemento secundario de un contacto.</span><span class="sxs-lookup"><span data-stu-id="5f2ca-114">Contains the name of a contact's child.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f2ca-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f2ca-115">Parent elements</span></span>

|<span data-ttu-id="5f2ca-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f2ca-116">**Element**</span></span>|<span data-ttu-id="5f2ca-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f2ca-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f2ca-118">Contacto</span><span class="sxs-lookup"><span data-stu-id="5f2ca-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5f2ca-119">Representa un contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f2ca-119">Represents a contact in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f2ca-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f2ca-120">Remarks</span></span>

<span data-ttu-id="5f2ca-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5f2ca-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f2ca-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5f2ca-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f2ca-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f2ca-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f2ca-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5f2ca-124">Schema name</span></span>  <br/> |<span data-ttu-id="5f2ca-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5f2ca-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f2ca-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5f2ca-126">Validation file</span></span>  <br/> |<span data-ttu-id="5f2ca-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5f2ca-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f2ca-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5f2ca-128">Can be empty</span></span>  <br/> |<span data-ttu-id="5f2ca-129">Falso</span><span class="sxs-lookup"><span data-stu-id="5f2ca-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f2ca-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f2ca-130">See also</span></span>



- [<span data-ttu-id="5f2ca-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5f2ca-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

