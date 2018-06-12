---
title: GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: El elemento GetPasswordExpirationDate define una solicitud para obtener la fecha de caducidad de contraseña para una cuenta de correo electrónico. Este elemento es el elemento base para la operación de la operación de GetPasswordExpirationDate.
ms.openlocfilehash: a9e0955566372f7b99c48c56e62ce2c5025f9f95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764935"
---
# <a name="getpasswordexpirationdate"></a><span data-ttu-id="2a975-104">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="2a975-104">GetPasswordExpirationDate</span></span>

<span data-ttu-id="2a975-105">El elemento **GetPasswordExpirationDate** define una solicitud para obtener la fecha de caducidad de contraseña para una cuenta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2a975-105">The **GetPasswordExpirationDate** element defines a request to get the password expiration date for an email account.</span></span> <span data-ttu-id="2a975-106">Este elemento es el elemento base para la operación de la [operación de GetPasswordExpirationDate](getpasswordexpirationdate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2a975-106">This element is the base element for the [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation.</span></span> 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 <span data-ttu-id="2a975-107">**GetPasswordExpirationDateType**</span><span class="sxs-lookup"><span data-stu-id="2a975-107">**GetPasswordExpirationDateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a975-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2a975-108">Attributes and elements</span></span>

<span data-ttu-id="2a975-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2a975-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a975-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a975-110">Attributes</span></span>

<span data-ttu-id="2a975-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2a975-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a975-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a975-112">Child elements</span></span>

|<span data-ttu-id="2a975-113">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="2a975-113">**Element name**</span></span>|<span data-ttu-id="2a975-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a975-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a975-115">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="2a975-115">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="2a975-116">Representa la dirección de correo electrónico de la cuenta de correo electrónico para la que es la fecha de caducidad de contraseña que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="2a975-116">Represents the email address of the email account for which the password expiration date is to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a975-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2a975-117">Parent elements</span></span>

<span data-ttu-id="2a975-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2a975-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a975-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a975-119">Remarks</span></span>

<span data-ttu-id="2a975-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2a975-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="2a975-121">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="2a975-121">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a975-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2a975-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a975-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a975-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2a975-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2a975-124">Schema Name</span></span>  <br/> |<span data-ttu-id="2a975-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2a975-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2a975-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2a975-126">Validation File</span></span>  <br/> |<span data-ttu-id="2a975-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2a975-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2a975-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2a975-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="2a975-129">False</span><span class="sxs-lookup"><span data-stu-id="2a975-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a975-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="2a975-130">See also</span></span>



[<span data-ttu-id="2a975-131">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="2a975-131">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)


- [<span data-ttu-id="2a975-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2a975-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

