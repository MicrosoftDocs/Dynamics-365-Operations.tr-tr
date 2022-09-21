---
title: Çalışan üst bilgisi denetimi
description: Bu makalede, Employee Self-Service, People hub'ı ve Microsoft Dynamics 365 Human Resources'taki Çalışan sayfasındaki kişiselleştirilebilir üst bilgi denetimi hakkında bilgi sağlanmaktadır.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445957"
---
# <a name="worker-header-control"></a>Çalışan üst bilgisi denetimi

Microsoft Dynamics 365 Human Resources, **Employee Self-Service**'te, **People** hub'ında ve iyileştirilmiş **Çalışan** sayfasında kişiselleştirilebilir bir üst bilgi denetimi sağlar. Üst bilgi, çalışan hakkında önemli bilgiler ve ayrıca e-posta, arama veya mesajlaşma gibi tek tıklamayla gerçekleştirilecek eylemler içerir. Üst bilgi, alanları kaldırarak veya ek bilgiler göstermek için özel alanlar da dahil olmak üzere alanlar ekleyerek değiştirilebilir. Yeni üst bilgi denetimini kullanmak için **Özellik yönetimi**'ne gidin ve **Çalışan üst bilgi denetimi** özelliğini etkinleştirin.

## <a name="personalization"></a>Kişiselleştirme

Çalışan üst bilgi denetiminin en önemli yararlarından biri, üst bilgide görünen bilgileri kişiselleştirme yeteneğidir.

Üst bilginin sağ üst köşesinde, çalışanın durumuna bağlı olarak farklı veriler gösteren üç alandan oluşan bir grup bulunur. Bu alan grubu, üst bilginin Spotlight bölümü olarak adlandırılır. Geçerli alanları kaldırarak veya alanlar ekleyerek üst bilginin Spotlight bölümünü kişiselleştirebilirsiniz. Üst bilgi denetimindeki Spotlight bölümüne eklenebilecek alanlar **Employee Self-Service**, **People** hub'ı ve **Çalışan** sayfası için farklılık gösterir.

## <a name="employee-self-service"></a>Personel self servisi

**Employee Self-Service** sayfasındaki çalışan üst bilgisi aşağıdaki bilgileri içerir:

- Çalışan adı
- Personel numarası
- Pozisyon unvanı
- Departmanlar
- Çalışan türü
- İşe alan tüzel kişilik
- Hizmet yılları
- Üstü (yönetici)
- Pozisyon türü

Üst bilgi, kişinin kişisel bilgilerini düzenlemek için tek tıklamayla gerçekleştirilen bir eylem de içerir. **Employee Self-Service**'teki **Kişisel bilgiler** sayfasını açmak için **Kişisel ayrıntıları düzenle**'yi seçin.

## <a name="people-hub"></a>Kişi hub'ı

**People** hub'ındaki (**People workspace** sayfası) çalışan üst bilgisi aşağıdaki bilgileri içerir:

- Çalışan adı
- Personel numarası
- Pozisyon unvanı
- Departmanlar
- Çalışan türü
- İşe alan tüzel kişilik
- Hizmet yılları
- Üstü (yönetici)
- Pozisyon türü

Üst bilgi ayrıca e-posta, arama veya mesajlaşma gibi tek tıklamayla gerçekleştirilen eylemler de içerir. Bir kullanıcı **People workspace** sayfasında kendi bilgilerini görüntülüyorsa tek tıklamayla gerçekleştirilen eylem bölümünde **Kişisel ayrıntıları düzenle** düğmesi bulunur. Kullanıcı, **Employee Self-Service**'te **Kişisel bilgiler** sayfasını açmak için bu düğmeyi seçebilir.

## <a name="streamlined-worker-page"></a>Geliştirilmiş Çalışan sayfası

Geliştirilmiş **Çalışan** sayfasındaki çalışan üst bilgisi aşağıdaki bilgileri içerir:

