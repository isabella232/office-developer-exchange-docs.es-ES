---
title: CreateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 110bada1-517b-4bd6-870d-7086dc879e5d
description: El elemento CreateFolder define una solicitud para crear una carpeta en el almacén de Exchange.
ms.openlocfilehash: c2a971a6b827553a1632c2a86e4d36e3b83a2de3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457546"
---
# <a name="createfolder"></a><span data-ttu-id="c0c77-103">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="c0c77-103">CreateFolder</span></span>

<span data-ttu-id="c0c77-104">El elemento **CreateFolder** define una solicitud para crear una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0c77-104">The **CreateFolder** element defines a request to create a folder in the Exchange store.</span></span> 
  
```xml
<CreateFolder>
   <ParentFolderId/>
   <Folders/>
</CreateFolder>
```

 <span data-ttu-id="c0c77-105">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="c0c77-105">**CreateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0c77-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c0c77-106">Attributes and elements</span></span>

<span data-ttu-id="c0c77-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c0c77-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0c77-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c0c77-108">Attributes</span></span>

<span data-ttu-id="c0c77-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c0c77-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0c77-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c0c77-110">Child elements</span></span>

|<span data-ttu-id="c0c77-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c0c77-111">**Element**</span></span>|<span data-ttu-id="c0c77-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0c77-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0c77-113">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="c0c77-113">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="c0c77-114">Elemento que identifica la ubicación en la que se crea la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="c0c77-114">The element that identifies the location where the new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="c0c77-115">Folders</span><span class="sxs-lookup"><span data-stu-id="c0c77-115">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c0c77-116">Elemento que contiene todas las carpetas que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="c0c77-116">The element that contains all the folders to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0c77-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c0c77-117">Parent elements</span></span>

<span data-ttu-id="c0c77-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c0c77-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0c77-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0c77-119">Remarks</span></span>

<span data-ttu-id="c0c77-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c0c77-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0c77-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c0c77-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0c77-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0c77-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0c77-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c0c77-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c0c77-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c0c77-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="c0c77-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c0c77-125">Validation File</span></span>  <br/> |<span data-ttu-id="c0c77-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c0c77-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0c77-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c0c77-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0c77-128">Falso</span><span class="sxs-lookup"><span data-stu-id="c0c77-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0c77-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0c77-129">See also</span></span>



[<span data-ttu-id="c0c77-130">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="c0c77-130">CreateFolder operation</span></span>](createfolder-operation.md)


[<span data-ttu-id="c0c77-131">Creación de carpetas (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="c0c77-131">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

