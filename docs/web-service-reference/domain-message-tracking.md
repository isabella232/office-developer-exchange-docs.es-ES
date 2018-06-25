---
title: Dominio (el seguimiento de mensajes)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Domain
api_type:
- schema
ms.assetid: 4e8e9efa-8885-4ca5-bf90-424e63768dc3
description: El elemento de dominio representa el dominio que se va a buscar.
ms.openlocfilehash: dc161557b59acc580d918f2e196457714bce4ba9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764258"
---
# <a name="domain-message-tracking"></a><span data-ttu-id="3ef55-103">Dominio (el seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="3ef55-103">Domain (Message Tracking)</span></span>

<span data-ttu-id="3ef55-104">El elemento de **dominio** representa el dominio que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="3ef55-104">The **Domain** element represents the domain to search for.</span></span> 
  
```XML
<Domain/>
```

 <span data-ttu-id="3ef55-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="3ef55-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ef55-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3ef55-106">Attributes and elements</span></span>

<span data-ttu-id="3ef55-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3ef55-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ef55-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ef55-108">Attributes</span></span>

<span data-ttu-id="3ef55-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3ef55-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ef55-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3ef55-110">Child elements</span></span>

<span data-ttu-id="3ef55-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3ef55-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3ef55-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3ef55-112">Parent elements</span></span>

|<span data-ttu-id="3ef55-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ef55-113">**Element**</span></span>|<span data-ttu-id="3ef55-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ef55-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ef55-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="3ef55-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="3ef55-116">Contiene los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="3ef55-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3ef55-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3ef55-117">Text value</span></span>

<span data-ttu-id="3ef55-118">Si se usa este elemento, es necesario un valor de texto que representa una cadena.</span><span class="sxs-lookup"><span data-stu-id="3ef55-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ef55-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ef55-119">Remarks</span></span>

<span data-ttu-id="3ef55-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3ef55-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ef55-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3ef55-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ef55-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ef55-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3ef55-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3ef55-123">Schema Name</span></span>  <br/> |<span data-ttu-id="3ef55-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3ef55-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3ef55-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3ef55-125">Validation File</span></span>  <br/> |<span data-ttu-id="3ef55-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3ef55-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3ef55-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3ef55-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="3ef55-128">False</span><span class="sxs-lookup"><span data-stu-id="3ef55-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ef55-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ef55-129">See also</span></span>

- [<span data-ttu-id="3ef55-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3ef55-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

