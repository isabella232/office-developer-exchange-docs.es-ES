---
title: State (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: El elemento State contiene el estado del ciclo de vida que se establece en un buzón del sitio.
ms.openlocfilehash: 597946b48649d997f8dd57823b4e0fcc091a6f84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465166"
---
# <a name="state-teammailboxlifecyclestatetype"></a><span data-ttu-id="b6d82-103">State (TeamMailboxLifecycleStateType)</span><span class="sxs-lookup"><span data-stu-id="b6d82-103">State (TeamMailboxLifecycleStateType)</span></span>

<span data-ttu-id="b6d82-104">El elemento **State** contiene el estado del ciclo de vida que se establece en un buzón del sitio.</span><span class="sxs-lookup"><span data-stu-id="b6d82-104">The **State** element contains the lifecycle state that is set on a site mailbox.</span></span> 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

<span data-ttu-id="b6d82-105">**TeamMailboxLifecycleStateType**</span><span class="sxs-lookup"><span data-stu-id="b6d82-105">**TeamMailboxLifecycleStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b6d82-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b6d82-106">Attributes and elements</span></span>

<span data-ttu-id="b6d82-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b6d82-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6d82-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6d82-108">Attributes</span></span>

<span data-ttu-id="b6d82-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b6d82-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6d82-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b6d82-110">Child elements</span></span>

<span data-ttu-id="b6d82-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b6d82-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b6d82-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b6d82-112">Parent elements</span></span>

[<span data-ttu-id="b6d82-113">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="b6d82-113">SetTeamMailbox</span></span>](setteammailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="b6d82-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b6d82-114">Text value</span></span>

<span data-ttu-id="b6d82-115">El valor de texto del elemento de **Estado** es el estado de ciclo de vida que se establece en un buzón de sitio.</span><span class="sxs-lookup"><span data-stu-id="b6d82-115">The text value of the **State** element is the lifecycle state that is set on a site mailbox.</span></span> <span data-ttu-id="b6d82-116">Un valor de texto **activo** indica que un buzón de sitio está en uso.</span><span class="sxs-lookup"><span data-stu-id="b6d82-116">A text value of **Active** indicates that a site mailbox is in active use.</span></span> <span data-ttu-id="b6d82-117">Un valor de texto de **Closed** indica que se ha cerrado un buzón de sitio y no está en uso activo.</span><span class="sxs-lookup"><span data-stu-id="b6d82-117">A text value of **Closed** indicates that a site mailbox has been closed and is not in active use.</span></span> <span data-ttu-id="b6d82-118">Un valor de texto de **unlinkd** indica que un buzón de sitio no está vinculado a un entorno de colaboración basado en Web.</span><span class="sxs-lookup"><span data-stu-id="b6d82-118">A text value of **Unlinked** indicates that a site mailbox is not linked to a web-based collaboration environment.</span></span> <span data-ttu-id="b6d82-119">Los valores **Active**, **Closed**y **PendingDelete** se excluyen mutuamente, pero el valor **desvinculado** no se excluye mutuamente de los demás valores.</span><span class="sxs-lookup"><span data-stu-id="b6d82-119">The **Active**, **Closed**, and **PendingDelete** values are mutually exclusive, but the **Unlinked** value is not mutually exclusive of the other values.</span></span> <span data-ttu-id="b6d82-120">Un valor de texto de **PendingDelete** indica que hay un buzón de sitio pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="b6d82-120">A text value of **PendingDelete** indicates that a site mailbox is pending deletion.</span></span> <span data-ttu-id="b6d82-121">Un buzón de sitio tiene que cerrarse antes de que se pueda establecer como **PendingDelete**.</span><span class="sxs-lookup"><span data-stu-id="b6d82-121">A site mailbox has to be closed before it can be set as **PendingDelete**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6d82-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6d82-122">Remarks</span></span>

<span data-ttu-id="b6d82-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b6d82-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b6d82-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6d82-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6d82-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b6d82-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6d82-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6d82-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b6d82-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b6d82-127">Schema name</span></span>  <br/> |<span data-ttu-id="b6d82-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b6d82-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b6d82-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b6d82-129">Validation file</span></span>  <br/> |<span data-ttu-id="b6d82-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b6d82-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b6d82-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b6d82-131">Can be empty</span></span>  <br/> ||
   

