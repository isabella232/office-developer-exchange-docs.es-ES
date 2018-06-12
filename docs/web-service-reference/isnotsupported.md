---
title: IsNotSupported
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNotSupported
api_type:
- schema
ms.assetid: 4db469ae-1515-47ea-9905-6aabf199febd
description: El elemento IsNotSupported indica si la regla no se puede modificar mediante el uso de la API de código administrado.
ms.openlocfilehash: 2468d47dbfdcaf1a28ed1a4afb1e7ea60147d1dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836057"
---
# <a name="isnotsupported"></a><span data-ttu-id="c1666-103">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="c1666-103">IsNotSupported</span></span>

<span data-ttu-id="c1666-104">El elemento **IsNotSupported** indica si la regla no se puede modificar mediante el uso de la API de código administrado.</span><span class="sxs-lookup"><span data-stu-id="c1666-104">The **IsNotSupported** element indicates whether the rule cannot be modified by using the managed code APIs.</span></span> 
  
```XML
<IsNotSupported/>
```

 <span data-ttu-id="c1666-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c1666-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1666-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1666-106">Attributes and elements</span></span>

<span data-ttu-id="c1666-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1666-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1666-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1666-108">Attributes</span></span>

<span data-ttu-id="c1666-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1666-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1666-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1666-110">Child elements</span></span>

<span data-ttu-id="c1666-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1666-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1666-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1666-112">Parent elements</span></span>

|<span data-ttu-id="c1666-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1666-113">**Element**</span></span>|<span data-ttu-id="c1666-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1666-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1666-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="c1666-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="c1666-116">Representa una regla en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="c1666-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1666-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c1666-117">Text value</span></span>

<span data-ttu-id="c1666-118">Un valor de texto de **true** indica que la regla no se puede modificar mediante el uso de la API de código administrado.</span><span class="sxs-lookup"><span data-stu-id="c1666-118">A text value of **true** indicates that the rule cannot be modified by using the managed code APIs.</span></span> <span data-ttu-id="c1666-119">Un valor de **false** indica que la regla puede modificarse mediante el uso de la API de código administrado.</span><span class="sxs-lookup"><span data-stu-id="c1666-119">A value of **false** indicates that the rule can be modified by using the managed code APIs.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c1666-120">Notas</span><span class="sxs-lookup"><span data-stu-id="c1666-120">Remarks</span></span>

<span data-ttu-id="c1666-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1666-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1666-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1666-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1666-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1666-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1666-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1666-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c1666-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c1666-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1666-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1666-126">Validation File</span></span>  <br/> |<span data-ttu-id="c1666-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c1666-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1666-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1666-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1666-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c1666-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1666-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="c1666-130">See also</span></span>



- [<span data-ttu-id="c1666-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c1666-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

