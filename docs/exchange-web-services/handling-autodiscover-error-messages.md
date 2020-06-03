---
title: Administrar los mensajes de error de detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: Obtenga información sobre los distintos tipos de errores de detección automática y qué hacer con ellos.
localization_priority: Priority
ms.openlocfilehash: 0cba7e54cb251a9775e0971826560e277dcd9d2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455964"
---
# <a name="handling-autodiscover-error-messages"></a>Administrar los mensajes de error de detección automática

Obtenga información sobre los distintos tipos de errores de detección automática y qué hacer con ellos.
  
La detección automática permite que las aplicaciones recuperen automáticamente la información de configuración y funciona bien. Sin embargo, las cosas no siempre van según el plan. Veamos los errores comunes que pueden producirse y cómo puede controlarlos para minimizar la necesidad de solicitar al usuario que configure el cliente de forma manual.
  
## <a name="http-status-errors"></a>Errores de Estado HTTP
<a name="bk_HttpErrors"> </a>

El primer tipo de error que puede encontrarse al enviar solicitudes de detección automática es el estado de HTTP. Si el Estado HTTP de la respuesta es distinto de 200 (correcto), la carga de respuesta no contiene la respuesta de detección automática que estaba buscando. Para simplificar, podemos agrupar los códigos de estado que no sean 200 en tres categorías.
  
**Tabla 1. Códigos de Estado HTTP**

