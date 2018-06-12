---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: El elemento PostalAddress especifica la dirección postal para un rol.
ms.openlocfilehash: fb418154867aebb4d284e75be579003c0ddc88f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836855"
---
# <a name="postaladdress-personapostaladdresstype"></a><span data-ttu-id="462f3-103">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="462f3-103">PostalAddress (PersonaPostalAddressType)</span></span>

<span data-ttu-id="462f3-104">El elemento **PostalAddress** especifica la dirección postal para un rol.</span><span class="sxs-lookup"><span data-stu-id="462f3-104">The **PostalAddress** element specifies the postal address for a persona.</span></span> 
  
```XML
<PostalAddress>
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
</PostalAddress>
```

 <span data-ttu-id="462f3-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="462f3-105">**PersonaPostalAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="462f3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="462f3-106">Attributes and elements</span></span>

<span data-ttu-id="462f3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="462f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="462f3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="462f3-108">Attributes</span></span>

<span data-ttu-id="462f3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="462f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="462f3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="462f3-110">Child elements</span></span>

<span data-ttu-id="462f3-111">[Calle](street.md) | [Ciudad](city.md) | [estado](state-ex15websvcsotherref.md) | [país](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [(string) de tipo](type-string.md) | [latitud](latitude.md)  |  [ Longitud](longitude.md) | [precisión](accuracy.md) | [altitud](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="462f3-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="462f3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="462f3-112">Parent elements</span></span>

[<span data-ttu-id="462f3-113">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="462f3-113">EnhancedLocation</span></span>](enhancedlocation.md)
  
## <a name="remarks"></a><span data-ttu-id="462f3-114">Notas</span><span class="sxs-lookup"><span data-stu-id="462f3-114">Remarks</span></span>

<span data-ttu-id="462f3-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="462f3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="462f3-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="462f3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="462f3-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="462f3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="462f3-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="462f3-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="462f3-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="462f3-119">Schema name</span></span>  <br/> |<span data-ttu-id="462f3-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="462f3-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="462f3-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="462f3-121">Validation file</span></span>  <br/> |<span data-ttu-id="462f3-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="462f3-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="462f3-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="462f3-123">Can be empty</span></span>  <br/> ||
   

