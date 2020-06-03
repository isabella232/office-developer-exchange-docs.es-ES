---
title: Empresas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Companies
api_type:
- schema
ms.assetid: 5d9ea76f-e14d-4424-8842-0c3cc3305119
description: El elemento compañías representa la colección de compañías que están asociadas a un contacto o tarea.
ms.openlocfilehash: eda2b92f3ca874aeeceef6a0935a49a98af0ec39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461453"
---
# <a name="companies"></a><span data-ttu-id="46c4b-103">Empresas</span><span class="sxs-lookup"><span data-stu-id="46c4b-103">Companies</span></span>

<span data-ttu-id="46c4b-104">El elemento **compañías** representa la colección de compañías que están asociadas a un contacto o tarea.</span><span class="sxs-lookup"><span data-stu-id="46c4b-104">The **Companies** element represents the collection of companies that are associated with a contact or task.</span></span> 
  
```xml
<Companies>
   <String/>
</Companies>
```

 <span data-ttu-id="46c4b-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="46c4b-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46c4b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="46c4b-106">Attributes and elements</span></span>

<span data-ttu-id="46c4b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="46c4b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46c4b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="46c4b-108">Attributes</span></span>

<span data-ttu-id="46c4b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="46c4b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46c4b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="46c4b-110">Child elements</span></span>

|<span data-ttu-id="46c4b-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46c4b-111">**Element**</span></span>|<span data-ttu-id="46c4b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46c4b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46c4b-113">String</span><span class="sxs-lookup"><span data-stu-id="46c4b-113">String</span></span>](string.md) <br/> |<span data-ttu-id="46c4b-114">Representa el nombre de una compañía.</span><span class="sxs-lookup"><span data-stu-id="46c4b-114">Represents the name of a company.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46c4b-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="46c4b-115">Parent elements</span></span>

|<span data-ttu-id="46c4b-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46c4b-116">**Element**</span></span>|<span data-ttu-id="46c4b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46c4b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46c4b-118">Contacto</span><span class="sxs-lookup"><span data-stu-id="46c4b-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="46c4b-119">Representa un contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46c4b-119">Represents a contact in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="46c4b-120">Tarea</span><span class="sxs-lookup"><span data-stu-id="46c4b-120">Task</span></span>](task.md) <br/> |<span data-ttu-id="46c4b-121">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46c4b-121">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46c4b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46c4b-122">Remarks</span></span>

<span data-ttu-id="46c4b-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="46c4b-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46c4b-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="46c4b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46c4b-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="46c4b-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="46c4b-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="46c4b-126">Schema name</span></span>  <br/> |<span data-ttu-id="46c4b-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="46c4b-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="46c4b-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="46c4b-128">Validation file</span></span>  <br/> |<span data-ttu-id="46c4b-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="46c4b-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="46c4b-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="46c4b-130">Can be empty</span></span>  <br/> |<span data-ttu-id="46c4b-131">Falso</span><span class="sxs-lookup"><span data-stu-id="46c4b-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46c4b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="46c4b-132">See also</span></span>



- [<span data-ttu-id="46c4b-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="46c4b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

