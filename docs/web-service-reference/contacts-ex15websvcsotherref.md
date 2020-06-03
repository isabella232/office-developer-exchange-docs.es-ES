---
title: Contactos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contacts
api_type:
- schema
ms.assetid: 0cc67cdf-9707-45e7-92c6-fa83a016cdbe
description: El elemento Contacts contiene una lista de contactos que están asociados a una tarea.
ms.openlocfilehash: c2b7bbadd494081a3e47b7b6c489218fab31d574
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458393"
---
# <a name="contacts"></a><span data-ttu-id="351cb-103">Contactos</span><span class="sxs-lookup"><span data-stu-id="351cb-103">Contacts</span></span>

<span data-ttu-id="351cb-104">El elemento **Contacts** contiene una lista de contactos que están asociados a una tarea.</span><span class="sxs-lookup"><span data-stu-id="351cb-104">The **Contacts** element contains a list of contacts that are associated with a task.</span></span> 
  
```xml
<Contacts>
   <String/>
</Contacts>
```

 <span data-ttu-id="351cb-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="351cb-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="351cb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="351cb-106">Attributes and elements</span></span>

<span data-ttu-id="351cb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="351cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="351cb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="351cb-108">Attributes</span></span>

<span data-ttu-id="351cb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="351cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="351cb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="351cb-110">Child elements</span></span>

|<span data-ttu-id="351cb-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="351cb-111">**Element**</span></span>|<span data-ttu-id="351cb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="351cb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="351cb-113">String</span><span class="sxs-lookup"><span data-stu-id="351cb-113">String</span></span>](string.md) <br/> |<span data-ttu-id="351cb-114">Representa una lista de nombres de contactos separados por comas.</span><span class="sxs-lookup"><span data-stu-id="351cb-114">Represents a comma-separated list of contact names.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="351cb-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="351cb-115">Parent elements</span></span>

|<span data-ttu-id="351cb-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="351cb-116">**Element**</span></span>|<span data-ttu-id="351cb-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="351cb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="351cb-118">Tarea</span><span class="sxs-lookup"><span data-stu-id="351cb-118">Task</span></span>](task.md) <br/> |<span data-ttu-id="351cb-119">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="351cb-119">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="351cb-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="351cb-120">Remarks</span></span>

<span data-ttu-id="351cb-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="351cb-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="351cb-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="351cb-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="351cb-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="351cb-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="351cb-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="351cb-124">Schema name</span></span>  <br/> |<span data-ttu-id="351cb-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="351cb-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="351cb-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="351cb-126">Validation file</span></span>  <br/> |<span data-ttu-id="351cb-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="351cb-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="351cb-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="351cb-128">Can be empty</span></span>  <br/> |<span data-ttu-id="351cb-129">Falso</span><span class="sxs-lookup"><span data-stu-id="351cb-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="351cb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="351cb-130">See also</span></span>



- [<span data-ttu-id="351cb-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="351cb-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

