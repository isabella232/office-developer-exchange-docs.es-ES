---
title: Valor (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be838fc2-cfcb-4856-b095-a8e5366bb6c6
description: El elemento de valor especifica la información asociada con una dirección postal.
ms.openlocfilehash: 048d3a49552f1a9e89744e4cd16ec1745417e923
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840950"
---
# <a name="value-personapostaladdresstype"></a><span data-ttu-id="a1a9d-103">Valor (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="a1a9d-103">Value (PersonaPostalAddressType)</span></span>

<span data-ttu-id="a1a9d-104">El elemento de **valor** especifica información asociada con una dirección postal.</span><span class="sxs-lookup"><span data-stu-id="a1a9d-104">The **Value** element specifies information associated with a postal address.</span></span> 
  
```XML
<Value>
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
   <PostOfficeBox/>
   <Type/>
   <Latitude/>
   <Longitude/>
   <Accuracy/>
   <Altitude/>
   <AltitudeAccuracy/>
   <FormattedAddress/>
   <LocationUri/>
   <LocationSource/>
</Value>
```

<span data-ttu-id="a1a9d-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="a1a9d-105">**PersonaPostalAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a1a9d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a1a9d-106">Attributes and elements</span></span>

<span data-ttu-id="a1a9d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a1a9d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1a9d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a1a9d-108">Attributes</span></span>

<span data-ttu-id="a1a9d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1a9d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1a9d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a1a9d-110">Child elements</span></span>

<span data-ttu-id="a1a9d-111">[Calle](street.md) | [Ciudad](city.md) | [estado](state-ex15websvcsotherref.md) | [país](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [(string) de tipo](type-string.md) | [latitud](latitude.md)  |  [ Longitud](longitude.md) | [precisión](accuracy.md) | [altitud](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="a1a9d-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a1a9d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a1a9d-112">Parent elements</span></span>

[<span data-ttu-id="a1a9d-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="a1a9d-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="a1a9d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1a9d-114">Remarks</span></span>

<span data-ttu-id="a1a9d-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a1a9d-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a1a9d-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a1a9d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1a9d-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a1a9d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1a9d-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a1a9d-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a1a9d-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a1a9d-119">Schema name</span></span>  <br/> |<span data-ttu-id="a1a9d-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a1a9d-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="a1a9d-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a1a9d-121">Validation file</span></span>  <br/> |<span data-ttu-id="a1a9d-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a1a9d-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a1a9d-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a1a9d-123">Can be empty</span></span>  <br/> ||
   

