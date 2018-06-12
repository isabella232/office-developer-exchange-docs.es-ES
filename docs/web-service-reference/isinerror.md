---
title: IsInError
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsInError
api_type:
- schema
ms.assetid: f56e6c31-a566-4761-8755-d90ffe6fe790
description: El elemento IsInError indica si la regla está en una condición de error.
ms.openlocfilehash: 9f77bbe11106174d0e82c5257e08c3728d67c60c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836033"
---
# <a name="isinerror"></a><span data-ttu-id="e0047-103">IsInError</span><span class="sxs-lookup"><span data-stu-id="e0047-103">IsInError</span></span>

<span data-ttu-id="e0047-104">El elemento **IsInError** indica si la regla está en una condición de error.</span><span class="sxs-lookup"><span data-stu-id="e0047-104">The **IsInError** element indicates whether the rule is in an error condition.</span></span> 
  
```XML
<IsInError/>
```

 <span data-ttu-id="e0047-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0047-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0047-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0047-106">Attributes and elements</span></span>

<span data-ttu-id="e0047-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0047-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0047-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0047-108">Attributes</span></span>

<span data-ttu-id="e0047-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0047-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0047-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0047-110">Child elements</span></span>

<span data-ttu-id="e0047-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0047-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e0047-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0047-112">Parent elements</span></span>

|<span data-ttu-id="e0047-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0047-113">**Element**</span></span>|<span data-ttu-id="e0047-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0047-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0047-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="e0047-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="e0047-116">Representa una regla en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="e0047-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e0047-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e0047-117">Text value</span></span>

<span data-ttu-id="e0047-118">Un valor de texto de **true** indica que la regla está en una condición de error.</span><span class="sxs-lookup"><span data-stu-id="e0047-118">A text value of **true** indicates that the rule is in an error condition.</span></span> <span data-ttu-id="e0047-119">Un valor de **false** indica que la regla no está en una condición de error.</span><span class="sxs-lookup"><span data-stu-id="e0047-119">A value of **false** indicates that the rule is not in an error condition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e0047-120">Notas</span><span class="sxs-lookup"><span data-stu-id="e0047-120">Remarks</span></span>

<span data-ttu-id="e0047-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0047-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0047-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0047-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0047-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e0047-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0047-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0047-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e0047-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e0047-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0047-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0047-126">Validation File</span></span>  <br/> |<span data-ttu-id="e0047-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e0047-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0047-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0047-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0047-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e0047-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0047-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="e0047-130">See also</span></span>



- [<span data-ttu-id="e0047-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e0047-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

