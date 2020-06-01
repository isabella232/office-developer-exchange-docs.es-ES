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
description: El elemento IsInError indica si la regla se encuentra en una condición de error.
ms.openlocfilehash: 9e642c9f89434bdcad97b0c16dc35f99196051d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464220"
---
# <a name="isinerror"></a><span data-ttu-id="3d463-103">IsInError</span><span class="sxs-lookup"><span data-stu-id="3d463-103">IsInError</span></span>

<span data-ttu-id="3d463-104">El elemento **IsInError** indica si la regla se encuentra en una condición de error.</span><span class="sxs-lookup"><span data-stu-id="3d463-104">The **IsInError** element indicates whether the rule is in an error condition.</span></span> 
  
```XML
<IsInError/>
```

 <span data-ttu-id="3d463-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3d463-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3d463-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3d463-106">Attributes and elements</span></span>

<span data-ttu-id="3d463-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3d463-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d463-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3d463-108">Attributes</span></span>

<span data-ttu-id="3d463-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3d463-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3d463-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3d463-110">Child elements</span></span>

<span data-ttu-id="3d463-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3d463-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3d463-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3d463-112">Parent elements</span></span>

|<span data-ttu-id="3d463-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3d463-113">**Element**</span></span>|<span data-ttu-id="3d463-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3d463-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d463-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="3d463-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="3d463-116">Representa una regla en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="3d463-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3d463-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3d463-117">Text value</span></span>

<span data-ttu-id="3d463-118">Un valor de texto de **true** indica que la regla está en una condición de error.</span><span class="sxs-lookup"><span data-stu-id="3d463-118">A text value of **true** indicates that the rule is in an error condition.</span></span> <span data-ttu-id="3d463-119">Un valor de **false** indica que la regla no se encuentra en una condición de error.</span><span class="sxs-lookup"><span data-stu-id="3d463-119">A value of **false** indicates that the rule is not in an error condition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3d463-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d463-120">Remarks</span></span>

<span data-ttu-id="3d463-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3d463-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d463-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3d463-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d463-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d463-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3d463-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3d463-124">Schema Name</span></span>  <br/> |<span data-ttu-id="3d463-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3d463-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3d463-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3d463-126">Validation File</span></span>  <br/> |<span data-ttu-id="3d463-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3d463-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3d463-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3d463-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="3d463-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="3d463-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d463-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d463-130">See also</span></span>



- [<span data-ttu-id="3d463-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3d463-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

