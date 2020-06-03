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
description: El elemento DomainSetting contiene la configuración de dominio que devuelve la solicitud de operación de GetDomainSettings (SOAP).
ms.openlocfilehash: 54441dd7cfcf7372807a1e6bfd8ea5d26805bffc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526301"
---
# <a name="domainsetting-soap"></a><span data-ttu-id="b51d0-103">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b51d0-103">DomainSetting (SOAP)</span></span>

<span data-ttu-id="b51d0-104">El elemento **DomainSetting** contiene la configuración de dominio que devuelve la solicitud de operación de [GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="b51d0-104">The **DomainSetting** element contains domain settings that are returned by the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<DomainSetting>
   <Name/>
</DomainSetting>
```

 <span data-ttu-id="b51d0-105">**DomainSetting**</span><span class="sxs-lookup"><span data-stu-id="b51d0-105">**DomainSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b51d0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b51d0-106">Attributes and elements</span></span>

<span data-ttu-id="b51d0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b51d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b51d0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b51d0-108">Attributes</span></span>

<span data-ttu-id="b51d0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b51d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b51d0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b51d0-110">Child elements</span></span>

|<span data-ttu-id="b51d0-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b51d0-111">**Element**</span></span>|<span data-ttu-id="b51d0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b51d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b51d0-113">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b51d0-113">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="b51d0-114">Representa el nombre de una configuración.</span><span class="sxs-lookup"><span data-stu-id="b51d0-114">Represents the name of a setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b51d0-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b51d0-115">Parent elements</span></span>

|<span data-ttu-id="b51d0-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b51d0-116">**Element**</span></span>|<span data-ttu-id="b51d0-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b51d0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b51d0-118">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b51d0-118">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="b51d0-119">Representa la configuración de dominio que se ha enviado en una solicitud de detección automática o devuelta por una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="b51d0-119">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b51d0-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b51d0-120">Text value</span></span>

<span data-ttu-id="b51d0-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b51d0-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b51d0-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b51d0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b51d0-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b51d0-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b51d0-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b51d0-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b51d0-125">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="b51d0-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b51d0-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b51d0-126">Validation File</span></span>  <br/> |<span data-ttu-id="b51d0-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b51d0-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b51d0-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b51d0-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="b51d0-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b51d0-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b51d0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b51d0-130">See also</span></span>

- [<span data-ttu-id="b51d0-131">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b51d0-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

