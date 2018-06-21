---
title: Prioridad
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Priority
api_type:
- schema
ms.assetid: e1adb8b9-e3d5-469a-b188-822733d2503e
description: El elemento de prioridad indica el orden en el que es una regla para ejecutarse.
ms.openlocfilehash: 49e9bda063d8766ff49c8a2e9574c986bcfdbeb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19836888"
---
# <a name="priority"></a><span data-ttu-id="1def9-103">Prioridad</span><span class="sxs-lookup"><span data-stu-id="1def9-103">Priority</span></span>

<span data-ttu-id="1def9-104">El elemento de **prioridad** indica el orden en el que es una regla para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="1def9-104">The **Priority** element indicates the order in which a rule is to be run.</span></span> 
  
```XML
<Priority/>
```

 <span data-ttu-id="1def9-105">**int**</span><span class="sxs-lookup"><span data-stu-id="1def9-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1def9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1def9-106">Attributes and elements</span></span>

<span data-ttu-id="1def9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1def9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1def9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1def9-108">Attributes</span></span>

<span data-ttu-id="1def9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1def9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1def9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1def9-110">Child elements</span></span>

<span data-ttu-id="1def9-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1def9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1def9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1def9-112">Parent elements</span></span>

|<span data-ttu-id="1def9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1def9-113">**Element**</span></span>|<span data-ttu-id="1def9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1def9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1def9-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="1def9-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="1def9-116">Representa una regla en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="1def9-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1def9-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1def9-117">Text value</span></span>

<span data-ttu-id="1def9-118">El valor de texto para el elemento de **prioridad** es un entero que indica el orden de ejecución en el que se debe ejecutar una regla.</span><span class="sxs-lookup"><span data-stu-id="1def9-118">The text value for the **Priority** element is an integer that indicates the execution order in which a rule should be run.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1def9-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1def9-119">Remarks</span></span>

<span data-ttu-id="1def9-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1def9-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1def9-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1def9-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1def9-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1def9-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1def9-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1def9-123">Schema Name</span></span>  <br/> |<span data-ttu-id="1def9-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1def9-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1def9-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1def9-125">Validation File</span></span>  <br/> |<span data-ttu-id="1def9-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1def9-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1def9-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1def9-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="1def9-128">False</span><span class="sxs-lookup"><span data-stu-id="1def9-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1def9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1def9-129">See also</span></span>



- [<span data-ttu-id="1def9-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1def9-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

