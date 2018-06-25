---
title: Tipo de datos
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
description: El tipo del elemento describe el tipo de datos que se comparten por una carpeta compartida.
ms.openlocfilehash: b1adac8e3029abd64df96ab1560706babe4b12f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764036"
---
# <a name="datatype"></a><span data-ttu-id="a60b3-103">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a60b3-103">DataType</span></span>

<span data-ttu-id="a60b3-104">El **tipo** del elemento describe el tipo de datos que se comparten por una carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="a60b3-104">The **DataType** element describes the type of data that is shared by a shared folder.</span></span> 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

<span data-ttu-id="a60b3-105">**SharingDataType**</span><span class="sxs-lookup"><span data-stu-id="a60b3-105">**SharingDataType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a60b3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a60b3-106">Attributes and elements</span></span>

<span data-ttu-id="a60b3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a60b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a60b3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a60b3-108">Attributes</span></span>

<span data-ttu-id="a60b3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a60b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a60b3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a60b3-110">Child elements</span></span>

<span data-ttu-id="a60b3-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a60b3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a60b3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a60b3-112">Parent elements</span></span>

|<span data-ttu-id="a60b3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a60b3-113">**Element**</span></span>|<span data-ttu-id="a60b3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a60b3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a60b3-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="a60b3-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="a60b3-116">Define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="a60b3-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a60b3-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a60b3-117">Text value</span></span>

<span data-ttu-id="a60b3-118">En la siguiente tabla se enumera los valores posibles para el **tipo** del elemento.</span><span class="sxs-lookup"><span data-stu-id="a60b3-118">The following table lists the possible values for the **DataType** element.</span></span> 
  
<span data-ttu-id="a60b3-119">**Valores del elemento de tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a60b3-119">**DataType element values**</span></span>

|<span data-ttu-id="a60b3-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a60b3-120">**Value**</span></span>|<span data-ttu-id="a60b3-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a60b3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a60b3-122">Calendario</span><span class="sxs-lookup"><span data-stu-id="a60b3-122">Calendar</span></span>  <br/> |<span data-ttu-id="a60b3-123">Indica que la carpeta compartida contiene información de calendario.</span><span class="sxs-lookup"><span data-stu-id="a60b3-123">Indicates that the shared folder contains calendar information.</span></span>  <br/> |
|<span data-ttu-id="a60b3-124">Contactos</span><span class="sxs-lookup"><span data-stu-id="a60b3-124">Contacts</span></span>  <br/> |<span data-ttu-id="a60b3-125">Indica que la carpeta compartida contiene información de contacto.</span><span class="sxs-lookup"><span data-stu-id="a60b3-125">Indicates that the shared folder contains contact information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a60b3-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a60b3-126">Remarks</span></span>

<span data-ttu-id="a60b3-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a60b3-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a60b3-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a60b3-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a60b3-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a60b3-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a60b3-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a60b3-130">Schema Name</span></span>  <br/> |<span data-ttu-id="a60b3-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a60b3-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a60b3-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a60b3-132">Validation File</span></span>  <br/> |<span data-ttu-id="a60b3-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a60b3-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a60b3-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a60b3-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="a60b3-135">False</span><span class="sxs-lookup"><span data-stu-id="a60b3-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a60b3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a60b3-136">See also</span></span>

- [<span data-ttu-id="a60b3-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a60b3-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

