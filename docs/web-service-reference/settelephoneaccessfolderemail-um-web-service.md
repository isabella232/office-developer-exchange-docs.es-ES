---
title: SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 90759da7-6dba-499e-b8c8-e44a016b3198
description: El elemento SetTelephoneAccessFolderEmail define una solicitud para establecer la carpeta de correo electrónico predeterminada desde la que la mensajería unificada leerá los mensajes a través del teléfono.
ms.openlocfilehash: 806bdb1f0c7930a9e89555192aa32ad997716e7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467322"
---
# <a name="settelephoneaccessfolderemail-um-web-service"></a><span data-ttu-id="a4eae-103">SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a4eae-103">SetTelephoneAccessFolderEmail (UM web service)</span></span>

<span data-ttu-id="a4eae-104">El elemento **SetTelephoneAccessFolderEmail** define una solicitud para establecer la carpeta de correo electrónico predeterminada desde la que la mensajería unificada leerá los mensajes a través del teléfono.</span><span class="sxs-lookup"><span data-stu-id="a4eae-104">The **SetTelephoneAccessFolderEmail** element defines a request to set the default e-mail folder from which Unified Messaging will read messages over the telephone.</span></span> 
  
[<span data-ttu-id="a4eae-105">SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a4eae-105">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
```xml
<SetTelephoneAccessFolderEmail>
  <base64FolderId>   </base64FolderId>
</SetTelephoneAccessFolderEmail>
```

 <span data-ttu-id="a4eae-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="a4eae-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4eae-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a4eae-107">Attributes and elements</span></span>

<span data-ttu-id="a4eae-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a4eae-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4eae-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4eae-109">Attributes</span></span>

<span data-ttu-id="a4eae-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a4eae-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4eae-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a4eae-111">Child elements</span></span>

|<span data-ttu-id="a4eae-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a4eae-112">**Element**</span></span>|<span data-ttu-id="a4eae-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4eae-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4eae-114">base64FolderId (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a4eae-114">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md) <br/> |<span data-ttu-id="a4eae-115">El identificador de la carpeta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a4eae-115">The identifier of the e-mail folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a4eae-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a4eae-116">Parent elements</span></span>

<span data-ttu-id="a4eae-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a4eae-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a4eae-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a4eae-118">Text value</span></span>

<span data-ttu-id="a4eae-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a4eae-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4eae-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a4eae-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4eae-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4eae-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a4eae-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a4eae-122">Schema Name</span></span>  <br/> |<span data-ttu-id="a4eae-123">Mensajes</span><span class="sxs-lookup"><span data-stu-id="a4eae-123">Messages</span></span>  <br/> |
|<span data-ttu-id="a4eae-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a4eae-124">Validation File</span></span>  <br/> |<span data-ttu-id="a4eae-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a4eae-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a4eae-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a4eae-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4eae-127">Falso</span><span class="sxs-lookup"><span data-stu-id="a4eae-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4eae-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4eae-128">See also</span></span>



[<span data-ttu-id="a4eae-129">Operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a4eae-129">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)

