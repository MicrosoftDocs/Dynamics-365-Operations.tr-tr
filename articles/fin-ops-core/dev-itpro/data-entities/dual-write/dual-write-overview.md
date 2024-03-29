---
title: Çift yazmaya genel bakış
description: Bu makalede, müşteri etkileşimi uygulamaları ile finans ve operasyon uygulamaları arasında gerçek zamanlıya yakın etkileşim sağlayan çift yazma özelliğine dair genel bir bakış sunulmaktadır.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 943607a3ef28db11b7bc7805257914117e6ae38c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289653"
---
# <a name="dual-write-overview"></a>Çift yazmaya genel bakış

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Çift yazma nedşr?

Çift yazma, Customer Engagement uygulamaları ile finans ve operasyon uygulamaları arasında gerçek zamanlıya yakın etkileşim sağlayan hazır bir altyapıdır. Müşteriler, ürünler, kişiler ve işlemlerle ilgili veriler, uygulama sınırlarının ötesinde akar, bir kuruluştaki tüm bölümler korunur.

Çift yazma, finans ve operasyon uygulamaları ve Dataverse arasında sıkı şekilde bağlanmış, çift yönlü tümleştirme sağlar. Finans ve operasyon uygulamalarındaki tüm veri değişiklikleri Dataverse'e yazmaya neden olur ve Dataverse'teki tüm veri değişiklikleri finans ve operasyon uygulamalara yazmaya neden olur. Bu otomatik veri akışı, uygulamalar arasında tümleşik bir kullanıcı deneyimi sağlar.

![Uygulamalar arasında veri ilişkisi.](media/dual-write-overview.jpg)

Çift yazıış iki yönden sahiptir : *altyapı* yönü ve *uygulama* en yönü.

### <a name="infrastructure"></a>Altyapı

Çift-yazılır altyapı genişletilebilir ve güvenilirdir ve aşağıdaki önemli özellikleri içerir:

+ Uygulamalar arasında eşzamanlı ve çift yönlü veri akışı
+ Çevrimiçi ve çevrimdışı/zaman uyumsuz modlar sistemi destekleyecek şekilde yürütme, duraklatma ve yakalama modlarıyla birlikte eşitleme.
+ Uygulamalar arasında ilk verileri eşitleme yeteneği
+ Veri yöneticileri için etkinliğin birleşmiş görünümü ve hata günlükleri
+ Özel uyarıları ve eşikleri konfigüre etme ve bildirimlere abone olma yeteneği
+ Filtreleme ve dönüşümler için sezgisel kullanıcı arabirimi (UI)
+ Tablo bağımlılıklarını ve ilişkilerini ayarlama ve görüntüleme yeteneği
+ Standart ve özel tablolar ve haritalar için genişletilebilirlik
+ Güvenilir uygulama yaşam döngüsü yönetimi
+ Yeni müşteriler için kutulu kurulum deneyimi

### <a name="application"></a>Uygulama

Çift yazma, finans ve operasyon uygulamalarında bulunan kavramlar ile müşteri etkileşimi uygulamalarındaki kavramlar arasında bir eşleme oluşturur. Bu tümleştirme aşağıdaki senaryoları destekler:

+ Tümleşik müşteri aslı
+ Müşteri bağlılık programı kartlarına ve ödül noktalarına erişim
+ Birleşik ürün uzmanlaşma deneyimi
+ Organizasyon hiyerarşisi farkındalığı
+ Tümleşik satıcı aslı
+ Finans ve vergi referans verilerine erişim
+ İsteğe bağlı fiyat altyapısı deneyimi
+ Tümleşik aday müşteri-nakit deneyimi
+ Alan aracıları aracılığıyla hem şirket içi kıymetler hem de müşteri varlıklarını kullanabilme olanağı
+ Entegre temin-ödeme deneyimi
+ Müşteri verileri ve belgeleri ile ilgili tümleşik etkinlikler ve notlar
+ Eldeki stok kullanılabilirliğini ve ayrıntılarını arama yeteneği
+ Proje-nakit deneyimi
+ Parti kavramıyla birden çok adres ve rolü işleyebilme yeteneği


## <a name="top-reasons-to-use-dual-write"></a>Çift-yazma kullanmanın başlıca nedenleri

Çift-yazılır, Microsoft Dynamics 365 uygulama arasında veri tümleştirmesi sağlar. Bu güçlü çerçeve, ortamları birbirine bağlar ve farklı iş uygulamalarının birlikte çalışmasını sağlar. Çift-yazmayı kullanmanız gereken başlıca nedenler şunlardır:

