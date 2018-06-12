---
title: Tratamiento de mensajes de error de detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: Obtenga información sobre los diferentes tipos de errores de detección automática y qué hacer con ellos.
ms.openlocfilehash: fcafc799f4d35e92159d2913845474ecf7bc5657
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763014"
---
# <a name="handling-autodiscover-error-messages"></a>Tratamiento de mensajes de error de detección automática

Obtenga información sobre los diferentes tipos de errores de detección automática y qué hacer con ellos.
  
Detección automática permite a las aplicaciones recuperar información de configuración automáticamente y funciona muy bien. Sin embargo, las cosas no vaya siempre según el plan. Vamos a examinar los errores comunes que pueden surgir y cómo se puede controlar a fin de minimizar la necesidad de solicitar el usuario para configurar manualmente su cliente.
  
## <a name="http-status-errors"></a>Errores de estado HTTP
<a name="bk_HttpErrors"> </a>

El primer tipo de error que pueden surgir al enviar solicitudes de detección automática es el estado HTTP. Si el estado HTTP en la respuesta no es 200 (Aceptar), la carga de respuesta no contiene la respuesta de detección automática que estaba buscando. Por motivos de simplicidad, podemos agrupar los códigos de estado no es 200 en tres categorías.
  
**La tabla 1. Códigos de estado HTTP**

