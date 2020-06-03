---
title: Priority
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
description: El elemento Priority indica el orden en que se ejecutará una regla.
ms.openlocfilehash: a5a894bba583618dd04430fc89f125c8920b0202
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462405"
---
# <a name="priority"></a><span data-ttu-id="0519b-103">Priority</span><span class="sxs-lookup"><span data-stu-id="0519b-103">Priority</span></span>

<span data-ttu-id="0519b-104">El elemento **Priority** indica el orden en que se ejecutará una regla.</span><span class="sxs-lookup"><span data-stu-id="0519b-104">The **Priority** element indicates the order in which a rule is to be run.</span></span> 
  
```XML
<Priority/>
```

 <span data-ttu-id="0519b-105">**int**</span><span class="sxs-lookup"><span data-stu-id="0519b-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0519b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0519b-106">Attributes and elements</span></span>

<span data-ttu-id="0519b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0519b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0519b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0519b-108">Attributes</span></span>

<span data-ttu-id="0519b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0519b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0519b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0519b-110">Child elements</span></span>

<span data-ttu-id="0519b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0519b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0519b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0519b-112">Parent elements</span></span>

|<span data-ttu-id="0519b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0519b-113">**Element**</span></span>|<span data-ttu-id="0519b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0519b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0519b-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="0519b-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="0519b-116">Representa una regla en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="0519b-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0519b-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0519b-117">Text value</span></span>

<span data-ttu-id="0519b-118">El valor de texto del elemento **Priority** es un entero que indica el orden de ejecución en el que debe ejecutarse una regla.</span><span class="sxs-lookup"><span data-stu-id="0519b-118">The text value for the **Priority** element is an integer that indicates the execution order in which a rule should be run.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0519b-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0519b-119">Remarks</span></span>

<span data-ttu-id="0519b-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0519b-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0519b-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0519b-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0519b-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0519b-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0519b-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0519b-123">Schema Name</span></span>  <br/> |<span data-ttu-id="0519b-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0519b-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0519b-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0519b-125">Validation File</span></span>  <br/> |<span data-ttu-id="0519b-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0519b-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0519b-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0519b-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="0519b-128">Falso</span><span class="sxs-lookup"><span data-stu-id="0519b-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0519b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0519b-129">See also</span></span>



- [<span data-ttu-id="0519b-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0519b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