+ Çift yazma, finans ve operasyon uygulamaları ile müşteri etkileşimi uygulamaları arasında sıkı bir şekilde birleştirilmiş, neredeyse gerçek zamanlı ve çift yönlü tümleştirme sunar. Bu bütünleşme, Microsoft Dynamics 365 tüm iş çözümleri için tek durduran mağaza yapar. Müşteri ilişkileri yönetimi (CRM) için Microsoft dışı çözümler kullanan ancak Dynamics 365 Finance ve Dynamics 365 Supply Chain Management kullanan müşteriler çift yazma desteği için Dynamics 365'e geçiş yapmaktadır.
+ Müşteriler, ürünler, operasyonlar, projeler ve bunların Internet bilgileri (IoT), otomatik olarak çift-yazılabilir olarak Dataverse'e akar. Bu bağlantı, Power Platform uzantıları ile ilgilenen işletmeler için yararlıdır.
+ Çift-yazılır altyapı, No-Code/Low-Code ilkesini izler. Standart tablo-tablo eşlemelerini genişletmek ve özel eşlemeler eklemek için minimal mühendislik çaba gereklidir.
+ Çift yazım, hem çevrimiçi modu, hem de çevrimdışı modu destekler. Microsoft, çevrimiçi ve çevrimdışı modlar için destek sunan tek şirkettir.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Müşteri etkileşimi uygulamalarının geliştiricileri ve mimarları için çift yazma ortalaması nedir?

Çift yazma finans ve operasyon uygulamaları ve müşteri etkileşimi uygulamaları arasında veri akışını otomatikleştirir. Çift yazma, Dataverse üzerine yüklenen iki AppSource çözümünden oluşur. Çözümler, ERP boyutuna ölçeklendirilebilecek şekilde, Dataverse üzerindeki tablo şemasını, eklentileri ve iş akışlarını genişletir. Başarılı bir uygulama için, müşteri etkileşimi uygulamalarının geliştiricileri ve mimarları bu değişiklikleri anlayıp finans ve operasyon uygulamalarındaki meslektaşlarıyla birlikte çalışmalıdır.

Finans ve operasyon uygulamalarla eşitlik oluşturmak için çift yazma, Dataverse şemasında bazı önemli değişiklikler yapar. Planı anladığınızda, gelecekte tasarım ve geliştirme üzerinde yeniden çalışma yapmaktan kaçınabilirsiniz.

+ Çift yazma AppSource paketi yüklendiğinde, Dataverse uygulamasında şirket ve taraf gibi yeni kavramlar bulunacaktır. Bu kavramlar, Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ve Dynamics 365 Field Service uygulamalarının dahil olduğu Dataverse üzerine inşa edilen uygulamaların sorunsuz bir şekilde finans ve operasyon uygulamaları ile etkileşimde bulunmasına yardımcı olur.

+ Aktiviteler ve notlar, C1S (sistemin kullanıcılarını) ve C2s (sistemin müşterileri) desteklenmesi için birleştirilmiş ve genişletilmiştir.

+ Finans ve operasyon uygulamaları ile Dataverse arasında yapılan para birimi iletimi sırasında veri kaybını önlemek için, müşteri etkileşimi uygulamalarının para birimi veri türünde ondalık basamak sayısını genişletebilirsiniz. Özellik, var olan satırları meta veri katmanındaki yeni genişletilmiş duruma otomatik olarak çevirir. Bu işlem sırasında para birimi değeri para verileri yerine ondalık verilere çevrilir ve para birimi değeri 10 basamaklı ondalık değeri destekler. Bu özellik tercihe bağlıdır ve 4 basamaktan fazla ondalık değere ihtiyaç duymayan kuruluşların tercih etmesine gerek yoktur. Daha fazla bilgi için bkz. [Çift yazma için para birimi veri türü taşıma](currrency-decimal-places.md).

+ [Tarih etkililiği](../../dev-tools/date-effectivity.md) Dataverse uygulamasına eklenecektir. Aynı tablo üzerinde geçmiş, şimdiki ve gelecekteki verileri destekleyecektir.

+ Ürün [birimi dönüştürmeleri](../../../../supply-chain/pim/tasks/manage-unit-measure.md) ürünler, teklifler, siparişler ve faturalar için desteklenir.

Gelecekteki değişiklikler hakkında daha fazla bilgi için bkz. [Çift yazmadaki yenilikler veya değişiklikler](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