|**Código de estado**|**Tipo de error**|**Para controlar...**|
|:-----|:-----|:-----|
|301 o 302  <br/> |Error de redireccionamiento  <br/> |Volver a enviar la solicitud al URI de contenidos en el encabezado de respuesta HTTP "Location". Para obtener información detallada, vea [redirigir de tratamiento de errores](#bk_HandlingRedirects).  <br/> |
|401  <br/> |Error no autorizado  <br/> |Debido a que el [proceso de detección automática](autodiscover-for-exchange.md) implica intentar varias direcciones URL posibles, podría obtener esto en una dirección URL sólo tiene siguiente Aceptar sus credenciales. Por este motivo, no debería tener en cuenta un error 401 único para indicar que las credenciales no son válidas. Sin embargo, si recibe 401 errores de varias direcciones URL, es posible que desee pedir al usuario que vuelva a escribir su contraseña (si es posible).  <br/> |
|Cualquier otro estado no es 200  <br/> |Error de extremo no válido de detección automática  <br/> |Tenga en cuenta la dirección URL que devuelve cualquier otro código de estado no es 200 para que no sea válido y continuar intentando la dirección URL siguiente en la lista.  <br/> |
   
## <a name="autodiscover-errors"></a>Errores de detección automática
<a name="bk_AutodiscoverErrors"> </a>

Incluso si recibe un código de estado 200 (Aceptar) después de enviar una solicitud de detección automática, que no significa que el servidor envía la información que necesita. El estado 200 sólo significa que tiene una respuesta de detección automática, y esa respuesta puede contener un error dentro de la carga. La ubicación de la información de error difiere dependiendo de si el formato es SOAP o POX.
  
### <a name="soap-autodiscover-errors"></a>Errores de detección automática SOAP

Para la detección automática de SOAP, la respuesta puede contener uno o varios elementos [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) , en distintos lugares. Normalmente, puede esperar uno como un elemento secundario del elemento de [Respuesta (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) y otro como elemento secundario de cada elemento [UserResponse (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) en la respuesta. También se puede encontrar uno como un elemento secundario de un elemento [UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) , si hay alguno. El contexto del error depende de dónde **ErrorCode** se encuentra el elemento, como se indica a continuación: 
  
- Como un elemento secundario del elemento de **respuesta** , el elemento **ErrorCode** representa un error que se aplica a toda la petición. 
    
- Como elemento secundario del elemento **UserResponse** , que representa un error que se aplica sólo a ese usuario específico. 
    
- Como elemento secundario de un elemento **UserSettingError** , que representa un error que se aplica a una configuración específica que se solicitó. 
    
Vamos a echar un vistazo a un ejemplo de una respuesta. En este ejemplo, el elemento de **código de error** en el elemento de **respuesta** tiene un valor de "NoError", que indica el éxito general. Sin embargo, el elemento **ErrorCode** bajo el elemento **UserResponse** tiene un valor de "RedirectAddress", que indica que se ha producido un error para ese usuario concreto. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>elvin@mail.contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

El artículo [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) contiene una lista completa de posibles errores. La mayoría de estos indica un error irrecuperable, pero algunos requieran un tratamiento especial. 
  
**Tabla 2. Valores de Autodisover ErrorCode SOAP**

|**Valor de código de error**|**Para controlar...**|
|:-----|:-----|
|RedirectAddress  <br/> |[Reinicio de detección automática con una nueva dirección de correo electrónico](#bk_RestartAutodiscover) con la dirección de correo electrónico en el elemento [RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) .  <br/> |
|RedirectUrl  <br/> |[Volver a enviar la solicitud a una nueva dirección URL](#bk_ResendRequest) a la dirección URL en el elemento **RedirectTarget** .  <br/> |
|ServerBusy  <br/> |Vuelva a intentar esta dirección URL después de un pequeño retraso. Es posible que una cantidad de tiempo de espera o simplemente mover esta dirección URL hasta el final de la lista de direcciones URL para probar. Si recibe este error varias veces desde una dirección URL, debe tener en cuenta la dirección URL no es válido.  <br/> |
   
### <a name="pox-autodiscover-errors"></a>Errores de detección automática POX

El servicio Detección automática POX informes de errores de forma un poco diferente. Errores no recuperables están contenidos en el elemento de [Error (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) . El artículo [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) contiene una lista completa de posibles códigos de error. 
  
Errores de redireccionamiento están contenidos en el elemento de [Acción (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) . Cualquier valor del elemento de **acción** que no sea "configuración" indica un error de redirección. 
  
**Tabla 3. Valores de Autodisover ErrorCode POX**

|**Valor de acción**|**Para controlar...**|
|:-----|:-----|
|redirectAddr  <br/> |[Reinicio de detección automática con una nueva dirección de correo electrónico](#bk_RestartAutodiscover) con la dirección de correo electrónico en el elemento [RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) .  <br/> |
|redirectUrl  <br/> |[Volver a enviar la solicitud a una nueva dirección URL](#bk_ResendRequest) a la dirección URL en el elemento [RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) .  <br/> |
   
En este ejemplo, el elemento de **acción** tiene un valor de "redirectAddr", que indica que se debe enviar una solicitud de nuevo con la nueva dirección de correo electrónico incluida en el elemento **RedirectAddr** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a>Controlar errores de redireccionamiento
<a name="bk_HandlingRedirects"> </a>

Puede controlar los escenarios de error de redireccionamiento de dos maneras:
  
- Reiniciando detección automática con una nueva dirección de correo electrónico.
    
- Reenviando la solicitud a una nueva dirección URL.
    
Ambos escenarios requieren algunos validación antes de continuar.
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a>Reinicio de detección automática con una nueva dirección de correo electrónico
<a name="bk_RestartAutodiscover"> </a>

Al obtener una nueva dirección de correo electrónico en una detección automática redirigir respuesta, comprobar que la nueva dirección de correo electrónico que le ha proporcionado en la respuesta de error de redireccionamiento no es la misma dirección que envía en la solicitud que produjo el error. Si es así, no debe reiniciar la detección automática y en su lugar, tenga en cuenta la dirección URL que generó la respuesta para que no sea válido.
  
Si la nueva dirección de correo electrónico es distinto, descartar la lista existente de posibles direcciones URL de extremo de detección automática y generar una nueva lista en función de la nueva dirección de correo electrónico.
  
### <a name="resending-your-request-to-a-new-url"></a>Volver a enviar la solicitud a una nueva dirección URL
<a name="bk_ResendRequest"> </a>

Cuando se obtiene una nueva dirección URL en una respuesta de redirección de detección automática, primero debe validar la dirección URL como sigue:
  
- Compruebe que la dirección URL es una dirección URL HTTPS.
    
- Compruebe que no ha recibido un error desde esta dirección URL con la dirección de correo electrónico actual antes.
    
- Si es aplicable a su aplicación, que informan al usuario de la redirección y obtener sus permisos para seguir la redirección.
    
- Enviar una solicitud a la dirección URL y [Compruebe que el certificado SSL presentado por el servidor es válido](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).
    
Si la dirección URL pasa la validación, volver a enviar la solicitud a esta nueva dirección URL.
  
## <a name="see-also"></a>Ver también


- [Detección automática de Exchange](autodiscover-for-exchange.md)
    
- [Busque los extremos de detección automática mediante el uso de búsqueda de SCP en Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

