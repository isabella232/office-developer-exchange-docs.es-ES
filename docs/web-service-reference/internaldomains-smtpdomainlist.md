---
title: InternalDomains (SmtpDomainList)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternalDomains
api_type:
- schema
ms.assetid: 0f2cbb05-338d-4302-8871-a06e78b33f98
description: El elemento InternalDomains identifica la lista de dominios SMTP internos de la organización.
ms.openlocfilehash: f37a31f4348a7eb0024656489f249dec349bc67b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835953"
---
# <a name="internaldomains-smtpdomainlist"></a><span data-ttu-id="afcf8-103">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="afcf8-103">InternalDomains (SmtpDomainList)</span></span>

<span data-ttu-id="afcf8-104">El elemento **InternalDomains** identifica la lista de dominios SMTP internos de la organización.</span><span class="sxs-lookup"><span data-stu-id="afcf8-104">The **InternalDomains** element identifies the list of internal SMTP domains of the organization.</span></span> 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 <span data-ttu-id="afcf8-105">**SmtpDomainList**</span><span class="sxs-lookup"><span data-stu-id="afcf8-105">**SmtpDomainList**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afcf8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="afcf8-106">Attributes and elements</span></span>

<span data-ttu-id="afcf8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="afcf8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afcf8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="afcf8-108">Attributes</span></span>

<span data-ttu-id="afcf8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afcf8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="afcf8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="afcf8-110">Child elements</span></span>

|<span data-ttu-id="afcf8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="afcf8-111">**Element**</span></span>|<span data-ttu-id="afcf8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afcf8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afcf8-113">Domain</span><span class="sxs-lookup"><span data-stu-id="afcf8-113">Domain</span></span>](domain.md) <br/> |<span data-ttu-id="afcf8-114">Identifica un único dominio SMTP.</span><span class="sxs-lookup"><span data-stu-id="afcf8-114">Identifies a single SMTP domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afcf8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="afcf8-115">Parent elements</span></span>

|<span data-ttu-id="afcf8-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="afcf8-116">**Element**</span></span>|<span data-ttu-id="afcf8-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afcf8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afcf8-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="afcf8-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="afcf8-119">Contiene información de configuración de servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="afcf8-119">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="afcf8-120">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="afcf8-120">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="afcf8-121">Contiene información de configuración de servicio para el servicio de protección de las reglas.</span><span class="sxs-lookup"><span data-stu-id="afcf8-121">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="afcf8-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="afcf8-122">Text value</span></span>

<span data-ttu-id="afcf8-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afcf8-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afcf8-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afcf8-124">Remarks</span></span>

<span data-ttu-id="afcf8-125">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="afcf8-125">This element is required.</span></span> 
  
<span data-ttu-id="afcf8-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="afcf8-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afcf8-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="afcf8-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afcf8-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="afcf8-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="afcf8-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="afcf8-129">Schema Name</span></span>  <br/> |<span data-ttu-id="afcf8-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="afcf8-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="afcf8-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="afcf8-131">Validation File</span></span>  <br/> |<span data-ttu-id="afcf8-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="afcf8-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="afcf8-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="afcf8-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="afcf8-134">False</span><span class="sxs-lookup"><span data-stu-id="afcf8-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afcf8-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="afcf8-135">See also</span></span>



- [<span data-ttu-id="afcf8-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="afcf8-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

