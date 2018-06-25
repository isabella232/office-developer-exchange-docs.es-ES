---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: El elemento TextBody especifica el cuerpo de texto.
ms.openlocfilehash: 78b18b27891d571605d2eeeeffb5c252cc790c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840640"
---
# <a name="textbody"></a><span data-ttu-id="72744-103">TextBody</span><span class="sxs-lookup"><span data-stu-id="72744-103">TextBody</span></span>

<span data-ttu-id="72744-104">El elemento **TextBody** especifica el cuerpo de texto.</span><span class="sxs-lookup"><span data-stu-id="72744-104">The **TextBody** element specifies the text body.</span></span> 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 <span data-ttu-id="72744-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="72744-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="72744-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="72744-106">Attributes and elements</span></span>

<span data-ttu-id="72744-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="72744-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72744-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="72744-108">Attributes</span></span>

|<span data-ttu-id="72744-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="72744-109">**Attribute**</span></span>|<span data-ttu-id="72744-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72744-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72744-111">BodyTypeType</span><span class="sxs-lookup"><span data-stu-id="72744-111">BodyTypeType</span></span>  <br/> |<span data-ttu-id="72744-112">Indica el tipo de cuerpo.</span><span class="sxs-lookup"><span data-stu-id="72744-112">Indicates the body type.</span></span> <span data-ttu-id="72744-113">El valor de **texto** para el atributo **BodyTypeType** indica que el cuerpo tiene formato de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="72744-113">The value of **Text** for the **BodyTypeType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="72744-114">El valor de **HTML** para el atributo **BodyTypeType** indica que el cuerpo está en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="72744-114">The value of **HTML** for the **BodyTypeType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="72744-115">Se requiere el atributo **BodyTypeType** .</span><span class="sxs-lookup"><span data-stu-id="72744-115">The **BodyTypeType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="72744-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="72744-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="72744-117">Indica que el contenido del cuerpo se ha truncado.</span><span class="sxs-lookup"><span data-stu-id="72744-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="72744-118">Un valor de texto de **false** para el atributo **IsTruncated** indica que no se ha truncado el contenido del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="72744-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="72744-119">Si la longitud del texto del cuerpo es mayor que el valor establecido en el elemento [MaximumBodySize](maximumbodysize.md) , se truncará el cuerpo normalizado.</span><span class="sxs-lookup"><span data-stu-id="72744-119">The normalized body will be truncated if the text body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="72744-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="72744-120">Child elements</span></span>

<span data-ttu-id="72744-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="72744-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="72744-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="72744-122">Parent elements</span></span>

<span data-ttu-id="72744-123">[Elemento](item.md) | [contacto](contact.md) | [mensaje](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [tarea](task.md)</span><span class="sxs-lookup"><span data-stu-id="72744-123">[Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="72744-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="72744-124">Text value</span></span>

<span data-ttu-id="72744-125">El valor de texto del elemento **TextBody** es el cuerpo de texto del elemento.</span><span class="sxs-lookup"><span data-stu-id="72744-125">The text value of the **TextBody** element is the text body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="72744-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72744-126">Remarks</span></span>

<span data-ttu-id="72744-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="72744-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="72744-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="72744-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72744-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="72744-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72744-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72744-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="72744-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="72744-131">Schema name</span></span>  <br/> |<span data-ttu-id="72744-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="72744-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="72744-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="72744-133">Validation file</span></span>  <br/> |<span data-ttu-id="72744-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="72744-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="72744-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="72744-135">Can be empty</span></span>  <br/> ||
   

