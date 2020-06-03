---
title: DeliveryRestricted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryRestricted
api_type:
- schema
ms.assetid: 05989915-121c-4f26-93cc-af8d454ab442
description: El elemento DeliveryRestricted indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.
ms.openlocfilehash: 58fc85873326179d7745db4ba7d4854a76ced6a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462692"
---
# <a name="deliveryrestricted"></a><span data-ttu-id="da69f-103">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="da69f-103">DeliveryRestricted</span></span>

<span data-ttu-id="da69f-104">El elemento **DeliveryRestricted** indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.</span><span class="sxs-lookup"><span data-stu-id="da69f-104">The **DeliveryRestricted** element indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
```

 <span data-ttu-id="da69f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="da69f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da69f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="da69f-106">Attributes and elements</span></span>

<span data-ttu-id="da69f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="da69f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da69f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="da69f-108">Attributes</span></span>

<span data-ttu-id="da69f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="da69f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da69f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="da69f-110">Child elements</span></span>

<span data-ttu-id="da69f-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="da69f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="da69f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="da69f-112">Parent elements</span></span>

|<span data-ttu-id="da69f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="da69f-113">**Element**</span></span>|<span data-ttu-id="da69f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da69f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da69f-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="da69f-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="da69f-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="da69f-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da69f-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="da69f-117">Text value</span></span>

<span data-ttu-id="da69f-118">El valor de texto de este elemento es **true** si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.</span><span class="sxs-lookup"><span data-stu-id="da69f-118">The text value of this element is **true** if delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> <span data-ttu-id="da69f-119">El valor es **false** si las restricciones de entrega no impedirán que el mensaje del remitente llegue al destinatario.</span><span class="sxs-lookup"><span data-stu-id="da69f-119">The value is **false** if delivery restrictions will not prevent the sender's message from reaching the recipient.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="da69f-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da69f-120">Remarks</span></span>

<span data-ttu-id="da69f-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="da69f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da69f-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="da69f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da69f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="da69f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da69f-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="da69f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="da69f-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="da69f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="da69f-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="da69f-126">Validation File</span></span>  <br/> |<span data-ttu-id="da69f-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="da69f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da69f-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="da69f-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="da69f-129">Falso</span><span class="sxs-lookup"><span data-stu-id="da69f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da69f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="da69f-130">See also</span></span>

- [<span data-ttu-id="da69f-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="da69f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

