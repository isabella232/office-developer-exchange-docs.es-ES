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
ms.openlocfilehash: ec7ef2d72ae922c751f8f50b72ff7d6b31b212ca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459969"
---
# <a name="internaldomains-smtpdomainlist"></a><span data-ttu-id="be795-103">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="be795-103">InternalDomains (SmtpDomainList)</span></span>

<span data-ttu-id="be795-104">El elemento **InternalDomains** identifica la lista de dominios SMTP internos de la organización.</span><span class="sxs-lookup"><span data-stu-id="be795-104">The **InternalDomains** element identifies the list of internal SMTP domains of the organization.</span></span> 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 <span data-ttu-id="be795-105">**SmtpDomainList**</span><span class="sxs-lookup"><span data-stu-id="be795-105">**SmtpDomainList**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="be795-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="be795-106">Attributes and elements</span></span>

<span data-ttu-id="be795-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="be795-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be795-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="be795-108">Attributes</span></span>

<span data-ttu-id="be795-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="be795-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be795-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="be795-110">Child elements</span></span>

|<span data-ttu-id="be795-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="be795-111">**Element**</span></span>|<span data-ttu-id="be795-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be795-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be795-113">Dominio</span><span class="sxs-lookup"><span data-stu-id="be795-113">Domain</span></span>](domain.md) <br/> |<span data-ttu-id="be795-114">Identifica un solo dominio SMTP.</span><span class="sxs-lookup"><span data-stu-id="be795-114">Identifies a single SMTP domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="be795-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="be795-115">Parent elements</span></span>

|<span data-ttu-id="be795-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="be795-116">**Element**</span></span>|<span data-ttu-id="be795-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be795-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be795-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="be795-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="be795-119">Contiene información de configuración del servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="be795-119">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="be795-120">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="be795-120">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="be795-121">Contiene la información de configuración del servicio para el servicio de reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="be795-121">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="be795-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="be795-122">Text value</span></span>

<span data-ttu-id="be795-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="be795-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be795-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be795-124">Remarks</span></span>

<span data-ttu-id="be795-125">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="be795-125">This element is required.</span></span> 
  
<span data-ttu-id="be795-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="be795-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be795-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="be795-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be795-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="be795-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be795-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="be795-129">Schema Name</span></span>  <br/> |<span data-ttu-id="be795-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="be795-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="be795-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="be795-131">Validation File</span></span>  <br/> |<span data-ttu-id="be795-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="be795-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="be795-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="be795-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="be795-134">Falso</span><span class="sxs-lookup"><span data-stu-id="be795-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be795-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="be795-135">See also</span></span>



- [<span data-ttu-id="be795-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="be795-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

