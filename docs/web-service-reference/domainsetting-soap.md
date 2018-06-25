---
title: DomainSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bad5399c-0762-4979-9c15-58cf4b7b6278
description: El elemento DomainSetting contiene la configuración de dominio que es devueltos por la solicitud de operación GetDomainSettings operación (SOAP).
ms.openlocfilehash: f1c7a30ee221c5f3ca1358d0f3c3aca5c3467159
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764277"
---
# <a name="domainsetting-soap"></a><span data-ttu-id="9d7d9-103">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d7d9-103">DomainSetting (SOAP)</span></span>

<span data-ttu-id="9d7d9-104">El elemento **DomainSetting** contiene la configuración de dominio que es devueltos por la solicitud de operación de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="9d7d9-104">The **DomainSetting** element contains domain settings that are returned by the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<DomainSetting>
   <Name/>
</DomainSetting>
```

 <span data-ttu-id="9d7d9-105">**DomainSetting**</span><span class="sxs-lookup"><span data-stu-id="9d7d9-105">**DomainSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d7d9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9d7d9-106">Attributes and elements</span></span>

<span data-ttu-id="9d7d9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9d7d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d7d9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d7d9-108">Attributes</span></span>

<span data-ttu-id="9d7d9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9d7d9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d7d9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9d7d9-110">Child elements</span></span>

|<span data-ttu-id="9d7d9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d7d9-111">**Element**</span></span>|<span data-ttu-id="9d7d9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d7d9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d7d9-113">Nombre (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d7d9-113">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="9d7d9-114">Representa el nombre de una opción de configuración.</span><span class="sxs-lookup"><span data-stu-id="9d7d9-114">Represents the name of a setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d7d9-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9d7d9-115">Parent elements</span></span>

|<span data-ttu-id="9d7d9-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d7d9-116">**Element**</span></span>|<span data-ttu-id="9d7d9-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d7d9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d7d9-118">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d7d9-118">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="9d7d9-119">Representa la configuración de dominio que se ha enviado en una solicitud de detección automática o devueltas por una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="9d7d9-119">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9d7d9-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9d7d9-120">Text value</span></span>

<span data-ttu-id="9d7d9-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9d7d9-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d7d9-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9d7d9-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d7d9-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9d7d9-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9d7d9-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9d7d9-124">Schema Name</span></span>  <br/> |<span data-ttu-id="9d7d9-125">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="9d7d9-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9d7d9-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9d7d9-126">Validation File</span></span>  <br/> |<span data-ttu-id="9d7d9-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9d7d9-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d7d9-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9d7d9-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d7d9-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="9d7d9-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d7d9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d7d9-130">See also</span></span>

- [<span data-ttu-id="9d7d9-131">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d7d9-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

