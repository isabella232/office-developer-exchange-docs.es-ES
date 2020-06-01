---
title: Indirecciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ImAddresses
api_type:
- schema
ms.assetid: 29f614a7-7fe6-47fa-b5f2-8feff106aa99
description: El elemento imaddresses representa una colección de direcciones de mensajería instantánea de un contacto.
ms.openlocfilehash: 24ff74d29c918d71116e25e097878b6e4e0a8ead
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460431"
---
# <a name="imaddresses"></a><span data-ttu-id="196d8-103">Indirecciones</span><span class="sxs-lookup"><span data-stu-id="196d8-103">ImAddresses</span></span>

<span data-ttu-id="196d8-104">El elemento **Imaddresses** representa una colección de direcciones de mensajería instantánea de un contacto.</span><span class="sxs-lookup"><span data-stu-id="196d8-104">The **ImAddresses** element represents a collection of instant messaging addresses for a contact.</span></span> 
  
```xml
<ImAddresses>
   <Entry/>
</ImAddresses>
```

 <span data-ttu-id="196d8-105">**ImAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="196d8-105">**ImAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="196d8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="196d8-106">Attributes and elements</span></span>

<span data-ttu-id="196d8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="196d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="196d8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="196d8-108">Attributes</span></span>

<span data-ttu-id="196d8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="196d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="196d8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="196d8-110">Child elements</span></span>

|<span data-ttu-id="196d8-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="196d8-111">**Element**</span></span>|<span data-ttu-id="196d8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="196d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="196d8-113">Entrada (IMAddress)</span><span class="sxs-lookup"><span data-stu-id="196d8-113">Entry (IMAddress)</span></span>](entry-imaddress.md) <br/> |<span data-ttu-id="196d8-114">Representa una dirección de mensajería instantánea de un contacto.</span><span class="sxs-lookup"><span data-stu-id="196d8-114">Represents an instant messaging address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="196d8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="196d8-115">Parent elements</span></span>

|<span data-ttu-id="196d8-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="196d8-116">**Element**</span></span>|<span data-ttu-id="196d8-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="196d8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="196d8-118">Contacto</span><span class="sxs-lookup"><span data-stu-id="196d8-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="196d8-119">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="196d8-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="196d8-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="196d8-120">Remarks</span></span>

<span data-ttu-id="196d8-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="196d8-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="196d8-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="196d8-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="196d8-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="196d8-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="196d8-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="196d8-124">Schema name</span></span>  <br/> |<span data-ttu-id="196d8-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="196d8-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="196d8-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="196d8-126">Validation file</span></span>  <br/> |<span data-ttu-id="196d8-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="196d8-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="196d8-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="196d8-128">Can be empty</span></span>  <br/> |<span data-ttu-id="196d8-129">Falso</span><span class="sxs-lookup"><span data-stu-id="196d8-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="196d8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="196d8-130">See also</span></span>



- [<span data-ttu-id="196d8-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="196d8-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

