---
title: UserMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: El elemento UserMailbox identifica un buzón de usuario.
ms.openlocfilehash: 9bb1b08320f5e6f4843383a8e3aff96fc3dcccad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465320"
---
# <a name="usermailbox"></a><span data-ttu-id="2101d-103">UserMailbox</span><span class="sxs-lookup"><span data-stu-id="2101d-103">UserMailbox</span></span>

<span data-ttu-id="2101d-104">El elemento **UserMailbox** identifica un buzón de usuario.</span><span class="sxs-lookup"><span data-stu-id="2101d-104">The **UserMailbox** element identifies a user mailbox.</span></span> 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 <span data-ttu-id="2101d-105">**UserMailboxType**</span><span class="sxs-lookup"><span data-stu-id="2101d-105">**UserMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2101d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2101d-106">Attributes and elements</span></span>

<span data-ttu-id="2101d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2101d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2101d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2101d-108">Attributes</span></span>

|<span data-ttu-id="2101d-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2101d-109">**Attribute**</span></span>|<span data-ttu-id="2101d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2101d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2101d-111">Id</span><span class="sxs-lookup"><span data-stu-id="2101d-111">Id</span></span>  <br/> |<span data-ttu-id="2101d-112">El valor de texto del atributo **ID** es el identificador del buzón.</span><span class="sxs-lookup"><span data-stu-id="2101d-112">The text value of the **Id** attribute is the identifier of the mailbox.</span></span>  <br/> |
|<span data-ttu-id="2101d-113">IsArchive</span><span class="sxs-lookup"><span data-stu-id="2101d-113">IsArchive</span></span>  <br/> |<span data-ttu-id="2101d-114">El valor de texto del atributo **IsArchive** indica si el buzón es un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="2101d-114">The text value of the **IsArchive** attribute indicates whether the mailbox is an archive mailbox.</span></span> <span data-ttu-id="2101d-115">Un valor de texto de **true** para el atributo **IsArchive** indica que el buzón de correo es un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="2101d-115">A text value of **true** for the **IsArchive** attribute indicates that the mailbox is an archive mailbox.</span></span> <span data-ttu-id="2101d-116">Un valor de **false** para el atributo **IsArchive** indica que el buzón de correo es un buzón principal.</span><span class="sxs-lookup"><span data-stu-id="2101d-116">A value of **false** for the **IsArchive** attribute indicates that the mailbox is a primary mailbox.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2101d-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2101d-117">Child elements</span></span>

<span data-ttu-id="2101d-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2101d-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2101d-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2101d-119">Parent elements</span></span>

<span data-ttu-id="2101d-120">[Buzones de correo (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md)  |  [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span><span class="sxs-lookup"><span data-stu-id="2101d-120">[Mailboxes (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2101d-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2101d-121">Remarks</span></span>

<span data-ttu-id="2101d-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2101d-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2101d-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2101d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2101d-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2101d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2101d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="2101d-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2101d-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2101d-126">Schema name</span></span>  <br/> |<span data-ttu-id="2101d-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2101d-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="2101d-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2101d-128">Validation file</span></span>  <br/> |<span data-ttu-id="2101d-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2101d-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2101d-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2101d-130">Can be empty</span></span>  <br/> |<span data-ttu-id="2101d-131">true</span><span class="sxs-lookup"><span data-stu-id="2101d-131">true</span></span>  <br/> |
   

