---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: El elemento MailboxSmtpAddress representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada que se va a recuperar o actualizar; o cuya fecha de caducidad de la contraseña se van a recuperar.
ms.openlocfilehash: 60b2c018f2a05e9630e92e28de1054a421b41e52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836303"
---
# <a name="mailboxsmtpaddress"></a><span data-ttu-id="f4ee8-103">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="f4ee8-103">MailboxSmtpAddress</span></span>

<span data-ttu-id="f4ee8-104">El elemento **MailboxSmtpAddress** representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada que se va a recuperar o actualizar; o cuya fecha de caducidad de la contraseña se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-104">The **MailboxSmtpAddress** element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved.</span></span> 
  
```XML
<MailboxSmtpAddress/>
```

<span data-ttu-id="f4ee8-105">**string**</span><span class="sxs-lookup"><span data-stu-id="f4ee8-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f4ee8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f4ee8-106">Attributes and elements</span></span>

<span data-ttu-id="f4ee8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4ee8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4ee8-108">Attributes</span></span>

<span data-ttu-id="f4ee8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4ee8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4ee8-110">Child elements</span></span>

<span data-ttu-id="f4ee8-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f4ee8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f4ee8-112">Parent elements</span></span>

|<span data-ttu-id="f4ee8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4ee8-113">**Element**</span></span>|<span data-ttu-id="f4ee8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4ee8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4ee8-115">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="f4ee8-115">GetInboxRules</span></span>](getinboxrules.md) <br/> |<span data-ttu-id="f4ee8-116">Define una solicitud para obtener las reglas de bandeja de entrada en un buzón de correo en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-116">Defines a request to get the Inbox rules on a mailbox in the server store.</span></span>  <br/> |
|[<span data-ttu-id="f4ee8-117">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="f4ee8-117">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md) <br/> |<span data-ttu-id="f4ee8-118">Define una solicitud para obtener la fecha de caducidad de la contraseña de una cuenta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-118">Defines a request to get the password expiration date of an email account.</span></span>  <br/> |
|[<span data-ttu-id="f4ee8-119">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="f4ee8-119">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="f4ee8-120">Define una solicitud para actualizar las reglas de bandeja de entrada en un buzón en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-120">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f4ee8-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f4ee8-121">Text value</span></span>

<span data-ttu-id="f4ee8-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4ee8-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4ee8-123">Remarks</span></span>

<span data-ttu-id="f4ee8-124">El elemento **MailboxSmtpAddress** es un elemento opcional.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-124">The **MailboxSmtpAddress** element is an optional element.</span></span> <span data-ttu-id="f4ee8-125">Si se omite el elemento **MailboxSmtpAddress** , se usa la dirección del usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-125">If the **MailboxSmtpAddress** element is omitted, the address of the logged on user is used.</span></span> 
  
<span data-ttu-id="f4ee8-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4ee8-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4ee8-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f4ee8-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4ee8-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4ee8-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f4ee8-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f4ee8-129">Schema Name</span></span>  <br/> |<span data-ttu-id="f4ee8-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f4ee8-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="f4ee8-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f4ee8-131">Validation File</span></span>  <br/> |<span data-ttu-id="f4ee8-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f4ee8-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f4ee8-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f4ee8-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4ee8-134">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f4ee8-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4ee8-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="f4ee8-135">See also</span></span>

- [<span data-ttu-id="f4ee8-136">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="f4ee8-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)
- [<span data-ttu-id="f4ee8-137">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="f4ee8-137">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="f4ee8-138">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="f4ee8-138">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="f4ee8-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f4ee8-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

