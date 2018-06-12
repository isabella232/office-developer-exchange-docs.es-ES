---
title: Estado (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: El elemento de estado contiene el estado del ciclo de vida que se haya establecido en un buzón del sitio.
ms.openlocfilehash: accd70d36cc34e7364387b98a2e94c56b91f012f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837571"
---
# <a name="state-teammailboxlifecyclestatetype"></a><span data-ttu-id="66726-103">Estado (TeamMailboxLifecycleStateType)</span><span class="sxs-lookup"><span data-stu-id="66726-103">State (TeamMailboxLifecycleStateType)</span></span>

<span data-ttu-id="66726-104">El elemento de **estado** contiene el estado del ciclo de vida que se haya establecido en un buzón del sitio.</span><span class="sxs-lookup"><span data-stu-id="66726-104">The **State** element contains the lifecycle state that is set on a site mailbox.</span></span> 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

<span data-ttu-id="66726-105">**TeamMailboxLifecycleStateType**</span><span class="sxs-lookup"><span data-stu-id="66726-105">**TeamMailboxLifecycleStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="66726-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="66726-106">Attributes and elements</span></span>

<span data-ttu-id="66726-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="66726-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66726-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="66726-108">Attributes</span></span>

<span data-ttu-id="66726-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="66726-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66726-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66726-110">Child elements</span></span>

<span data-ttu-id="66726-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="66726-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66726-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="66726-112">Parent elements</span></span>

[<span data-ttu-id="66726-113">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="66726-113">SetTeamMailbox</span></span>](setteammailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="66726-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="66726-114">Text value</span></span>

<span data-ttu-id="66726-115">El valor de texto del elemento de **estado** es el estado de ciclo de vida que se haya establecido en un buzón del sitio.</span><span class="sxs-lookup"><span data-stu-id="66726-115">The text value of the **State** element is the lifecycle state that is set on a site mailbox.</span></span> <span data-ttu-id="66726-116">Un valor de texto de **activo** indica que un buzón del sitio está en uso.</span><span class="sxs-lookup"><span data-stu-id="66726-116">A text value of **Active** indicates that a site mailbox is in active use.</span></span> <span data-ttu-id="66726-117">Un valor de texto de **cerrada** indica que un buzón del sitio se ha cerrado y no está en uso.</span><span class="sxs-lookup"><span data-stu-id="66726-117">A text value of **Closed** indicates that a site mailbox has been closed and is not in active use.</span></span> <span data-ttu-id="66726-118">Un valor de texto de **no vinculados** indica que un buzón del sitio no está vinculado a un entorno de colaboración basado en web.</span><span class="sxs-lookup"><span data-stu-id="66726-118">A text value of **Unlinked** indicates that a site mailbox is not linked to a web-based collaboration environment.</span></span> <span data-ttu-id="66726-119">Los valores **activo**, **cerrado**y **PendingDelete** son mutuamente excluyentes, pero el valor **no vinculados** no es mutuamente exclusivos de los demás valores de la implementación.</span><span class="sxs-lookup"><span data-stu-id="66726-119">The **Active**, **Closed**, and **PendingDelete** values are mutually exclusive, but the **Unlinked** value is not mutually exclusive of the other values.</span></span> <span data-ttu-id="66726-120">Un valor de texto de **PendingDelete** indica que un buzón del sitio está pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="66726-120">A text value of **PendingDelete** indicates that a site mailbox is pending deletion.</span></span> <span data-ttu-id="66726-121">Tiene un buzón del sitio que se cierre antes de que se puede establecer como **PendingDelete**.</span><span class="sxs-lookup"><span data-stu-id="66726-121">A site mailbox has to be closed before it can be set as **PendingDelete**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66726-122">Notas</span><span class="sxs-lookup"><span data-stu-id="66726-122">Remarks</span></span>

<span data-ttu-id="66726-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="66726-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="66726-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="66726-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66726-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="66726-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66726-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="66726-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="66726-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="66726-127">Schema name</span></span>  <br/> |<span data-ttu-id="66726-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="66726-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="66726-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="66726-129">Validation file</span></span>  <br/> |<span data-ttu-id="66726-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="66726-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="66726-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="66726-131">Can be empty</span></span>  <br/> ||
   

