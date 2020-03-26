---
title: Bir izin isteğini iş akışına gönderme
description: Microsoft Dynamics 365 Human Resources'ta, iş akışına bırakma isteği göndermek için MyLeaveRequests Submit () uygulama programlama arabirimini (API) kullanabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7552a4c921dc4a88034b5d2c87d5a9b47d699ae3
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092026"
---
# <a name="submit-a-leave-request-to-workflow"></a>Bir izin isteğini iş akışına gönderme

Microsoft Dynamics 365 Human Resources'ta, iş akışına bırakma isteği göndermek için MyLeaveRequests Submit () uygulama programlama arabirimini (API) kullanabilirsiniz. Bu API, MyLeaveRequests OData varlığı üzerinde bir eylem olarak sunulur.

## <a name="prerequisites"></a>Önkoşullar

İzin isteği veritabanına kaydedilmelidir ve MyLeaveRequests varlığı aracılığıyla alınabilir olmalıdır.

## <a name="permissions"></a>İzinler

Bu API 'YI çağırmak için aşağıdaki izinlerden biri gerekiyor. İzinler ve bunların seçilmesi hakkında daha fazla bilgi için, bkz [Kimlik doğrulama](hr-developer-api-authentication.md).

| İzin türü                    | İzinler (en az ayrıcalıklı-büyük ayrıcalıklı) |
|------------------------------------|--------------------------------------------------------|
| Yetkilendirilen (İş veya okul hesabı) | Kullanıcı\_kimliğine bürünme                                    |

## <a name="https-request"></a>HTTPS isteği

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

İstek OData standartlarına uygun. {requestId}, {leaveType}, {leaveDate} ve {dataArea} parametreleri, MyLeaveRequests varlığı için bileşik doğal anahtarı oluşturan alanlara başvuruda bulunuyor.

> [!NOTE]
> MyLeaveRequests varlığının alanları izin talebindeki tek bir satıra başvuruda bulunduğu sürece, API gönder çağrısı, tüm izin vermez isteği (tüm satırlar) iş akışına gönderir.

### <a name="request-headers"></a>İstek başlıkları

| Başlık         | Value                     |
|----------------|---------------------------|
| Yetkilendirme  | Taşıyıcı {token} (gerekli) |
| İçerik Türü   | Uygulama/json          |

### <a name="request-body"></a>İstek gövdesi

Bu yöntem için bir istek gövdesi sağlamamalısınız.

### <a name="response"></a>Yanıt

Başarılı bir yanıt, her zaman **204 içerik yok** yanıtıdır.

Yetkisiz arayıcılar **401 izinsiz** veya **403 Yasak** yanıt alır.

Gönderme işlemi başarısız olursa (örneğin, doğrulama nedeniyle), yanıt bir **500 sunucu hatası** olur ve yanıt gövdesinde daha ayrıntılı bir JSON nesnesi bulunur.

## <a name="example"></a>Örnek

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a>Doğrulama ve hata iletileri

Gönderme API'sine yapılan çağrının bir parçası olarak İnsan Kaynakları gönderme işleminden önce iş mantığı doğrulaması yapar ve bu da bırakma isteğinin gönderme için geçerli bir durumda olmasını sağlar. Doğrulama başarısız olursa yanıt olarak alabileceğiniz olası hata iletileri şunlardır:

 - Talep '{LeaveTypeId}' bakiyesini {date} tarihinde izin verilen minimum bakiyenin altına indirecek.
 - Tamamlandı durumundaki istek süresi gönderilemez.
 - Hiçbir değişiklik yapılmadı olarak istek gönderilemiyor veya kaydedilemiyor. Tutarı veya izin tipini ekleyin veya güncelleştirin ve yeniden deneyin.
 - Girilen zaman isteği, aynı tarihle aynı tarihe sahip bir veya daha fazla gün içeriyor ve mevcut bekleyen istek olarak bu türü bırak. Lütfen değişiklik yapmak için varolan isteği geri çekin.
 - '{ReasonCodeId}' neden kodu istekteki izin türlerinin hiçbiri için geçerli değildir.
 - '{LeaveTypeId}' Çıkış türü neden kodu gerektiriyor. Uygun türü ve neden kodunu seçin.
 - Kapatma saati başarıyla gönderilmedi. Kapatma zamanı taslak istek olarak kaydedildi.

## <a name="see-also"></a>Ayrıca bkz.

- [MyLeaveRequests genel bakış](hr-developer-api-myleaverequests-overview.md)
- [Kimlik doğrulama](hr-developer-api-authentication.md)