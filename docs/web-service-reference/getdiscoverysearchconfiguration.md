---
title: GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e15dbfca-3b9d-463e-94ec-4f1b6115bee3
description: El elemento GetDiscoverySearchConfiguration especifica una solicitud para recuperar la configuración de búsqueda de eDiscovery.
ms.openlocfilehash: 821c5e1429c160e326f6d99df3ff4fcc831b83d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461005"
---
# <a name="getdiscoverysearchconfiguration"></a><span data-ttu-id="05f7f-103">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="05f7f-103">GetDiscoverySearchConfiguration</span></span>

<span data-ttu-id="05f7f-104">El elemento **GetDiscoverySearchConfiguration** especifica una solicitud para recuperar la configuración de búsqueda de eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="05f7f-104">The **GetDiscoverySearchConfiguration** element specifies a request to retrieve the eDiscovery search configuration.</span></span> 
  
```XML
<GetDiscoverySearchConfiguration>
    <SearchId/>
    <ExpandGroupMembership/>
</GetDiscoverySearchConfiguration>
```

 <span data-ttu-id="05f7f-105">**GetDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="05f7f-105">**GetDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05f7f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="05f7f-106">Attributes and elements</span></span>

<span data-ttu-id="05f7f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="05f7f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05f7f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="05f7f-108">Attributes</span></span>

<span data-ttu-id="05f7f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="05f7f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05f7f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="05f7f-110">Child elements</span></span>

|<span data-ttu-id="05f7f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="05f7f-111">**Element**</span></span>|<span data-ttu-id="05f7f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05f7f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05f7f-113">SearchId</span><span class="sxs-lookup"><span data-stu-id="05f7f-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="05f7f-114">Especifica el identificador de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="05f7f-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="05f7f-115">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="05f7f-115">ExpandGroupMembership</span></span>](expandgroupmembership.md) <br/> |<span data-ttu-id="05f7f-116">Contiene un valor booleano que indica si se va a expandir la pertenencia del grupo devuelto desde una solicitud **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="05f7f-116">Contains a Boolean value that indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05f7f-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="05f7f-117">Parent elements</span></span>

<span data-ttu-id="05f7f-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05f7f-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05f7f-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05f7f-119">Remarks</span></span>

<span data-ttu-id="05f7f-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="05f7f-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="05f7f-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="05f7f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05f7f-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="05f7f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05f7f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="05f7f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="05f7f-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="05f7f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="05f7f-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="05f7f-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="05f7f-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="05f7f-126">Validation File</span></span>  <br/> |<span data-ttu-id="05f7f-127">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="05f7f-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="05f7f-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="05f7f-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="05f7f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="05f7f-129">See also</span></span>



- [<span data-ttu-id="05f7f-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="05f7f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

