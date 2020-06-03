---
title: UserSettingErrors (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a9b94bae-cab9-412d-a811-801e849ed6c5
description: El elemento UserSettingErrors representa una colección de información sobre la configuración que no se pudo devolver.
ms.openlocfilehash: a6cc0fe114bd511dc4136532986b552c28b0d5c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467126"
---
# <a name="usersettingerrors-soap"></a><span data-ttu-id="b630c-103">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b630c-103">UserSettingErrors (SOAP)</span></span>

<span data-ttu-id="b630c-104">El elemento **UserSettingErrors** representa una colección de información sobre la configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="b630c-104">The **UserSettingErrors** element represents a collection of information about settings that could not be returned.</span></span> 
  
```XML
<UserSettingErrors>
    <UserSettingError/>
</UserSettingErrors>
```

 <span data-ttu-id="b630c-105">**UserSettingErrors**</span><span class="sxs-lookup"><span data-stu-id="b630c-105">**UserSettingErrors**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b630c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b630c-106">Attributes and elements</span></span>

<span data-ttu-id="b630c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b630c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b630c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b630c-108">Attributes</span></span>

<span data-ttu-id="b630c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b630c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b630c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b630c-110">Child elements</span></span>

|<span data-ttu-id="b630c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b630c-111">**Element**</span></span>|<span data-ttu-id="b630c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b630c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b630c-113">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b630c-113">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="b630c-114">Representa un error que se devuelve al recuperar una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="b630c-114">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b630c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b630c-115">Parent elements</span></span>

|<span data-ttu-id="b630c-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b630c-116">**Element**</span></span>|<span data-ttu-id="b630c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b630c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b630c-118">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b630c-118">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="b630c-119">Representa una respuesta a una solicitud de GetUserSettings para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="b630c-119">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b630c-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b630c-120">Text value</span></span>

<span data-ttu-id="b630c-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b630c-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b630c-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b630c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b630c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b630c-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b630c-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b630c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b630c-125">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="b630c-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b630c-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b630c-126">Validation File</span></span>  <br/> |<span data-ttu-id="b630c-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b630c-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b630c-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b630c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="b630c-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b630c-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b630c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b630c-130">See also</span></span>



[<span data-ttu-id="b630c-131">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="b630c-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

