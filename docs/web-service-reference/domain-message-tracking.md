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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764258"
---
# <a name="domain-message-tracking"></a><span data-ttu-id="eea04-103">Dominio (el seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="eea04-103">Domain (Message Tracking)</span></span>

<span data-ttu-id="eea04-104">El elemento de **dominio** representa el dominio que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="eea04-104">The **Domain** element represents the domain to search for.</span></span> 
  
```XML
<Domain/>
```

 <span data-ttu-id="eea04-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="eea04-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eea04-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eea04-106">Attributes and elements</span></span>

<span data-ttu-id="eea04-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eea04-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eea04-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eea04-108">Attributes</span></span>

<span data-ttu-id="eea04-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eea04-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eea04-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eea04-110">Child elements</span></span>

<span data-ttu-id="eea04-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eea04-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eea04-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eea04-112">Parent elements</span></span>

|<span data-ttu-id="eea04-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eea04-113">**Element**</span></span>|<span data-ttu-id="eea04-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eea04-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eea04-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="eea04-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="eea04-116">Contiene los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="eea04-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eea04-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eea04-117">Text value</span></span>

<span data-ttu-id="eea04-118">Si se usa este elemento, es necesario un valor de texto que representa una cadena.</span><span class="sxs-lookup"><span data-stu-id="eea04-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eea04-119">Notas</span><span class="sxs-lookup"><span data-stu-id="eea04-119">Remarks</span></span>

<span data-ttu-id="eea04-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eea04-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eea04-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eea04-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eea04-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eea04-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eea04-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eea04-123">Schema Name</span></span>  <br/> |<span data-ttu-id="eea04-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eea04-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eea04-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eea04-125">Validation File</span></span>  <br/> |<span data-ttu-id="eea04-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eea04-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eea04-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eea04-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="eea04-128">False</span><span class="sxs-lookup"><span data-stu-id="eea04-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eea04-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="eea04-129">See also</span></span>

- [<span data-ttu-id="eea04-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="eea04-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

