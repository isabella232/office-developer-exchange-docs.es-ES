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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836303"
---
# <a name="mailboxsmtpaddress"></a><span data-ttu-id="9119c-103">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="9119c-103">MailboxSmtpAddress</span></span>

<span data-ttu-id="9119c-104">El elemento **MailboxSmtpAddress** representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada que se va a recuperar o actualizar; o cuya fecha de caducidad de la contraseña se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9119c-104">The **MailboxSmtpAddress** element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved.</span></span> 
  
```XML
<MailboxSmtpAddress/>
```

<span data-ttu-id="9119c-105">**string**</span><span class="sxs-lookup"><span data-stu-id="9119c-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9119c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9119c-106">Attributes and elements</span></span>

<span data-ttu-id="9119c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9119c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9119c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9119c-108">Attributes</span></span>

<span data-ttu-id="9119c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9119c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9119c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9119c-110">Child elements</span></span>

<span data-ttu-id="9119c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9119c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9119c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9119c-112">Parent elements</span></span>

|<span data-ttu-id="9119c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9119c-113">**Element**</span></span>|<span data-ttu-id="9119c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9119c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9119c-115">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="9119c-115">GetInboxRules</span></span>](getinboxrules.md) <br/> |<span data-ttu-id="9119c-116">Define una solicitud para obtener las reglas de bandeja de entrada en un buzón de correo en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="9119c-116">Defines a request to get the Inbox rules on a mailbox in the server store.</span></span>  <br/> |
|[<span data-ttu-id="9119c-117">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="9119c-117">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md) <br/> |<span data-ttu-id="9119c-118">Define una solicitud para obtener la fecha de caducidad de la contraseña de una cuenta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9119c-118">Defines a request to get the password expiration date of an email account.</span></span>  <br/> |
|[<span data-ttu-id="9119c-119">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="9119c-119">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="9119c-120">Define una solicitud para actualizar las reglas de bandeja de entrada en un buzón en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="9119c-120">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9119c-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9119c-121">Text value</span></span>

<span data-ttu-id="9119c-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9119c-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9119c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9119c-123">Remarks</span></span>

<span data-ttu-id="9119c-124">El elemento **MailboxSmtpAddress** es un elemento opcional.</span><span class="sxs-lookup"><span data-stu-id="9119c-124">The **MailboxSmtpAddress** element is an optional element.</span></span> <span data-ttu-id="9119c-125">Si se omite el elemento **MailboxSmtpAddress** , se usa la dirección del usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="9119c-125">If the **MailboxSmtpAddress** element is omitted, the address of the logged on user is used.</span></span> 
  
<span data-ttu-id="9119c-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9119c-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9119c-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9119c-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9119c-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9119c-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9119c-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9119c-129">Schema Name</span></span>  <br/> |<span data-ttu-id="9119c-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9119c-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="9119c-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9119c-131">Validation File</span></span>  <br/> |<span data-ttu-id="9119c-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9119c-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9119c-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9119c-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="9119c-134">Verdadero</span><span class="sxs-lookup"><span data-stu-id="9119c-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9119c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9119c-135">See also</span></span>

- [<span data-ttu-id="9119c-136">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="9119c-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)
- [<span data-ttu-id="9119c-137">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="9119c-137">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="9119c-138">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="9119c-138">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="9119c-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9119c-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

