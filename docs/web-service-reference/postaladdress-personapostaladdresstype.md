---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: El elemento PostalAddress especifica la dirección postal de un rol.
ms.openlocfilehash: 9e316e5e0135c2d18fab4067241988c65eceec66
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465390"
---
# <a name="postaladdress-personapostaladdresstype"></a><span data-ttu-id="a308a-103">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="a308a-103">PostalAddress (PersonaPostalAddressType)</span></span>

<span data-ttu-id="a308a-104">El elemento **PostalAddress** especifica la dirección postal de un rol.</span><span class="sxs-lookup"><span data-stu-id="a308a-104">The **PostalAddress** element specifies the postal address for a persona.</span></span> 
  
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

 <span data-ttu-id="a308a-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="a308a-105">**PersonaPostalAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a308a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a308a-106">Attributes and elements</span></span>

<span data-ttu-id="a308a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a308a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a308a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a308a-108">Attributes</span></span>

<span data-ttu-id="a308a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a308a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a308a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a308a-110">Child elements</span></span>

<span data-ttu-id="a308a-111">[Calle](street.md)  |  [City](city.md)  |  [Provincia o estado](state-ex15websvcsotherref.md)  |  [País](country.md)  |  [CódigoPostal](postalcode.md)  |  [PostOfficeBox](postofficebox.md)  |  [Tipo (cadena)](type-string.md)  |  [Latitud](latitude.md)  |  [Longitud](longitude.md)  |  [Precisión](accuracy.md)  |  [Altitud](altitude.md)  |  [AltitudeAccuracy](altitudeaccuracy.md)  |  [FormattedAddress](formattedaddress.md)  |  [LocationUri](locationuri.md)  |  [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="a308a-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a308a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a308a-112">Parent elements</span></span>

[<span data-ttu-id="a308a-113">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="a308a-113">EnhancedLocation</span></span>](enhancedlocation.md)
  
## <a name="remarks"></a><span data-ttu-id="a308a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a308a-114">Remarks</span></span>

<span data-ttu-id="a308a-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a308a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a308a-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a308a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a308a-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a308a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a308a-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a308a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a308a-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a308a-119">Schema name</span></span>  <br/> |<span data-ttu-id="a308a-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a308a-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="a308a-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a308a-121">Validation file</span></span>  <br/> |<span data-ttu-id="a308a-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a308a-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a308a-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a308a-123">Can be empty</span></span>  <br/> ||
   

