---
title: Buzón de correo (PreviewItemMailboxType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e898d737-b6e4-4403-9c2c-aec52a48a83d
description: El elemento de buzón de correo contiene el identificador de buzón de correo y dirección de Protocolo Simple de transferencia de correo (SMTP) principal del usuario.
ms.openlocfilehash: 1b6669928015bc880806479d294a4063034a559f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836255"
---
# <a name="mailbox-previewitemmailboxtype"></a><span data-ttu-id="2c384-103">Buzón de correo (PreviewItemMailboxType)</span><span class="sxs-lookup"><span data-stu-id="2c384-103">Mailbox (PreviewItemMailboxType)</span></span>

<span data-ttu-id="2c384-104">El elemento de **buzón de correo** contiene el identificador de buzón de correo y dirección de Protocolo Simple de transferencia de correo (SMTP) principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="2c384-104">The **Mailbox** element contains the mailbox identifier and the user's primary Simple Mail Transfer Protocol (SMTP) address.</span></span> 
  
```XML
<Mailbox>
   <MailboxId/>
   <PrimarySmtpAddress/>
</Mailbox>
```

<span data-ttu-id="2c384-105">**PreviewItemMailboxType**</span><span class="sxs-lookup"><span data-stu-id="2c384-105">**PreviewItemMailboxType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2c384-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2c384-106">Attributes and elements</span></span>

<span data-ttu-id="2c384-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2c384-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c384-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2c384-108">Attributes</span></span>

<span data-ttu-id="2c384-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2c384-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c384-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2c384-110">Child elements</span></span>

<span data-ttu-id="2c384-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress (cadena)](primarysmtpaddress-string.md)</span><span class="sxs-lookup"><span data-stu-id="2c384-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c384-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2c384-112">Parent elements</span></span>

[<span data-ttu-id="2c384-113">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="2c384-113">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="2c384-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c384-114">Remarks</span></span>

<span data-ttu-id="2c384-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2c384-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2c384-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2c384-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c384-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2c384-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c384-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c384-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c384-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2c384-119">Schema name</span></span>  <br/> |<span data-ttu-id="2c384-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2c384-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c384-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2c384-121">Validation file</span></span>  <br/> |<span data-ttu-id="2c384-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c384-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c384-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2c384-123">Can be empty</span></span>  <br/> |<span data-ttu-id="2c384-124">falso</span><span class="sxs-lookup"><span data-stu-id="2c384-124">false</span></span>  <br/> |
   

