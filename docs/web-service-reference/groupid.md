---
title: GroupId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 656d9b9a-8a65-4a75-8466-5b0d96512dab
description: El elemento GroupId identifica de forma exclusiva a un grupo.
ms.openlocfilehash: 3b8de4d0fef95e2caff4db0d90bb303830022d36
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530095"
---
# <a name="groupid"></a><span data-ttu-id="945ef-103">GroupId</span><span class="sxs-lookup"><span data-stu-id="945ef-103">GroupId</span></span>

<span data-ttu-id="945ef-104">El elemento **GROUPID** identifica de forma exclusiva a un grupo.</span><span class="sxs-lookup"><span data-stu-id="945ef-104">The **GroupId** element uniquely identifies a group.</span></span> 
  
```XML
<GroupId Id="" ChangeKey=""/>
```

 <span data-ttu-id="945ef-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="945ef-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="945ef-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="945ef-106">Attributes and elements</span></span>

<span data-ttu-id="945ef-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="945ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="945ef-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="945ef-108">Attributes</span></span>

|<span data-ttu-id="945ef-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="945ef-109">**Attribute**</span></span>|<span data-ttu-id="945ef-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="945ef-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="945ef-111">Id</span><span class="sxs-lookup"><span data-stu-id="945ef-111">Id</span></span>  <br/> |<span data-ttu-id="945ef-112">El valor de texto del atributo **ID** es el identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="945ef-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="945ef-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="945ef-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="945ef-114">El valor de texto del atributo **changekey** es la clave de cambio del grupo.</span><span class="sxs-lookup"><span data-stu-id="945ef-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="945ef-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="945ef-115">Child elements</span></span>

<span data-ttu-id="945ef-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="945ef-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="945ef-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="945ef-117">Parent elements</span></span>

<span data-ttu-id="945ef-118">[AddNewImContactToGroup](addnewimcontacttogroup.md)  |  [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md)  |  [AddImContactToGroup](addimcontacttogroup.md)  |  [RemoveContactFromImList](removecontactfromimlist.md)  |  [RemoveImContactFromGroup](removeimcontactfromgroup.md)  |  [RemoveImGroup](removeimgroup.md)  |  [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md)  |  [SetImGroup](setimgroup.md)</span><span class="sxs-lookup"><span data-stu-id="945ef-118">[AddNewImContactToGroup](addnewimcontacttogroup.md) | [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md) | [AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md) | [RemoveImGroup](removeimgroup.md) | [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md) | [SetImGroup](setimgroup.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="945ef-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="945ef-119">Remarks</span></span>

<span data-ttu-id="945ef-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="945ef-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="945ef-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="945ef-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="945ef-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="945ef-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="945ef-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="945ef-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="945ef-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="945ef-124">Schema name</span></span>  <br/> |<span data-ttu-id="945ef-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="945ef-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="945ef-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="945ef-126">Validation file</span></span>  <br/> |<span data-ttu-id="945ef-127">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="945ef-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="945ef-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="945ef-128">Can be empty</span></span>  <br/> ||
   

