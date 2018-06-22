---
title: GetInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: 7a54992d-03a6-4afc-a2e4-dcdc9ce54194
description: El elemento GetInboxRules define una solicitud para obtener las reglas de bandeja de entrada en un buzón de correo en el almacén del servidor.
ms.openlocfilehash: 3c3ee682dd009e5c4bec940637a7dfa3c11f8402
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764876"
---
# <a name="getinboxrules"></a><span data-ttu-id="3737b-103">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="3737b-103">GetInboxRules</span></span>

<span data-ttu-id="3737b-104">El elemento **GetInboxRules** define una solicitud para obtener las reglas de bandeja de entrada en un buzón de correo en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="3737b-104">The **GetInboxRules** element defines a request to get the Inbox rules on a mailbox in the server store.</span></span> 
  
```XML
<GetInboxRules>
   <MailboxSmtpAddress/>
</GetInboxRules>
```

 <span data-ttu-id="3737b-105">**GetInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="3737b-105">**GetInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3737b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3737b-106">Attributes and elements</span></span>

<span data-ttu-id="3737b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3737b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3737b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3737b-108">Attributes</span></span>

<span data-ttu-id="3737b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3737b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3737b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3737b-110">Child elements</span></span>

|<span data-ttu-id="3737b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3737b-111">**Element**</span></span>|<span data-ttu-id="3737b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3737b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3737b-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="3737b-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="3737b-114">Representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3737b-114">Represents the SMTP address of the user whose Inbox rules are to be retrieved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3737b-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3737b-115">Parent elements</span></span>

<span data-ttu-id="3737b-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3737b-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3737b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3737b-117">Remarks</span></span>

<span data-ttu-id="3737b-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3737b-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3737b-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3737b-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3737b-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3737b-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3737b-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3737b-121">Schema Name</span></span>  <br/> |<span data-ttu-id="3737b-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3737b-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3737b-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3737b-123">Validation File</span></span>  <br/> |<span data-ttu-id="3737b-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3737b-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3737b-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3737b-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="3737b-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="3737b-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3737b-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="3737b-127">See also</span></span>



[<span data-ttu-id="3737b-128">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="3737b-128">GetInboxRules operation</span></span>](getinboxrules-operation.md)

