---
title: UserParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: El elemento UserParameters contiene una lista de las extensiones de cliente habilitada y deshabilitada.
ms.openlocfilehash: e0a72fe13255380ee56b32c863fb3bffb2e1ac5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840922"
---
# <a name="userparameters"></a><span data-ttu-id="85a1c-103">UserParameters</span><span class="sxs-lookup"><span data-stu-id="85a1c-103">UserParameters</span></span>

<span data-ttu-id="85a1c-104">El elemento **UserParameters** contiene una lista de las extensiones de cliente habilitada y deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="85a1c-104">The **UserParameters** element contains a list of enabled and disabled client extensions.</span></span> 
  
```XML
<UserParameters UserId="" EnabledOnly="">
   <UserEnabledExtensions/>
   <UserDisabledExtensions/>
</UserParameters>
```

 <span data-ttu-id="85a1c-105">**GetClientExtensionUserParametersType**</span><span class="sxs-lookup"><span data-stu-id="85a1c-105">**GetClientExtensionUserParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85a1c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="85a1c-106">Attributes and elements</span></span>

<span data-ttu-id="85a1c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="85a1c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85a1c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="85a1c-108">Attributes</span></span>

|<span data-ttu-id="85a1c-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="85a1c-109">**Attribute**</span></span>|<span data-ttu-id="85a1c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85a1c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85a1c-111">UserId</span><span class="sxs-lookup"><span data-stu-id="85a1c-111">UserId</span></span>  <br/> |<span data-ttu-id="85a1c-112">El valor de texto del atributo **UserId** es el identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="85a1c-112">The text value of the **UserId** attribute is the identifier of the user.</span></span>  <br/> |
|<span data-ttu-id="85a1c-113">EnabledOnly</span><span class="sxs-lookup"><span data-stu-id="85a1c-113">EnabledOnly</span></span>  <br/> |<span data-ttu-id="85a1c-114">El valor de texto de la **EnabledOnly** indica si la respuesta contiene sólo las extensiones habilitadas.</span><span class="sxs-lookup"><span data-stu-id="85a1c-114">The text value of the **EnabledOnly** indicates whether the response only contains the enabled extensions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85a1c-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85a1c-115">Child elements</span></span>

<span data-ttu-id="85a1c-116">[UserEnabledExtensions](userenabledextensions.md) | [UserDisabledExtensions](userdisabledextensions.md)</span><span class="sxs-lookup"><span data-stu-id="85a1c-116">[UserEnabledExtensions](userenabledextensions.md) | [UserDisabledExtensions](userdisabledextensions.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85a1c-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="85a1c-117">Parent elements</span></span>

[<span data-ttu-id="85a1c-118">GetClientExtension</span><span class="sxs-lookup"><span data-stu-id="85a1c-118">GetClientExtension</span></span>](getclientextension.md)
  
## <a name="remarks"></a><span data-ttu-id="85a1c-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85a1c-119">Remarks</span></span>

<span data-ttu-id="85a1c-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85a1c-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="85a1c-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="85a1c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85a1c-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="85a1c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85a1c-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85a1c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85a1c-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="85a1c-124">Schema name</span></span>  <br/> |<span data-ttu-id="85a1c-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="85a1c-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="85a1c-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="85a1c-126">Validation file</span></span>  <br/> |<span data-ttu-id="85a1c-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85a1c-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85a1c-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="85a1c-128">Can be empty</span></span>  <br/> ||
   

