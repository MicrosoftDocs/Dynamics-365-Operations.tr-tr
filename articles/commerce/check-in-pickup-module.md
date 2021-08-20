---
title: Malzeme çekme modülü için giriş yapma
description: Bu konu malzeme çekme modülü için giriş yapmayı ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f6359f41f3b97325db4fda083dc32d39839811297a96a1f2d99a93990c00afae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747477"
---
# <a name="check-in-for-pickup-module"></a>Malzeme çekme modülü için giriş yapma

[!include [banner](includes/banner.md)]

Bu konu malzeme çekme modülü için giriş yapmayı ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.

Malzeme çekme modülü için giriş yapma, Dynamics 365 Commerce müşteri giriş özelliğini kullanan müşterilerin geldiğini mağazaya bildirmek için bir onay sayfası sağlar. Malzeme çekme modülü için giriş yapma aynı zamanda teslimatı kolaylaştırmak amacıyla müşterilerden ek bilgiler toplayan bir form yapılandırmanıza da olanak tanır. Bu bilgilere müşterinin park yeri numarası ve müşterinin aracının marka ve modeli dahildir. 

## <a name="module-properties"></a>Modül özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Onay metni | Metin dizesi | Giriş onayı sayfasında görünen başlığın içeriği. |
| QR kodunu göster | **Doğru** veya **yanlış** | Bu özellik, **Doğru** olarak ayarlandığında, giriş onayı sayfası sipariş onay kodunu temsil eden bir QR kodu gösterir. |
| Ek bilgi başlığı | Metin dizesi | Ek bilgi alanları yapılandırıldığında görüntülenen başlık içeriği. |
| Ek bilgi anahtarları | Kaynak kodu/kaynak değer çifti | Her bir anahtar, müşterilerden ek bilgi toplamak için kullanılan bir form alanı ve ilişkili bir etiket oluşturur. |
| Ek bilgi anahtarları \> Kaynak kodu | Metin dizesi | Her bir bilgi, müşterilerden ek bilgi toplamak için kullanılan bir form alanı ve ilişkili bir etiket oluşturur. Bu özellik, ek bilgi anahtarını tanımlar. Satış noktasında (POS) oluşturulan görevde, bu özelliğin değeri, talimatlar alanında etiket olarak gösterilir. |
| Ek bilgi anahtarları \> Kaynak değeri | Metin dizesi | POS'taki görevde yer alan metin alanı etiketi. |
| Ek bilgi anahtarları \> Zorunlu | **Doğru** veya **yanlış** | Bu özellik, müşterilerin devam edebilmek için form alanını doldurmaları gerektiğini belirtir. Bu özellik **Doğru** olarak ayarlandığında, form etiketinin yanında bir yıldız görüntülenir ve herhangi bir değer girilmediğinde müşterilerin devam etmesini önlemek için null denetimi yapılır. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Bir sayfaya malzeme çekme modülü için giriş yapmayı ekleme

Giriş onayı için oluşturduğunuz yeni sayfaya, malzeme çekme modülü için giriş yapma eklenmelidir. Bu sayfa, e-postadaki **Buradayım** bağlantısını veya düğmesini seçen müşteriler için giriş onayı deneyimi görevini üstlenecek. 

## <a name="configure-the-additional-information-form"></a>Ek bilgiler formunu yapılandırma

Ek bilgi anahtarları yapılandırılmamışsa modül, müşteriye varsayılan olarak giriş onayı sayfasını gösterir. Giriş onayı gösterildiğinde, POS'ta siparişin çekildiği mağaza için bir görev oluşturulur.

Bir veya daha fazla ek bilgi anahtarı yapılandırıldığında önce müşterilerden bilgi girmeleri istenir. **Gönder**'i seçtiklerinde, giriş onayı görüntülenir ve POS'ta bir görev oluşturulur. 

## <a name="additional-resources"></a>Ek kaynaklar

[Satış noktasında (POS) müşteri giriş bildirimlerini etkinleştirme](enable-customer-check-in.md)
