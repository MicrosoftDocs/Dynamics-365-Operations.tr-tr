---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (26 Mart 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 568a16a17ed3269c7b72f27f0d4b7bbdbd56630e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519335"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-26-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (26 Mart 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="enhancements-to-interview-scheduling"></a>Mülakat zamanlamadaki geliştirmeler
Aşağıdaki geliştirmeler mülakat zamanlamada kullanılabilir.

- İşe alımcılar veya işe alma müdürleri artık bir mülakatçı için geri bildirimlerini göndermeleri üzerine bir hatırlatmayı el ile tetikleyebilirler. Anımsatma için ilişkili e-posta şablonu da yapılandırılabilir.
- Görüşme özetini aday ile paylaşırken, mülakat zamanlayıcı, mülakatı yapanların adını gizlemeyi seçebilir ve mülakat özet görünümünden sütunları saklamayı seçebilir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

### <a name="embedded-images-in-activities"></a>Etkinliklerde katıştırılmış resimler
Artık resimleri doğrudan etkinliklere katıştırabilirsiniz. Web'den resimleri kopyalayıp yapıştırabilmenin yanı sıra, yerel dosya sisteminizden de resimleri karşıya yükleyebilirsiniz. Etkinliğin boyutu 1 MB ile sınırlıdır. Resim çok büyükse, yeniden boyutlandırın ve tekrar karşıya yüklemeyi deneyin.

[![Eşleştirme](./media/embedimages.png)](./media/embedimages.png)

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içerir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler
**Derleme 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Özel alan desteği, Common Data Service içindeki seçili varlıklarda kullanılabilir 

Aşağıdaki Common Data Service varlıkları artık Dynamics 365 for Talent içinde oluşturulan özel alanları desteklemektedir:

- Çalışan
- Etnik köken
- Gazilik durumu
- Dil kodu
- Görev
- İş türü
- İş işlevi
- Bölme
- Pozisyon türü
 
### <a name="employment-history-not-displayed-chronologically"></a>Çalışma geçmişi kronolojik olarak görüntülenmez
Bu değişiklik ile, çalışan geçmişi sayfası artık çalışma kayıtlarını kronolojik olarak görüntüler, şirketten bağımsız olarak. Şirket bazında sıralama yapmak için sıralama seçeneklerini de kullanabilirsiniz.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Sabit ücret planları, kullanıcıyı güvenlik içinde şirket bazında sınırlarken görüntülenmez.
Bu sürümde, sabit ücret planları artık kullanıcıları güvenlik içinde şirket bazın sınırlarken görüntülenir. Tüm güvenlik ayarları dikkate alınacaktır ve sabit planlar, kullanıcının erişime izni olduğu şirketler için görüntülenecektir. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Talent içinde Excel içinde Aç seçeneğini kullanarak İş kayıtları silinemiyor
Bu sürüm ile birlikte, **Excel içinde aç** seçeneğini Dynamics 365 for Talent içinde kullanarak iş kayıtlarını artık silebilirsiniz.

### <a name="upgrade-to-common-data-service"></a>Common Data Service'a yükseltin
Common Data Service'e yükseltme için son tarihler hızla yaklaşmaktadır. PowerApps Yönetim Merkezine oturum açarak veritabanınızın yükseltilmeye ihtiyacı olup olmadığını görün. Son tarihler ve yükseltme için gerekli adımlar hakkında daha fazla bilgi için bkz. [Common Data Service'e yükseltme](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Ön izlemede

Önizleme özelliklerini etkinleştirmek hakkında daha fazla bilgi için bkz. [Talent içinde önizleme özelliklerine erişim](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Sebep kodlarının izin türlerinde belirtilmesine izin ver
Kuruluşların izin istekleriyle ilgili ek bilgilere ihtiyacı olabilir. Bu bilgiyi eklemek için çalışanların bir sebep kodunu izin taleplerine eklemeleri gerekir. Bu sürüm ile, belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Sebep kodlarının çeşitli izin türleri için talep gönderildiğinde gerektirilmesini yapılandır
Kuruluşlar, bir çalışan izin talebi gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir. Bu, ülke/bölge veya şirket ilkelerindeki bir düzenleyici gereksinime dayanıyor olabilir. Bu sürüm, IK için hangi izin türlerinin bir sebep kodu gerektirdiğini belirleme olanağı sağlar. Bu, çalışanlar izin almanın bir sebep kodu gerektirdiği izin talepleri gönderdiklerinde uygulanacaktır.

## <a name="coming-soon"></a>Çok yakında

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Gelişmiş ücret güvenliği (sabit ve değişken)
Pek çok kuruluşta, ücret ve kazanç yöneticilerinin yalnızca belirli ücret kayıtlarına erişimi olabilir. Bunlar yöneticiler veya bölgesel çalışanlar için olabilir. Bu değişiklik ile IK, yönetimini değiştirebilir ve ücret planlarını kuruluş içindeki farklı personel grupları için korur. Planlar ve planlarla ilişkili personel verilerine, örneğin maaş veya ikramiye kayıtlarına erişimi belirleyen sabit ve değişken planlara güvenlik rolleri atayabilirsiniz. Yalnızca erişime sahip roller bu çalışanlar için işlem ücretine erişebilir.

###  <a name="email-support-for-alerts"></a>Uyarılar için e-posta desteği
Platform güncelleştirmesi 25 ile kullanıcılar otomatik olarak, bir etkinlik tarafından tetiklendiğinde e-posta bildirimlerini ilgili kişilere gönderen uyarı kuralları oluşturabilirler. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Yinelenen personel çekleri: Kullanıcı arabirimi değişiklikleri
Bu değişiklikle, isim alanlarını girdiğinizde yinelenenler tespit edilir ve yinelenenlerin sayısını görüntüleyen bir durum gösterilir. Sağlanan bağlantıyı tespit edilen eşleşmeyi kullanıp kullanmamak üzere yeni bir sayfa açmak için seçebilirsiniz. Veri girişinin kesilmesini engellemek için yinelenenler formu otomatik olarak açılmaz.
