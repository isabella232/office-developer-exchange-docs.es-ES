---
title: IsEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEnabled
api_type:
- schema
ms.assetid: c7e3035e-a4ef-4c11-8cb0-214790a554ff
description: El elemento IsEnabled indica si la regla está habilitada.
ms.openlocfilehash: 7a150dc4a27cf4ff7da9825d1daae2b747088539
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455313"
---
# <a name="isenabled"></a><span data-ttu-id="35502-103">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="35502-103">IsEnabled</span></span>

<span data-ttu-id="35502-104">El elemento **IsEnabled** indica si la regla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="35502-104">The **IsEnabled** element indicates whether the rule is enabled.</span></span> 
  
```XML
<IsEnabled/>
```

 <span data-ttu-id="35502-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="35502-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35502-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="35502-106">Attributes and elements</span></span>

<span data-ttu-id="35502-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="35502-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35502-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="35502-108">Attributes</span></span>

<span data-ttu-id="35502-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="35502-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35502-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="35502-110">Child elements</span></span>

<span data-ttu-id="35502-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="35502-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="35502-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="35502-112">Parent elements</span></span>

|<span data-ttu-id="35502-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="35502-113">**Element**</span></span>|<span data-ttu-id="35502-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35502-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35502-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="35502-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="35502-116">Representa una regla en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="35502-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35502-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="35502-117">Text value</span></span>

<span data-ttu-id="35502-118">Un valor de texto de **true** indica que la regla está habilitada y se puede ejecutar.</span><span class="sxs-lookup"><span data-stu-id="35502-118">A text value of **true** indicates that the rule is enabled and can be executed.</span></span> <span data-ttu-id="35502-119">Un valor de **false** indica que no se puede ejecutar la regla.</span><span class="sxs-lookup"><span data-stu-id="35502-119">A value of **false** indicates that the rule cannot be executed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="35502-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35502-120">Remarks</span></span>

<span data-ttu-id="35502-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="35502-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35502-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="35502-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35502-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="35502-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="35502-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="35502-124">Schema Name</span></span>  <br/> |<span data-ttu-id="35502-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="35502-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="35502-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="35502-126">Validation File</span></span>  <br/> |<span data-ttu-id="35502-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="35502-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="35502-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="35502-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="35502-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="35502-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35502-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="35502-130">See also</span></span>



- [<span data-ttu-id="35502-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="35502-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

