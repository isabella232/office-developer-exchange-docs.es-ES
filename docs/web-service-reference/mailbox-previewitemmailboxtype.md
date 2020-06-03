---
title: Buzón de correo (PreviewItemMailboxType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e898d737-b6e4-4403-9c2c-aec52a48a83d
description: El elemento Mailbox contiene el identificador de buzón y la dirección principal del Protocolo simple de transferencia de correo (SMTP) del usuario.
ms.openlocfilehash: 4dc5ee45c00945c30a699daa0158c96679189ab1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463898"
---
# <a name="mailbox-previewitemmailboxtype"></a><span data-ttu-id="03f40-103">Buzón de correo (PreviewItemMailboxType)</span><span class="sxs-lookup"><span data-stu-id="03f40-103">Mailbox (PreviewItemMailboxType)</span></span>

<span data-ttu-id="03f40-104">El elemento **Mailbox** contiene el identificador de buzón y la dirección principal del Protocolo simple de transferencia de correo (SMTP) del usuario.</span><span class="sxs-lookup"><span data-stu-id="03f40-104">The **Mailbox** element contains the mailbox identifier and the user's primary Simple Mail Transfer Protocol (SMTP) address.</span></span> 
  
```XML
<Mailbox>
   <MailboxId/>
   <PrimarySmtpAddress/>
</Mailbox>
```

<span data-ttu-id="03f40-105">**PreviewItemMailboxType**</span><span class="sxs-lookup"><span data-stu-id="03f40-105">**PreviewItemMailboxType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="03f40-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="03f40-106">Attributes and elements</span></span>

<span data-ttu-id="03f40-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="03f40-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="03f40-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="03f40-108">Attributes</span></span>

<span data-ttu-id="03f40-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="03f40-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="03f40-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="03f40-110">Child elements</span></span>

<span data-ttu-id="03f40-111">[Se especifica mailboxid](mailboxid.md)  |  [PrimarySmtpAddress (cadena)](primarysmtpaddress-string.md)</span><span class="sxs-lookup"><span data-stu-id="03f40-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="03f40-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="03f40-112">Parent elements</span></span>

[<span data-ttu-id="03f40-113">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="03f40-113">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="03f40-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03f40-114">Remarks</span></span>

<span data-ttu-id="03f40-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="03f40-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="03f40-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="03f40-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="03f40-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="03f40-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03f40-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="03f40-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="03f40-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="03f40-119">Schema name</span></span>  <br/> |<span data-ttu-id="03f40-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="03f40-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="03f40-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="03f40-121">Validation file</span></span>  <br/> |<span data-ttu-id="03f40-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="03f40-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="03f40-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="03f40-123">Can be empty</span></span>  <br/> |<span data-ttu-id="03f40-124">false</span><span class="sxs-lookup"><span data-stu-id="03f40-124">false</span></span>  <br/> |
   

