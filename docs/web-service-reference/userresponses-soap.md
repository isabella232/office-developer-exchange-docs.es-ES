---
title: UserResponses (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a48766df-4cc8-47c2-a8c1-826daec94e5a
description: El elemento UserResponses contiene las opciones de configuración para cada usuario solicitado.
ms.openlocfilehash: db2bab16334b90395d29dc03353dce05b0e45357
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526749"
---
# <a name="userresponses-soap"></a><span data-ttu-id="2f1d4-103">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2f1d4-103">UserResponses (SOAP)</span></span>

<span data-ttu-id="2f1d4-104">El elemento **UserResponses** contiene las opciones de configuración para cada usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="2f1d4-104">The **UserResponses** element contains the configuration settings for each requested user.</span></span> 
  
```XML
<UserResponses>
   <UserResponse/>
</UserResponses>
```

 <span data-ttu-id="2f1d4-105">**ArrayOfUserResponse**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-105">**ArrayOfUserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f1d4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2f1d4-106">Attributes and elements</span></span>

<span data-ttu-id="2f1d4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2f1d4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f1d4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f1d4-108">Attributes</span></span>

<span data-ttu-id="2f1d4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2f1d4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f1d4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f1d4-110">Child elements</span></span>

|<span data-ttu-id="2f1d4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-111">**Element**</span></span>|<span data-ttu-id="2f1d4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f1d4-113">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2f1d4-113">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="2f1d4-114">Representa una respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="2f1d4-114">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f1d4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2f1d4-115">Parent elements</span></span>

|<span data-ttu-id="2f1d4-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-116">**Element**</span></span>|<span data-ttu-id="2f1d4-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f1d4-118">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2f1d4-118">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="2f1d4-119">Contiene la respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="2f1d4-119">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="2f1d4-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2f1d4-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f1d4-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f1d4-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="2f1d4-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2f1d4-122">Schema Name</span></span>  <br/> |<span data-ttu-id="2f1d4-123">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="2f1d4-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="2f1d4-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2f1d4-124">Validation File</span></span>  <br/> |<span data-ttu-id="2f1d4-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2f1d4-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f1d4-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2f1d4-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f1d4-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="2f1d4-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f1d4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f1d4-128">See also</span></span>



[<span data-ttu-id="2f1d4-129">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2f1d4-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

