---
title: IsSigned
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsSigned
api_type:
- schema
ms.assetid: a4f90fe5-2834-4621-9aa3-b561f74d4674
description: El elemento IsSigned indica si se deben firmar los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: fe8551d01e6f9e813da8936f15b0b7ba1d4ce56c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455530"
---
# <a name="issigned"></a><span data-ttu-id="18938-103">IsSigned</span><span class="sxs-lookup"><span data-stu-id="18938-103">IsSigned</span></span>

<span data-ttu-id="18938-104">El elemento **IsSigned** indica si se deben firmar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="18938-104">The **IsSigned** element indicates whether incoming messages must be signed in order for the condition or exception to apply.</span></span> 
  
```XML
<IsSigned>true | false</IsSigned>
```

 <span data-ttu-id="18938-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="18938-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18938-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="18938-106">Attributes and elements</span></span>

<span data-ttu-id="18938-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="18938-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18938-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="18938-108">Attributes</span></span>

<span data-ttu-id="18938-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="18938-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18938-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18938-110">Child elements</span></span>

<span data-ttu-id="18938-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="18938-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="18938-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="18938-112">Parent elements</span></span>

|<span data-ttu-id="18938-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="18938-113">**Element**</span></span>|<span data-ttu-id="18938-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18938-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18938-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="18938-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="18938-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="18938-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="18938-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="18938-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="18938-118">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="18938-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18938-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="18938-119">Text value</span></span>

<span data-ttu-id="18938-120">Un valor de texto de **true** indica que el mensaje debe estar firmado para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="18938-120">A text value of **true** indicates that the message must be signed in order for the condition or exception to apply.</span></span> <span data-ttu-id="18938-121">Un valor de texto **falso** indica que el mensaje no tiene que estar firmado para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="18938-121">A text value of **false** indicates that the message does not have to be signed for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="18938-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18938-122">Remarks</span></span>

<span data-ttu-id="18938-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="18938-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18938-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="18938-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18938-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="18938-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18938-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="18938-126">Schema Name</span></span>  <br/> |<span data-ttu-id="18938-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="18938-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18938-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="18938-128">Validation File</span></span>  <br/> |<span data-ttu-id="18938-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="18938-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18938-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="18938-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="18938-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="18938-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18938-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="18938-132">See also</span></span>



- [<span data-ttu-id="18938-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="18938-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

