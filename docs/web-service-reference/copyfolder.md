---
title: CopyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: 7d5cd08a-fe81-4cb6-a5a0-6dec2d3c93d4
description: El elemento CopyFolder define una solicitud para copiar carpetas en un buzón de correo en el almacén de Exchange.
ms.openlocfilehash: fa75272540169a96d5567181d27b8a8f056cce42
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452513"
---
# <a name="copyfolder"></a><span data-ttu-id="0ab0b-103">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="0ab0b-103">CopyFolder</span></span>

<span data-ttu-id="0ab0b-104">El elemento **CopyFolder** define una solicitud para copiar carpetas en un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ab0b-104">The **CopyFolder** element defines a request to copy folders in a mailbox in the Exchange store.</span></span> 
  
```xml
<CopyFolder>
   <ToFolderId/>
   <FolderIds/>
</CopyFolder>
```

 <span data-ttu-id="0ab0b-105">**CopyFolderType**</span><span class="sxs-lookup"><span data-stu-id="0ab0b-105">**CopyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ab0b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0ab0b-106">Attributes and elements</span></span>

<span data-ttu-id="0ab0b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0ab0b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ab0b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ab0b-108">Attributes</span></span>

<span data-ttu-id="0ab0b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0ab0b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ab0b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ab0b-110">Child elements</span></span>

|<span data-ttu-id="0ab0b-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0ab0b-111">**Element**</span></span>|<span data-ttu-id="0ab0b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ab0b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ab0b-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="0ab0b-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="0ab0b-114">Representa la carpeta de destino de una carpeta copiada.</span><span class="sxs-lookup"><span data-stu-id="0ab0b-114">Represents the destination folder for a copied folder.</span></span>  <br/> |
|[<span data-ttu-id="0ab0b-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="0ab0b-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="0ab0b-116">Contiene una matriz de carpetas para copiar a la carpeta identificada por el elemento [ToFolderId](tofolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="0ab0b-116">Contains an array of folders to copy to the folder identified by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ab0b-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ab0b-117">Parent elements</span></span>

<span data-ttu-id="0ab0b-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ab0b-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ab0b-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ab0b-119">Remarks</span></span>

<span data-ttu-id="0ab0b-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="0ab0b-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ab0b-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0ab0b-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ab0b-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ab0b-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0ab0b-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0ab0b-123">Schema Name</span></span>  <br/> |<span data-ttu-id="0ab0b-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0ab0b-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0ab0b-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0ab0b-125">Validation File</span></span>  <br/> |<span data-ttu-id="0ab0b-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0ab0b-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0ab0b-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0ab0b-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="0ab0b-128">Falso</span><span class="sxs-lookup"><span data-stu-id="0ab0b-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ab0b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ab0b-129">See also</span></span>



[<span data-ttu-id="0ab0b-130">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="0ab0b-130">CopyFolder operation</span></span>](copyfolder-operation.md)

