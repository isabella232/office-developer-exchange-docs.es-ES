---
title: NombreDeOpción (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8bcb0411-58b0-4e37-b97e-00c07dcbecb1
description: El elemento nombreDeOpción representa el nombre de una configuración en la respuesta.
ms.openlocfilehash: 9bf7c8197693bc6887a99ffcbeb2240e1f4c3b20
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837468"
---
# <a name="settingname-soap"></a><span data-ttu-id="68b15-103">NombreDeOpción (SOAP)</span><span class="sxs-lookup"><span data-stu-id="68b15-103">SettingName (SOAP)</span></span>

<span data-ttu-id="68b15-104">El elemento **nombreDeOpción** representa el nombre de una configuración en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68b15-104">The **SettingName** element represents the name of a setting in the response.</span></span> 
  
```XML
<SettingName/>
```

 <span data-ttu-id="68b15-105">**string**</span><span class="sxs-lookup"><span data-stu-id="68b15-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68b15-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="68b15-106">Attributes and elements</span></span>

<span data-ttu-id="68b15-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="68b15-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68b15-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="68b15-108">Attributes</span></span>

<span data-ttu-id="68b15-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="68b15-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68b15-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="68b15-110">Child elements</span></span>

<span data-ttu-id="68b15-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="68b15-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="68b15-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="68b15-112">Parent elements</span></span>

|<span data-ttu-id="68b15-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="68b15-113">**Element**</span></span>|<span data-ttu-id="68b15-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68b15-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68b15-115">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="68b15-115">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="68b15-116">Representa un error que se devuelve al recuperar una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="68b15-116">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="68b15-117">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="68b15-117">DomainSettingError (SOAP)</span></span>](domainsettingerror-soap.md) <br/> |<span data-ttu-id="68b15-118">Representa un error que se produjo durante la recuperación de una configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="68b15-118">Represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="68b15-119">Esto representa un error de una solicitud de **GetDomainSettings** .</span><span class="sxs-lookup"><span data-stu-id="68b15-119">This represents an error from a **GetDomainSettings** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="68b15-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="68b15-120">Text value</span></span>

<span data-ttu-id="68b15-121">El valor del elemento **nombreDeOpción** representa el nombre de una configuración en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="68b15-121">The value of the **SettingName** element represents the name of a setting in a response.</span></span> 
  
<span data-ttu-id="68b15-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="68b15-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68b15-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="68b15-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68b15-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68b15-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="68b15-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="68b15-125">Schema Name</span></span>  <br/> |<span data-ttu-id="68b15-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="68b15-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="68b15-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="68b15-127">Validation File</span></span>  <br/> |<span data-ttu-id="68b15-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="68b15-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="68b15-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="68b15-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="68b15-130">True</span><span class="sxs-lookup"><span data-stu-id="68b15-130">True</span></span>  <br/> |
   

