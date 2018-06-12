---
title: Identificador de regla
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RuleId
api_type:
- schema
ms.assetid: 456e3c34-e536-456a-ac40-7fd4f94c0bad
description: El elemento de identificador de regla especifica un identificador de regla.
ms.openlocfilehash: 4dfa71c9fb6ee362d776487952199f2430e5e4a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837260"
---
# <a name="ruleid"></a><span data-ttu-id="83772-103">Identificador de regla</span><span class="sxs-lookup"><span data-stu-id="83772-103">RuleId</span></span>

<span data-ttu-id="83772-104">El elemento de **identificador de regla** especifica un identificador de regla.</span><span class="sxs-lookup"><span data-stu-id="83772-104">The **RuleId** element specifies a rule identifier.</span></span> 
  
```XML
<RuleId/>
```

 <span data-ttu-id="83772-105">**string**</span><span class="sxs-lookup"><span data-stu-id="83772-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83772-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="83772-106">Attributes and elements</span></span>

<span data-ttu-id="83772-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="83772-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83772-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="83772-108">Attributes</span></span>

<span data-ttu-id="83772-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83772-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83772-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83772-110">Child elements</span></span>

<span data-ttu-id="83772-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83772-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="83772-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="83772-112">Parent elements</span></span>

|<span data-ttu-id="83772-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="83772-113">**Element**</span></span>|<span data-ttu-id="83772-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83772-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83772-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="83772-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="83772-116">Representa una regla en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="83772-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="83772-117">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="83772-117">DeleteRuleOperation</span></span>](deleteruleoperation.md) <br/> |<span data-ttu-id="83772-118">Representa la operación para eliminar una regla de bandeja de entrada existente.</span><span class="sxs-lookup"><span data-stu-id="83772-118">Represents the operation to delete an existing Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83772-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="83772-119">Text value</span></span>

<span data-ttu-id="83772-120">El valor de texto es un valor de tipo string que representa la regla.</span><span class="sxs-lookup"><span data-stu-id="83772-120">The text value is a string value that represents the rule.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83772-121">Notas</span><span class="sxs-lookup"><span data-stu-id="83772-121">Remarks</span></span>

<span data-ttu-id="83772-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="83772-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83772-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="83772-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83772-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83772-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="83772-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="83772-125">Schema Name</span></span>  <br/> |<span data-ttu-id="83772-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="83772-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="83772-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="83772-127">Validation File</span></span>  <br/> |<span data-ttu-id="83772-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="83772-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="83772-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="83772-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="83772-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="83772-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83772-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="83772-131">See also</span></span>



- [<span data-ttu-id="83772-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="83772-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

