---
title: Contacto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86f66275-1e39-48ed-bd89-ac3bffc465a7
description: El elemento ContactId identifica de forma única un contacto.
ms.openlocfilehash: 17e8012283078d5d6e2cd1d2e88eef37b008be42
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463184"
---
# <a name="contactid"></a><span data-ttu-id="16134-103">Contacto</span><span class="sxs-lookup"><span data-stu-id="16134-103">ContactId</span></span>

<span data-ttu-id="16134-104">El elemento **ContactId** identifica de forma única un contacto.</span><span class="sxs-lookup"><span data-stu-id="16134-104">The **ContactId** element uniquely identifies a contact.</span></span> 
  
```XML
<ContactId Id="" ChangeKey=""/>
```

 <span data-ttu-id="16134-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="16134-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="16134-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="16134-106">Attributes and elements</span></span>

<span data-ttu-id="16134-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="16134-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="16134-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="16134-108">Attributes</span></span>

|<span data-ttu-id="16134-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="16134-109">**Attribute**</span></span>|<span data-ttu-id="16134-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16134-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16134-111">Id</span><span class="sxs-lookup"><span data-stu-id="16134-111">Id</span></span>  <br/> |<span data-ttu-id="16134-112">El valor de texto del atributo **ID** es el identificador del elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="16134-112">The text value of the **Id** attribute is the identifier of the contact item.</span></span>  <br/> |
|<span data-ttu-id="16134-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="16134-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="16134-114">El valor de texto del atributo **changekey** es la clave de cambio del elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="16134-114">The text value of the **ChangeKey** attribute is the change key of the contact item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="16134-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="16134-115">Child elements</span></span>

<span data-ttu-id="16134-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="16134-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="16134-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="16134-117">Parent elements</span></span>

<span data-ttu-id="16134-118">[AddImContactToGroup](addimcontacttogroup.md)  |  [RemoveContactFromImList](removecontactfromimlist.md)  |  [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span><span class="sxs-lookup"><span data-stu-id="16134-118">[AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16134-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16134-119">Remarks</span></span>

<span data-ttu-id="16134-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="16134-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="16134-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="16134-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16134-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="16134-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16134-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="16134-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="16134-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="16134-124">Schema name</span></span>  <br/> |<span data-ttu-id="16134-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="16134-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="16134-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="16134-126">Validation file</span></span>  <br/> |<span data-ttu-id="16134-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="16134-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="16134-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="16134-128">Can be empty</span></span>  <br/> |<span data-ttu-id="16134-129">false</span><span class="sxs-lookup"><span data-stu-id="16134-129">false</span></span>  <br/> |
   

