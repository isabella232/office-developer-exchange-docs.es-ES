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
description: El elemento MailboxSmtpAddress representa la dirección SMTP del usuario cuyas reglas de la bandeja de entrada se van a recuperar o actualizar; o cuya fecha de expiración de contraseña se va a recuperar.
ms.openlocfilehash: 613e8098210257280bec47f2b22a2d29d04fa07c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530547"
---
# <a name="mailboxsmtpaddress"></a><span data-ttu-id="c7e8a-103">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c7e8a-103">MailboxSmtpAddress</span></span>

<span data-ttu-id="c7e8a-104">El elemento **MailboxSmtpAddress** representa la dirección SMTP del usuario cuyas reglas de la bandeja de entrada se van a recuperar o actualizar; o cuya fecha de expiración de contraseña se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-104">The **MailboxSmtpAddress** element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved.</span></span> 
  
```XML
<MailboxSmtpAddress/>
```

<span data-ttu-id="c7e8a-105">**string**</span><span class="sxs-lookup"><span data-stu-id="c7e8a-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c7e8a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7e8a-106">Attributes and elements</span></span>

<span data-ttu-id="c7e8a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7e8a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7e8a-108">Attributes</span></span>

<span data-ttu-id="c7e8a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7e8a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7e8a-110">Child elements</span></span>

<span data-ttu-id="c7e8a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7e8a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7e8a-112">Parent elements</span></span>

|<span data-ttu-id="c7e8a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c7e8a-113">**Element**</span></span>|<span data-ttu-id="c7e8a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7e8a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7e8a-115">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c7e8a-115">GetInboxRules</span></span>](getinboxrules.md) <br/> |<span data-ttu-id="c7e8a-116">Define una solicitud para obtener las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-116">Defines a request to get the Inbox rules on a mailbox in the server store.</span></span>  <br/> |
|[<span data-ttu-id="c7e8a-117">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="c7e8a-117">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md) <br/> |<span data-ttu-id="c7e8a-118">Define una solicitud para obtener la fecha de expiración de la contraseña de una cuenta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-118">Defines a request to get the password expiration date of an email account.</span></span>  <br/> |
|[<span data-ttu-id="c7e8a-119">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c7e8a-119">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="c7e8a-120">Define una solicitud para actualizar las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-120">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c7e8a-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c7e8a-121">Text value</span></span>

<span data-ttu-id="c7e8a-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7e8a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7e8a-123">Remarks</span></span>

<span data-ttu-id="c7e8a-124">El elemento **MailboxSmtpAddress** es un elemento opcional.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-124">The **MailboxSmtpAddress** element is an optional element.</span></span> <span data-ttu-id="c7e8a-125">Si se omite el elemento **MailboxSmtpAddress** , se usa la dirección del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-125">If the **MailboxSmtpAddress** element is omitted, the address of the logged on user is used.</span></span> 
  
<span data-ttu-id="c7e8a-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7e8a-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7e8a-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7e8a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7e8a-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7e8a-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7e8a-129">Schema Name</span></span>  <br/> |<span data-ttu-id="c7e8a-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c7e8a-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="c7e8a-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7e8a-131">Validation File</span></span>  <br/> |<span data-ttu-id="c7e8a-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c7e8a-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7e8a-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7e8a-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7e8a-134">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c7e8a-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7e8a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7e8a-135">See also</span></span>

- [<span data-ttu-id="c7e8a-136">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c7e8a-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)
- [<span data-ttu-id="c7e8a-137">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="c7e8a-137">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="c7e8a-138">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c7e8a-138">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="c7e8a-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c7e8a-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

