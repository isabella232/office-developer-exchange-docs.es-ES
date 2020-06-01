---
title: GetFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 34e4c9ea-adcd-46bd-ae8f-7abb256c585a
description: El elemento GetFolder define una solicitud para obtener una carpeta de un buzón de correo en el almacén de Exchange.
ms.openlocfilehash: 41d2b1ab5fcd5d2d60c399e8070ca957ee4b66e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458708"
---
# <a name="getfolder"></a><span data-ttu-id="f7f14-103">GetFolder</span><span class="sxs-lookup"><span data-stu-id="f7f14-103">GetFolder</span></span>

<span data-ttu-id="f7f14-104">El elemento **GetFolder** define una solicitud para obtener una carpeta de un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f7f14-104">The **GetFolder** element defines a request to get a folder from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetFolder>
   <FolderShape/>
   <FolderIds/>
</GetFolder>
```

 <span data-ttu-id="f7f14-105">**GetFolderType**</span><span class="sxs-lookup"><span data-stu-id="f7f14-105">**GetFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7f14-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f7f14-106">Attributes and elements</span></span>

<span data-ttu-id="f7f14-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f7f14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7f14-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f7f14-108">Attributes</span></span>

<span data-ttu-id="f7f14-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f7f14-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7f14-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f7f14-110">Child elements</span></span>

|<span data-ttu-id="f7f14-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f7f14-111">**Element**</span></span>|<span data-ttu-id="f7f14-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7f14-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7f14-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="f7f14-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="f7f14-114">Identifica las propiedades que se van a obtener para cada carpeta identificada en el elemento [FolderIds](folderids.md) .</span><span class="sxs-lookup"><span data-stu-id="f7f14-114">Identifies the properties to get for each folder identified in the [FolderIds](folderids.md) element.</span></span>  <br/> |
|[<span data-ttu-id="f7f14-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="f7f14-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="f7f14-116">Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a obtener de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f7f14-116">Contains an array of folder identifiers that are used to identify folders to get from a mailbox in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f7f14-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f7f14-117">Parent elements</span></span>

<span data-ttu-id="f7f14-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f7f14-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7f14-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7f14-119">Remarks</span></span>

<span data-ttu-id="f7f14-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f7f14-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7f14-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f7f14-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7f14-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7f14-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f7f14-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f7f14-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f7f14-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f7f14-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="f7f14-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f7f14-125">Validation File</span></span>  <br/> |<span data-ttu-id="f7f14-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f7f14-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f7f14-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f7f14-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7f14-128">Falso</span><span class="sxs-lookup"><span data-stu-id="f7f14-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7f14-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7f14-129">See also</span></span>



[<span data-ttu-id="f7f14-130">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="f7f14-130">GetFolder operation</span></span>](getfolder-operation.md)

