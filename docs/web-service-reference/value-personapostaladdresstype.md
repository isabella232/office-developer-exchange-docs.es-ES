---
title: Valor (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be838fc2-cfcb-4856-b095-a8e5366bb6c6
description: El elemento Value especifica información asociada con una dirección postal.
ms.openlocfilehash: 2d644ff45fe89061ccd90279773f3a5a5b7fe7cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466475"
---
# <a name="value-personapostaladdresstype"></a><span data-ttu-id="1740b-103">Valor (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="1740b-103">Value (PersonaPostalAddressType)</span></span>

<span data-ttu-id="1740b-104">El elemento **Value** especifica información asociada con una dirección postal.</span><span class="sxs-lookup"><span data-stu-id="1740b-104">The **Value** element specifies information associated with a postal address.</span></span> 
  
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

<span data-ttu-id="1740b-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="1740b-105">**PersonaPostalAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1740b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1740b-106">Attributes and elements</span></span>

<span data-ttu-id="1740b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1740b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1740b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1740b-108">Attributes</span></span>

<span data-ttu-id="1740b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1740b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1740b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1740b-110">Child elements</span></span>

<span data-ttu-id="1740b-111">[Calle](street.md)  |  [City](city.md)  |  [Provincia o estado](state-ex15websvcsotherref.md)  |  [País](country.md)  |  [CódigoPostal](postalcode.md)  |  [PostOfficeBox](postofficebox.md)  |  [Tipo (cadena)](type-string.md)  |  [Latitud](latitude.md)  |  [Longitud](longitude.md)  |  [Precisión](accuracy.md)  |  [Altitud](altitude.md)  |  [AltitudeAccuracy](altitudeaccuracy.md)  |  [FormattedAddress](formattedaddress.md)  |  [LocationUri](locationuri.md)  |  [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="1740b-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1740b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1740b-112">Parent elements</span></span>

[<span data-ttu-id="1740b-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="1740b-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="1740b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1740b-114">Remarks</span></span>

<span data-ttu-id="1740b-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1740b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1740b-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1740b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1740b-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1740b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1740b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1740b-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1740b-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1740b-119">Schema name</span></span>  <br/> |<span data-ttu-id="1740b-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1740b-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1740b-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1740b-121">Validation file</span></span>  <br/> |<span data-ttu-id="1740b-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1740b-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1740b-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1740b-123">Can be empty</span></span>  <br/> ||
   

