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
description: El elemento DeliveryRestricted indica si las restricciones de entrega impedirá que el mensaje del remitente llegar al destinatario.
ms.openlocfilehash: ba1c6e00b93c9e442a427fe98a5e15bf5fe1effd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764124"
---
# <a name="deliveryrestricted"></a><span data-ttu-id="369e6-103">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="369e6-103">DeliveryRestricted</span></span>

<span data-ttu-id="369e6-104">El elemento **DeliveryRestricted** indica si las restricciones de entrega impedirá que el mensaje del remitente llegar al destinatario.</span><span class="sxs-lookup"><span data-stu-id="369e6-104">The **DeliveryRestricted** element indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
```

 <span data-ttu-id="369e6-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="369e6-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="369e6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="369e6-106">Attributes and elements</span></span>

<span data-ttu-id="369e6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="369e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="369e6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="369e6-108">Attributes</span></span>

<span data-ttu-id="369e6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="369e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="369e6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="369e6-110">Child elements</span></span>

<span data-ttu-id="369e6-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="369e6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="369e6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="369e6-112">Parent elements</span></span>

|<span data-ttu-id="369e6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="369e6-113">**Element**</span></span>|<span data-ttu-id="369e6-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="369e6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="369e6-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="369e6-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="369e6-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="369e6-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="369e6-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="369e6-117">Text value</span></span>

<span data-ttu-id="369e6-118">El valor de texto de este elemento es **true** si las restricciones de entrega impedirá que el mensaje del remitente llegar al destinatario.</span><span class="sxs-lookup"><span data-stu-id="369e6-118">The text value of this element is **true** if delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> <span data-ttu-id="369e6-119">El valor es **false** si las restricciones de entrega no se impide que el mensaje del remitente de llegar al destinatario.</span><span class="sxs-lookup"><span data-stu-id="369e6-119">The value is **false** if delivery restrictions will not prevent the sender's message from reaching the recipient.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="369e6-120">Notas</span><span class="sxs-lookup"><span data-stu-id="369e6-120">Remarks</span></span>

<span data-ttu-id="369e6-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="369e6-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="369e6-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="369e6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="369e6-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="369e6-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="369e6-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="369e6-124">Schema Name</span></span>  <br/> |<span data-ttu-id="369e6-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="369e6-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="369e6-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="369e6-126">Validation File</span></span>  <br/> |<span data-ttu-id="369e6-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="369e6-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="369e6-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="369e6-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="369e6-129">False</span><span class="sxs-lookup"><span data-stu-id="369e6-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="369e6-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="369e6-130">See also</span></span>

- [<span data-ttu-id="369e6-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="369e6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

