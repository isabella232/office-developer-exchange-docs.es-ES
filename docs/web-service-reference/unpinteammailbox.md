---
title: UnpinTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1034b013-ef34-4e72-99b3-38bff475b3e8
description: El elemento UnpinTeamMailbox contiene la solicitud de desanclar un buzón de sitio del cliente quitándolo de la respuesta de detección automática.
ms.openlocfilehash: a6b01bfa9c5908765ff04ef7f5edbef0b99a9be2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467245"
---
# <a name="unpinteammailbox"></a><span data-ttu-id="3edc4-103">UnpinTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="3edc4-103">UnpinTeamMailbox</span></span>

<span data-ttu-id="3edc4-104">El elemento **UnpinTeamMailbox** contiene la solicitud de desanclar un buzón de sitio del cliente quitándolo de la respuesta de **detección automática** .</span><span class="sxs-lookup"><span data-stu-id="3edc4-104">The **UnpinTeamMailbox** element contains the request to unpin a site mailbox from the client by removing it from the **Autodiscover** response.</span></span> 
  
```XML
<UnpinTeamMailbox>
   <EmailAddress/>
</UnpinTeamMailbox>
```

 <span data-ttu-id="3edc4-105">**UnpinTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="3edc4-105">**UnpinTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3edc4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3edc4-106">Attributes and elements</span></span>

<span data-ttu-id="3edc4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3edc4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3edc4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3edc4-108">Attributes</span></span>

<span data-ttu-id="3edc4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3edc4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3edc4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3edc4-110">Child elements</span></span>

[<span data-ttu-id="3edc4-111">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="3edc4-111">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="3edc4-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3edc4-112">Parent elements</span></span>

<span data-ttu-id="3edc4-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3edc4-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3edc4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3edc4-114">Remarks</span></span>

<span data-ttu-id="3edc4-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3edc4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3edc4-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3edc4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3edc4-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3edc4-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3edc4-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="3edc4-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3edc4-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3edc4-119">Schema name</span></span>  <br/> |<span data-ttu-id="3edc4-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3edc4-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3edc4-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3edc4-121">Validation file</span></span>  <br/> |<span data-ttu-id="3edc4-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3edc4-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3edc4-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3edc4-123">Can be empty</span></span>  <br/> ||
   

