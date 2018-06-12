---
title: UnpinTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1034b013-ef34-4e72-99b3-38bff475b3e8
description: El elemento UnpinTeamMailbox contiene la solicitud para desanclar un buzón del sitio desde el cliente mediante la eliminación de la respuesta de detección automática.
ms.openlocfilehash: d303b47f0796f9bec7e9f198afa81d2ecd9fd5cd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840783"
---
# <a name="unpinteammailbox"></a><span data-ttu-id="ef59c-103">UnpinTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="ef59c-103">UnpinTeamMailbox</span></span>

<span data-ttu-id="ef59c-104">El elemento **UnpinTeamMailbox** contiene la solicitud para desanclar un buzón del sitio desde el cliente mediante la eliminación de la respuesta de **detección automática** .</span><span class="sxs-lookup"><span data-stu-id="ef59c-104">The **UnpinTeamMailbox** element contains the request to unpin a site mailbox from the client by removing it from the **Autodiscover** response.</span></span> 
  
```XML
<UnpinTeamMailbox>
   <EmailAddress/>
</UnpinTeamMailbox>
```

 <span data-ttu-id="ef59c-105">**UnpinTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="ef59c-105">**UnpinTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef59c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ef59c-106">Attributes and elements</span></span>

<span data-ttu-id="ef59c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ef59c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef59c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef59c-108">Attributes</span></span>

<span data-ttu-id="ef59c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ef59c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef59c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ef59c-110">Child elements</span></span>

[<span data-ttu-id="ef59c-111">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="ef59c-111">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="ef59c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ef59c-112">Parent elements</span></span>

<span data-ttu-id="ef59c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ef59c-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef59c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef59c-114">Remarks</span></span>

<span data-ttu-id="ef59c-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef59c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ef59c-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef59c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef59c-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ef59c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef59c-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef59c-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef59c-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ef59c-119">Schema name</span></span>  <br/> |<span data-ttu-id="ef59c-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ef59c-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef59c-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ef59c-121">Validation file</span></span>  <br/> |<span data-ttu-id="ef59c-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef59c-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef59c-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ef59c-123">Can be empty</span></span>  <br/> ||
   

