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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460228"
---
# <a name="children"></a><span data-ttu-id="c6aa3-103">Children</span><span class="sxs-lookup"><span data-stu-id="c6aa3-103">Children</span></span>

<span data-ttu-id="c6aa3-104">El elemento **Children** contiene los nombres de los elementos secundarios de un contacto.</span><span class="sxs-lookup"><span data-stu-id="c6aa3-104">The **Children** element contains the names of a contact's children.</span></span> 
  
```xml
<Children>
   <String/>
</Children>
```

 <span data-ttu-id="c6aa3-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="c6aa3-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6aa3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c6aa3-106">Attributes and elements</span></span>

<span data-ttu-id="c6aa3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c6aa3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6aa3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c6aa3-108">Attributes</span></span>

<span data-ttu-id="c6aa3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c6aa3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6aa3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c6aa3-110">Child elements</span></span>

|<span data-ttu-id="c6aa3-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c6aa3-111">**Element**</span></span>|<span data-ttu-id="c6aa3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6aa3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6aa3-113">String</span><span class="sxs-lookup"><span data-stu-id="c6aa3-113">String</span></span>](string.md) <br/> |<span data-ttu-id="c6aa3-114">Contiene el nombre del elemento secundario de un contacto.</span><span class="sxs-lookup"><span data-stu-id="c6aa3-114">Contains the name of a contact's child.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c6aa3-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c6aa3-115">Parent elements</span></span>

|<span data-ttu-id="c6aa3-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c6aa3-116">**Element**</span></span>|<span data-ttu-id="c6aa3-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6aa3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6aa3-118">Contacto</span><span class="sxs-lookup"><span data-stu-id="c6aa3-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c6aa3-119">Representa un contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c6aa3-119">Represents a contact in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6aa3-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6aa3-120">Remarks</span></span>

<span data-ttu-id="c6aa3-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c6aa3-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6aa3-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c6aa3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6aa3-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6aa3-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c6aa3-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c6aa3-124">Schema name</span></span>  <br/> |<span data-ttu-id="c6aa3-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c6aa3-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c6aa3-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c6aa3-126">Validation file</span></span>  <br/> |<span data-ttu-id="c6aa3-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c6aa3-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c6aa3-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c6aa3-128">Can be empty</span></span>  <br/> |<span data-ttu-id="c6aa3-129">Falso</span><span class="sxs-lookup"><span data-stu-id="c6aa3-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6aa3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6aa3-130">See also</span></span>



- [<span data-ttu-id="c6aa3-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c6aa3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

