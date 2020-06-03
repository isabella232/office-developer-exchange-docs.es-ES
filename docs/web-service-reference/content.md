---
title: Contenido
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Content
api_type:
- schema
ms.assetid: 24f8c54a-505f-4fc0-b7e7-93ad50b97070
description: El elemento Content contiene el contenido codificado en Base64 de un archivo de datos adjuntos.
ms.openlocfilehash: 81f6acf69ff702bd0645663cb2e499ee5b45ea78
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458953"
---
# <a name="content"></a><span data-ttu-id="da2b3-103">Contenido</span><span class="sxs-lookup"><span data-stu-id="da2b3-103">Content</span></span>

<span data-ttu-id="da2b3-104">El elemento **Content** contiene el contenido codificado en Base64 de un archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="da2b3-104">The **Content** element contains the Base64-encoded contents of a file attachment.</span></span> 
  
```xml
<Content/>
```

 <span data-ttu-id="da2b3-105">**Base64Binary**</span><span class="sxs-lookup"><span data-stu-id="da2b3-105">**Base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da2b3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="da2b3-106">Attributes and elements</span></span>

<span data-ttu-id="da2b3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="da2b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da2b3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="da2b3-108">Attributes</span></span>

<span data-ttu-id="da2b3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="da2b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da2b3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="da2b3-110">Child elements</span></span>

<span data-ttu-id="da2b3-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="da2b3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="da2b3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="da2b3-112">Parent elements</span></span>

|<span data-ttu-id="da2b3-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="da2b3-113">**Element**</span></span>|<span data-ttu-id="da2b3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da2b3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da2b3-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="da2b3-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="da2b3-116">Representa un archivo t se thattached a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="da2b3-116">Represents a file t is thattached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da2b3-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="da2b3-117">Text value</span></span>

<span data-ttu-id="da2b3-118">El valor de cadena representa los datos binarios codificados en base64 del archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="da2b3-118">The string value represents the Base64-encoded binary data of the file attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da2b3-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da2b3-119">Remarks</span></span>

<span data-ttu-id="da2b3-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="da2b3-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da2b3-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="da2b3-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da2b3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="da2b3-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da2b3-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="da2b3-123">Schema name</span></span>  <br/> |<span data-ttu-id="da2b3-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="da2b3-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="da2b3-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="da2b3-125">Validation file</span></span>  <br/> |<span data-ttu-id="da2b3-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="da2b3-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da2b3-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="da2b3-127">Can be empty</span></span>  <br/> |<span data-ttu-id="da2b3-128">Falso</span><span class="sxs-lookup"><span data-stu-id="da2b3-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da2b3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="da2b3-129">See also</span></span>



- [<span data-ttu-id="da2b3-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="da2b3-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

