---
title: GetOrganizationRelationshipSettingsRequestMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec9ad6a0-1a3c-405b-a6ea-b8dd4323c22a
description: El elemento GetOrganizationRelationshipSettingRequestMessage representa una solicitud de operación GetOrganizationRelationshipSettings operación (SOAP). El elemento GetOrganizationRelationshipSettingRequestMessage es sólo para uso interno. Este elemento no se usa en los clientes.
ms.openlocfilehash: 357f6c75ff81fdf6b31bab15f4662d0f17fbbec0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764925"
---
# <a name="getorganizationrelationshipsettingsrequestmessage-soap"></a><span data-ttu-id="eb311-105">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="eb311-105">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span></span>

<span data-ttu-id="eb311-106">El elemento **GetOrganizationRelationshipSettingRequestMessage** representa una solicitud de operación de la [operación de GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="eb311-106">The **GetOrganizationRelationshipSettingRequestMessage** element represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation request.</span></span> <span data-ttu-id="eb311-107">El elemento **GetOrganizationRelationshipSettingRequestMessage** es sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="eb311-107">The **GetOrganizationRelationshipSettingRequestMessage** element is for internal use only.</span></span> <span data-ttu-id="eb311-108">Este elemento no se usa en los clientes.</span><span class="sxs-lookup"><span data-stu-id="eb311-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingRequestMessage>
   <Request/>
</GetOrganizationRelationshipSettingRequestMessage>
```

 <span data-ttu-id="eb311-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="eb311-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb311-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb311-110">Attributes and elements</span></span>

<span data-ttu-id="eb311-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb311-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb311-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb311-112">Attributes</span></span>

<span data-ttu-id="eb311-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb311-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb311-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb311-114">Child elements</span></span>

|<span data-ttu-id="eb311-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb311-115">**Element**</span></span>|<span data-ttu-id="eb311-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb311-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb311-117">Solicitud (SOAP) (GetOrganizationRelationship)</span><span class="sxs-lookup"><span data-stu-id="eb311-117">Request (GetOrganizationRelationship) (SOAP)</span></span>](request-getorganizationrelationshipsoap.md) <br/> |<span data-ttu-id="eb311-118">Representa una solicitud de [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="eb311-118">Represents a [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb311-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb311-119">Parent elements</span></span>

<span data-ttu-id="eb311-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb311-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb311-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb311-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb311-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb311-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="eb311-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb311-123">Schema Name</span></span>  <br/> |<span data-ttu-id="eb311-124">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="eb311-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="eb311-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb311-125">Validation File</span></span>  <br/> |<span data-ttu-id="eb311-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb311-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb311-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb311-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb311-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="eb311-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb311-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb311-129">See also</span></span>



[<span data-ttu-id="eb311-130">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="eb311-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

