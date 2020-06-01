---
title: Dominio (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: El elemento de dominio contiene un dominio federado en una respuesta de GetFederationInformation o contiene un dominio con los valores de configuración que se solicitan en una solicitud de GetDomainSettings.
ms.openlocfilehash: f90c608ee1fc3356a227bca6411eaeff0c1e8b22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456986"
---
# <a name="domain-soap"></a><span data-ttu-id="f6520-103">Dominio (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f6520-103">Domain (SOAP)</span></span>

<span data-ttu-id="f6520-104">El elemento de **dominio** contiene un dominio federado en una respuesta de **GetFederationInformation** o contiene un dominio con los valores de configuración que se solicitan en una solicitud de **GetDomainSettings** .</span><span class="sxs-lookup"><span data-stu-id="f6520-104">The **Domain** element contains a federated domain in a **GetFederationInformation** response or contains a domain the configuration settings for which are requested in a **GetDomainSettings** request.</span></span> 
  
```XML
<Domain/> 
```

 <span data-ttu-id="f6520-105">**string**</span><span class="sxs-lookup"><span data-stu-id="f6520-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6520-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f6520-106">Attributes and elements</span></span>

<span data-ttu-id="f6520-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f6520-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6520-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f6520-108">Attributes</span></span>

<span data-ttu-id="f6520-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f6520-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6520-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f6520-110">Child elements</span></span>

<span data-ttu-id="f6520-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f6520-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f6520-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f6520-112">Parent elements</span></span>

|<span data-ttu-id="f6520-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f6520-113">**Element**</span></span>|<span data-ttu-id="f6520-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6520-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6520-115">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f6520-115">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="f6520-116">Representa los dominios a los que se devuelven las opciones de configuración en una operación **GetDomainSettings** o los dominios que la organización ha federado en una operación **GetFederationInformation** .</span><span class="sxs-lookup"><span data-stu-id="f6520-116">Represents the domains the configuration settings for which are returned in a **GetDomainSettings** operation or the domains that the organization has federated in a **GetFederationInformation** operation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f6520-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f6520-117">Text value</span></span>

<span data-ttu-id="f6520-118">El valor de texto del elemento **Domain** representa un nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="f6520-118">The text value of the **Domain** element represents a domain name.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f6520-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f6520-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6520-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6520-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f6520-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f6520-121">Schema Name</span></span>  <br/> |<span data-ttu-id="f6520-122">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="f6520-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f6520-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f6520-123">Validation File</span></span>  <br/> |<span data-ttu-id="f6520-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f6520-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f6520-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f6520-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="f6520-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f6520-126">True</span></span>  <br/> |
   