- Çalışan adı
- Personel numarası
- Pozisyon unvanı
- Departmanlar
- Çalışan türü
- İşe alan tüzel kişilik

Çalışanın durumuna bağlı olarak, üst bilgideki veriler değişebilir. Örneğin, çalışan şirketten çıktıysa üst bilgi denetimi bir **İşten Çıktı** rozeti, istihdam bitiş tarihi ve fesih nedeni içerir.

Aşağıdaki tabloda, farklı çalışan durumları için üst bilgide görünen veriler gösterilmektedir.

| Personel durumu | Gösterilen veriler | Dekont |
|-----------------|--------------------|------|
| Beklemede | <ul><li>Adı</li><li>Personel numarası</li><li>Pozisyon unvanı</li><li>Departman</li><li>Çalışan türü</li><li>Tüzel kişilik</li><li>Beklemede rozeti</li><li>Başlangıç tarihi</li><li>Bağlı olduğu kişi</li><li>Pozisyon türü</li></ul> | |
| En son işe alma | <ul><li>Adı</li><li>Personel numarası</li><li>Pozisyon unvanı</li><li>Departman</li><li>Çalışan türü</li><li>Tüzel kişilik</li><li>Son işe alınan rozeti</li><li>Hizmet yılları</li><li>Bağlı olduğu kişi</li><li>Pozisyon türü</li></ul> | Varsayılan olarak, **Son işe alınan** rozeti, son yedi gün içinde işe alınan çalışanlar için gösterilir. Bu ayarı değiştirmek için **İnsan kaynakları parametreleri** sayfasında, **Genel** sekmesinde **En son işe alımlar tarih aralığı** bölümü için bir zaman dilimi belirleyin. Örneğin, son 14 günde işe alınan çalışanların **Son işe alma** rozetini görüntülemek için **Dönem** alanını **14** olarak ve **Birim** alanını **Gün** olarak ayarlayın. |
| Etkin çalışan | <ul><li>Adı</li><li>Personel numarası</li><li>Pozisyon unvanı</li><li>Departman</li><li>Çalışan türü</li><li>Tüzel kişilik</li><li>Başlangıç tarihi</li><li>Bağlı olduğu kişi</li><li>Pozisyon türü</li></ul> | |
| Çıkış | <ul><li>Adı</li><li>Personel numarası</li><li>Pozisyon unvanı</li><li>Departman</li><li>Çalışan türü</li><li>Tüzel kişilik</li><li>Ayrılacak rozeti</li><li>Hizmet yılları</li><li>Bağlı olduğu kişi</li><li>Pozisyon türü</li></ul> | Varsayılan olarak, **Ayrılacak** rozeti önümüzdeki yedi gün içinde işten ayrılacak çalışanlar için gösterilir. Bu ayarı değiştirmek için **İnsan kaynakları parametreleri** sayfasında, **Genel** sekmesinde **Çıkış yapan çalışan tarih aralığı** için bir zaman dilimi belirleyin. Örneğin, önümüzdeki 14 günde işten çıkacak çalışanların **İşten çıkacak** rozetini görüntülemek için **Dönem** alanını **14** olarak ve **Birim** alanını **Gün** olarak ayarlayın. |
| Çıktı | <ul><li>İşten Ayrıldı rozeti</li><li>Personel numarası</li><li>İş bitiş tarihi</li><li>Neden kodu</li></ul> | Varsayılan olarak, **İşten Ayrıldı** rozeti son yedi gün içinde işten ayrılan çalışanlar için gösterilir. Bu ayarı değiştirmek için **İnsan kaynakları parametreleri** sayfasında, **Genel** sekmesinde **İşten çıkan çalışanlar tarih aralığı** için bir zaman dilimi belirleyin. Örneğin, son 14 günde işten çıkan çalışanların **İşten çıktı** rozetini görüntülemek için **Dönem** alanını **14** olarak ve **Birim** alanını **Gün** olarak ayarlayın. |
