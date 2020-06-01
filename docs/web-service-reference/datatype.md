---
title: DataType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DataType
api_type:
- schema
ms.assetid: 267fe5aa-f9b1-4d4c-ac11-0f2e50ec2627
description: El elemento DataType describe el tipo de datos que comparte una carpeta compartida.
ms.openlocfilehash: a7df8d38e10f0ab31038d790d8f35208d1be66d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458834"
---
# <a name="datatype"></a><span data-ttu-id="65774-103">DataType</span><span class="sxs-lookup"><span data-stu-id="65774-103">DataType</span></span>

<span data-ttu-id="65774-104">El elemento **DataType** describe el tipo de datos que comparte una carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="65774-104">The **DataType** element describes the type of data that is shared by a shared folder.</span></span> 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

<span data-ttu-id="65774-105">**SharingDataType**</span><span class="sxs-lookup"><span data-stu-id="65774-105">**SharingDataType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="65774-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65774-106">Attributes and elements</span></span>

<span data-ttu-id="65774-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65774-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65774-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="65774-108">Attributes</span></span>

<span data-ttu-id="65774-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65774-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65774-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65774-110">Child elements</span></span>

<span data-ttu-id="65774-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65774-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="65774-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65774-112">Parent elements</span></span>

|<span data-ttu-id="65774-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65774-113">**Element**</span></span>|<span data-ttu-id="65774-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65774-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65774-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="65774-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="65774-116">Define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="65774-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="65774-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="65774-117">Text value</span></span>

<span data-ttu-id="65774-118">En la siguiente tabla se enumeran los valores posibles para el elemento **DataType** .</span><span class="sxs-lookup"><span data-stu-id="65774-118">The following table lists the possible values for the **DataType** element.</span></span> 
  
<span data-ttu-id="65774-119">**Valores del elemento DataType**</span><span class="sxs-lookup"><span data-stu-id="65774-119">**DataType element values**</span></span>

|<span data-ttu-id="65774-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="65774-120">**Value**</span></span>|<span data-ttu-id="65774-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65774-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65774-122">Calendar</span><span class="sxs-lookup"><span data-stu-id="65774-122">Calendar</span></span>  <br/> |<span data-ttu-id="65774-123">Indica que la carpeta compartida contiene información del calendario.</span><span class="sxs-lookup"><span data-stu-id="65774-123">Indicates that the shared folder contains calendar information.</span></span>  <br/> |
|<span data-ttu-id="65774-124">Contactos</span><span class="sxs-lookup"><span data-stu-id="65774-124">Contacts</span></span>  <br/> |<span data-ttu-id="65774-125">Indica que la carpeta compartida contiene información de contacto.</span><span class="sxs-lookup"><span data-stu-id="65774-125">Indicates that the shared folder contains contact information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65774-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65774-126">Remarks</span></span>

<span data-ttu-id="65774-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="65774-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65774-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65774-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65774-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="65774-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65774-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65774-130">Schema Name</span></span>  <br/> |<span data-ttu-id="65774-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="65774-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="65774-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65774-132">Validation File</span></span>  <br/> |<span data-ttu-id="65774-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="65774-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65774-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65774-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="65774-135">Falso</span><span class="sxs-lookup"><span data-stu-id="65774-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65774-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="65774-136">See also</span></span>

- [<span data-ttu-id="65774-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="65774-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

