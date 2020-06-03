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
description: El elemento GetInboxRules define una solicitud para obtener las reglas de la bandeja de entrada en un buzón del almacén del servidor.
ms.openlocfilehash: 890592fd3f87fc5592a618a2febf28e4daf0dbe4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457931"
---
# <a name="getinboxrules"></a><span data-ttu-id="551a3-103">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="551a3-103">GetInboxRules</span></span>

<span data-ttu-id="551a3-104">El elemento **GetInboxRules** define una solicitud para obtener las reglas de la bandeja de entrada en un buzón del almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="551a3-104">The **GetInboxRules** element defines a request to get the Inbox rules on a mailbox in the server store.</span></span> 
  
```XML
<GetInboxRules>
   <MailboxSmtpAddress/>
</GetInboxRules>
```

 <span data-ttu-id="551a3-105">**GetInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="551a3-105">**GetInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="551a3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="551a3-106">Attributes and elements</span></span>

<span data-ttu-id="551a3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="551a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="551a3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="551a3-108">Attributes</span></span>

<span data-ttu-id="551a3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="551a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="551a3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="551a3-110">Child elements</span></span>

|<span data-ttu-id="551a3-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="551a3-111">**Element**</span></span>|<span data-ttu-id="551a3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="551a3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="551a3-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="551a3-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="551a3-114">Representa la dirección SMTP del usuario cuyas reglas de la bandeja de entrada se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="551a3-114">Represents the SMTP address of the user whose Inbox rules are to be retrieved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="551a3-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="551a3-115">Parent elements</span></span>

<span data-ttu-id="551a3-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="551a3-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="551a3-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="551a3-117">Remarks</span></span>

<span data-ttu-id="551a3-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="551a3-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="551a3-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="551a3-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="551a3-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="551a3-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="551a3-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="551a3-121">Schema Name</span></span>  <br/> |<span data-ttu-id="551a3-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="551a3-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="551a3-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="551a3-123">Validation File</span></span>  <br/> |<span data-ttu-id="551a3-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="551a3-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="551a3-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="551a3-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="551a3-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="551a3-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="551a3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="551a3-127">See also</span></span>



[<span data-ttu-id="551a3-128">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="551a3-128">GetInboxRules operation</span></span>](getinboxrules-operation.md)

