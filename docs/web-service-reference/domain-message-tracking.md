---
title: Dominio (seguimiento de mensajes)
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
description: El elemento Domain representa el dominio que se va a buscar.
ms.openlocfilehash: 77da9028766881b9bc633e1b3318cd4d70c6b72f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457028"
---
# <a name="domain-message-tracking"></a><span data-ttu-id="0ce2a-103">Dominio (seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="0ce2a-103">Domain (Message Tracking)</span></span>

<span data-ttu-id="0ce2a-104">El elemento **Domain** representa el dominio que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="0ce2a-104">The **Domain** element represents the domain to search for.</span></span> 
  
```XML
<Domain/>
```

 <span data-ttu-id="0ce2a-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="0ce2a-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ce2a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0ce2a-106">Attributes and elements</span></span>

<span data-ttu-id="0ce2a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0ce2a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ce2a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ce2a-108">Attributes</span></span>

<span data-ttu-id="0ce2a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0ce2a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ce2a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ce2a-110">Child elements</span></span>

<span data-ttu-id="0ce2a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0ce2a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0ce2a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ce2a-112">Parent elements</span></span>

|<span data-ttu-id="0ce2a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0ce2a-113">**Element**</span></span>|<span data-ttu-id="0ce2a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ce2a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ce2a-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0ce2a-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="0ce2a-116">Contiene los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="0ce2a-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0ce2a-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0ce2a-117">Text value</span></span>

<span data-ttu-id="0ce2a-118">Si se usa este elemento, se necesita un valor de texto que represente una cadena.</span><span class="sxs-lookup"><span data-stu-id="0ce2a-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ce2a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ce2a-119">Remarks</span></span>

<span data-ttu-id="0ce2a-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ce2a-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ce2a-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0ce2a-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ce2a-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ce2a-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0ce2a-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0ce2a-123">Schema Name</span></span>  <br/> |<span data-ttu-id="0ce2a-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0ce2a-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0ce2a-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0ce2a-125">Validation File</span></span>  <br/> |<span data-ttu-id="0ce2a-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0ce2a-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0ce2a-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0ce2a-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="0ce2a-128">Falso</span><span class="sxs-lookup"><span data-stu-id="0ce2a-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ce2a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ce2a-129">See also</span></span>

- [<span data-ttu-id="0ce2a-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0ce2a-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