|**Código de estado**|**Tipo de error**|**Para controlar...**|
|:-----|:-----|:-----|
|301 o 302  <br/> |Error de redirección  <br/> |Vuelva a enviar la solicitud al URI contenido en el encabezado de respuesta HTTP "Location". Para obtener más información, consulte [Handling Redirect Errors](#bk_HandlingRedirects).  <br/> |
|401  <br/> |Error no autorizado  <br/> |Dado que el [proceso de detección automática](autodiscover-for-exchange.md) implica probar varias direcciones URL potenciales, puede obtener esto en una dirección URL solo para que la siguiente acepte sus credenciales. Por este motivo, no debe tener en cuenta un solo error 401 para indicar que las credenciales no son válidas. Sin embargo, si recibe errores de 401 de varias direcciones URL, es posible que quiera pedir al usuario que vuelva a escribir su contraseña (si es posible).  <br/> |
|Cualquier otro Estado que no sea 200  <br/> |Error de punto de conexión de detección automática no válido  <br/> |Considere la dirección URL que devuelve cualquier otro código de estado que no sea 200 no es válido y continúe intentándolo con la siguiente dirección URL de la lista.  <br/> |
   
## <a name="autodiscover-errors"></a>Errores de detección automática
<a name="bk_AutodiscoverErrors"> </a>

Incluso si obtiene un código de estado 200 (correcto) después de enviar una solicitud de detección automática, eso no significa que el servidor haya enviado la información que necesita. El estado 200 solo significa que tiene una respuesta de detección automática y que la respuesta puede contener un error dentro de la carga. La ubicación de la información de error varía en función de si el formato es SOAP o POX.
  
### <a name="soap-autodiscover-errors"></a>Errores de detección automática de SOAP

Para la detección automática de SOAP, la respuesta puede contener uno o más elementos [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) , en lugares diferentes. Normalmente, se puede esperar que haya un elemento secundario del elemento [Response (SOAP)](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) y otro como elemento secundario de cada elemento [UserResponse (SOAP)](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) en la respuesta. También es posible que encuentre uno como elemento secundario de un elemento [UserSettingError (SOAP)](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) , si hay alguno presente. El contexto del error depende de dónde se encuentre el elemento **ErrorCode** , como se indica a continuación: 
  
- Como elemento secundario del elemento **Response** , el elemento **ErrorCode** representa un error que se aplica a toda la solicitud. 
    
- Como elemento secundario del elemento **UserResponse** , representa un error que se aplica solo a ese usuario específico. 
    
- Como elemento secundario de un elemento **UserSettingError** , representa un error que se aplica a una configuración específica que se solicitó. 
    
Echemos un vistazo a un ejemplo de respuesta. En este ejemplo, el elemento **ErrorCode** del elemento **Response** tiene un valor de "NoError", que indica el éxito general. Sin embargo, el elemento **ErrorCode** del elemento **UserResponse** tiene un valor de "RedirectAddress", que indica que se ha producido un error para ese usuario en particular. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

El artículo [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) contiene una lista completa de los posibles errores. La mayoría de estos errores indican un error irrecuperable, pero algunos de ellos justifican un tratamiento especial. 
  
**Tabla 2. Valores del ErrorCode de Autodisover SOAP**

|**Valor ErrorCode**|**Para controlar...**|
|:-----|:-----|
|RedirectAddress  <br/> |[Reiniciar la detección automática con una dirección de correo electrónico nueva](#bk_RestartAutodiscover) con la dirección de correo electrónico en el elemento [RedirectTarget (SOAP)](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) .  <br/> |
|RedirectUrl  <br/> |[Reenviar la solicitud a una nueva dirección URL](#bk_ResendRequest) en la dirección URL del elemento **RedirectTarget** .  <br/> |
|ServerBusy  <br/> |Vuelva a intentar esta dirección URL tras un pequeño retraso. Puede esperar un período de tiempo determinado o simplemente mover esta dirección URL al final de la lista de direcciones URL para probar. Si recibe este error varias veces desde una dirección URL, debe tener en cuenta que la dirección URL no es válida.  <br/> |
   
### <a name="pox-autodiscover-errors"></a>Errores de detección automática de POX

El servicio Detección automática de POX informa de los errores de una forma ligeramente distinta. Los errores no recuperables se encuentran en el elemento [error (POX)](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) . El artículo código de error [(POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) contiene una lista completa de los códigos de error posibles. 
  
Los errores de redirección se incluyen en el elemento [Action (POX)](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) . Cualquier valor del elemento **Action** distinto de "Settings" indica un error de redirección. 
  
**Tabla 3. Valores del ErrorCode Autodisover de POX**

|**Valor de la acción**|**Para controlar...**|
|:-----|:-----|
|redirectAddr  <br/> |[Reiniciando detección automática con una dirección de correo electrónico nueva](#bk_RestartAutodiscover) con la dirección de correo electrónico en el elemento [RedirectAddr (POX)](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) .  <br/> |
|redirectUrl  <br/> |[Reenviar la solicitud a una nueva dirección URL](#bk_ResendRequest) a la dirección URL en el elemento [RedirectURL (POX)](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) .  <br/> |
   
En este ejemplo, el elemento **Action** tiene un valor de "redirectAddr", que indica que se debe enviar una nueva solicitud con la nueva dirección de correo electrónico contenida en el elemento **redirectAddr** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a>Control de errores de redirección
<a name="bk_HandlingRedirects"> </a>

Puede controlar los escenarios de error de redirección de dos maneras:
  
- Reiniciando la detección automática con una nueva dirección de correo electrónico.
    
- Reenviando la solicitud a una nueva dirección URL.
    
Ambos escenarios requieren una validación antes de continuar.
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a>Reinicio de detección automática con una nueva dirección de correo electrónico
<a name="bk_RestartAutodiscover"> </a>

Cuando obtenga una nueva dirección de correo electrónico en una respuesta de redireccionamiento de detección automática, compruebe primero que la nueva dirección de correo electrónico que se proporcionó en la respuesta de error de redireccionamiento no es la misma dirección que envió en la solicitud que resultó en el error. Si es así, no debe reiniciar la detección automática y considere, en su lugar, que la dirección URL que generó la respuesta no sea válida.
  
Si la nueva dirección de correo electrónico es diferente, descarte la lista existente de direcciones URL potenciales del punto de conexión de detección automática y genere una nueva lista basada en la nueva dirección de correo electrónico.
  
### <a name="resending-your-request-to-a-new-url"></a>Reenviar la solicitud a una nueva dirección URL
<a name="bk_ResendRequest"> </a>

Cuando obtenga una nueva dirección URL en una respuesta de redireccionamiento de detección automática, primero debe validar la dirección URL de la siguiente manera:
  
- Compruebe que la dirección URL es una dirección URL HTTPS.
    
- Compruebe que no ha recibido un error de esta dirección URL con la dirección de correo electrónico actual anterior.
    
- Si es aplicable a la aplicación, informe al usuario de la redirección y obtenga su permiso para seguir el redireccionamiento.
    
- Envíe una solicitud a la dirección URL y [Compruebe que el certificado SSL presentado por el servidor es válido](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).
    
Si la dirección URL pasa la validación, vuelva a enviar la solicitud a esta nueva dirección URL.
  
## <a name="see-also"></a>Vea también


- [Detección automática en Exchange](autodiscover-for-exchange.md)
    
- [Buscar Autodisover extremos mediante el uso de búsqueda de SCP en Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [ErrorCode (POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

