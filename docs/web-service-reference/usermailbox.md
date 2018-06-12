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
ms.openlocfilehash: 9f359a2b0ba315c236d4bf189c3de321417bd390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840913"
---
# <a name="usermailbox"></a><span data-ttu-id="71907-103">UserMailbox</span><span class="sxs-lookup"><span data-stu-id="71907-103">UserMailbox</span></span>

<span data-ttu-id="71907-104">El elemento **UserMailbox** identifica un buzón de usuario.</span><span class="sxs-lookup"><span data-stu-id="71907-104">The **UserMailbox** element identifies a user mailbox.</span></span> 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 <span data-ttu-id="71907-105">**UserMailboxType**</span><span class="sxs-lookup"><span data-stu-id="71907-105">**UserMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="71907-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="71907-106">Attributes and elements</span></span>

<span data-ttu-id="71907-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="71907-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="71907-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="71907-108">Attributes</span></span>

|<span data-ttu-id="71907-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="71907-109">**Attribute**</span></span>|<span data-ttu-id="71907-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71907-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71907-111">Id</span><span class="sxs-lookup"><span data-stu-id="71907-111">Id</span></span>  <br/> |<span data-ttu-id="71907-112">El valor de texto del atributo **Id** es el identificador del buzón.</span><span class="sxs-lookup"><span data-stu-id="71907-112">The text value of the **Id** attribute is the identifier of the mailbox.</span></span>  <br/> |
|<span data-ttu-id="71907-113">IsArchive</span><span class="sxs-lookup"><span data-stu-id="71907-113">IsArchive</span></span>  <br/> |<span data-ttu-id="71907-114">El valor de texto del atributo **IsArchive** indica si el buzón de correo es un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="71907-114">The text value of the **IsArchive** attribute indicates whether the mailbox is an archive mailbox.</span></span> <span data-ttu-id="71907-115">Un valor de texto de **true** para el atributo **IsArchive** indica que el buzón de correo es un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="71907-115">A text value of **true** for the **IsArchive** attribute indicates that the mailbox is an archive mailbox.</span></span> <span data-ttu-id="71907-116">Un valor de **false** para el atributo **IsArchive** indica que el buzón de correo es un buzón principal.</span><span class="sxs-lookup"><span data-stu-id="71907-116">A value of **false** for the **IsArchive** attribute indicates that the mailbox is a primary mailbox.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="71907-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="71907-117">Child elements</span></span>

<span data-ttu-id="71907-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="71907-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="71907-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="71907-119">Parent elements</span></span>

<span data-ttu-id="71907-120">[Buzones de correo (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span><span class="sxs-lookup"><span data-stu-id="71907-120">[Mailboxes (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71907-121">Notas</span><span class="sxs-lookup"><span data-stu-id="71907-121">Remarks</span></span>

<span data-ttu-id="71907-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="71907-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="71907-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="71907-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="71907-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="71907-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71907-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="71907-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="71907-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="71907-126">Schema name</span></span>  <br/> |<span data-ttu-id="71907-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="71907-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="71907-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="71907-128">Validation file</span></span>  <br/> |<span data-ttu-id="71907-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="71907-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="71907-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="71907-130">Can be empty</span></span>  <br/> |<span data-ttu-id="71907-131">true</span><span class="sxs-lookup"><span data-stu-id="71907-131">true</span></span>  <br/> |
   

