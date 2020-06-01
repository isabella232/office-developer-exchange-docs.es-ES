---
title: GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: El elemento GetPasswordExpirationDate define una solicitud para obtener la fecha de expiración de la contraseña de una cuenta de correo electrónico. Este elemento es el elemento base para la operación de operación GetPasswordExpirationDate.
ms.openlocfilehash: ececbf51f71c7d87705d727229fce2314d922efb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456496"
---
# <a name="getpasswordexpirationdate"></a><span data-ttu-id="13359-104">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="13359-104">GetPasswordExpirationDate</span></span>

<span data-ttu-id="13359-105">El elemento **GetPasswordExpirationDate** define una solicitud para obtener la fecha de expiración de la contraseña de una cuenta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="13359-105">The **GetPasswordExpirationDate** element defines a request to get the password expiration date for an email account.</span></span> <span data-ttu-id="13359-106">Este elemento es el elemento base para la operación de [operación GetPasswordExpirationDate](getpasswordexpirationdate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="13359-106">This element is the base element for the [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation.</span></span> 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 <span data-ttu-id="13359-107">**GetPasswordExpirationDateType**</span><span class="sxs-lookup"><span data-stu-id="13359-107">**GetPasswordExpirationDateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13359-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="13359-108">Attributes and elements</span></span>

<span data-ttu-id="13359-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="13359-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13359-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="13359-110">Attributes</span></span>

<span data-ttu-id="13359-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="13359-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13359-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13359-112">Child elements</span></span>

|<span data-ttu-id="13359-113">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="13359-113">**Element name**</span></span>|<span data-ttu-id="13359-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13359-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13359-115">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="13359-115">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="13359-116">Representa la dirección de correo electrónico de la cuenta de correo electrónico para la que se va a devolver la fecha de expiración de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="13359-116">Represents the email address of the email account for which the password expiration date is to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13359-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="13359-117">Parent elements</span></span>

<span data-ttu-id="13359-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="13359-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13359-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13359-119">Remarks</span></span>

<span data-ttu-id="13359-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="13359-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="13359-121">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="13359-121">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13359-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="13359-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13359-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="13359-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="13359-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="13359-124">Schema Name</span></span>  <br/> |<span data-ttu-id="13359-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="13359-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="13359-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="13359-126">Validation File</span></span>  <br/> |<span data-ttu-id="13359-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="13359-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="13359-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="13359-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="13359-129">Falso</span><span class="sxs-lookup"><span data-stu-id="13359-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13359-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="13359-130">See also</span></span>



[<span data-ttu-id="13359-131">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="13359-131">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)


- [<span data-ttu-id="13359-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="13359-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

