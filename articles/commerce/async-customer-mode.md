---
title: Zaman uyumsuz müşteri oluşturma modu
description: Bu makale, Microsoft Dynamics 365 Commerce'teki zaman uyumsuz müşteri oluşturma modunu açıklamaktadır.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 95102936871e15f8e525abca736fa75927569b34
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473719"
---
# <a name="asynchronous-customer-creation-mode"></a>Zaman uyumsuz müşteri oluşturma modu

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'teki zaman uyumsuz müşteri oluşturma modunu açıklamaktadır.

Commerce'te, iki müşteri oluşturma modu vardır: zaman uyumlu (veya senkron) ve zaman uyumsuz (veya asenkron). Varsayılan olarak, müşteriler zaman uyumlu olarak oluşturulur. Başka bir deyişle, bunlar Commerce headquarters'da gerçek zamanlı olarak oluşturulur. Zaman uyumlu müşteri oluşturma modu, tüm kanallar arasında yeni müşteriler hemen aranabilir hale geldiği için yararlıdır. Ancak, bir dezavantajı da vardır. Commerce genel merkezine [Commerce Data Exchange: Gerçek Zamanlı Servis](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) çağrıları oluşturduğundan, birçok eşzamanlı müşteri oluşturma çağrısı yapılırsa performans etkilenebilir.

**Zaman uyumsuz modda müşteri oluştur** seçeneği mağazanın işlevsellik profilinde **Evet** olarak ayarlanmışsa (**Perakende ve Commerce \> Channel kurulum \> çevrimiçi mağaza kurulumu \> İşlev profilleri**), gerçek zamanlı Servis çağrıları kanal veritabanında müşteri kayıtları oluşturmak için kullanılmaz. Zaman uyumsuz müşteri oluşturma modu, Commerce genel merkezinin performansını etkilemez. Bir geçici genel benzersiz tanımlayıcı (GUID), her yeni zaman uyumsuz müşteri kaydına atanır ve müşteri hesap kodu olarak kullanılır. Bu GUID, satış noktası (POS) kullanıcıları için gösterilmez. Bunun yerine, bu kullanıcılar müşteri hesap kodu olarak **bekleyen eşitlemeyi** görürler.

> [!IMPORTANT]
> POS çevrimdışı olduğunda zaman uyumsuz müşteri oluşturma modu devre dışı bırakılsa bile sistem otomatik olarak müşterileri zaman uyumsuz olarak oluşturur. Bu nedenle, zaman uyumlu ile zaman uyumsuz oluşturma arasındaki seçiminizden bağımsız olarak Commerce headquarters yöneticilerinin, zaman uyumsuz müşterilerin Commerce headquarters'da zaman uyumlu müşterilere dönüştürülmesi için **P işi**, **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işi ve **1010** işi için yinelenen bir toplu iş oluşturup zamanlaması gerekir.

## <a name="async-customer-limitations"></a>Zaman uyumsuz müşteri sınırlamaları

Zaman uyumsuz müşteri işlevinde şu sınırlama vardır:

- Yeni müşteri hesap kodu kanalla geri eşitlenmedikçe, bağlılık programı kartları zaman uyumsuz müşterilere verilemez.

## <a name="async-customer-enhancements"></a>Zaman uyumsuz müşteri iyileştirmeleri

Kuruluşların müşterileri yönetmek için zaman uyumsuz müşteri oluşturma modunu kullanmasına yardımcı olmak ve Commerce Headquarters ile gerçek zamanlı iletişimleri azaltmaya yardımcı olmak için aşağıdaki geliştirmeler, kanallardaki zaman uyumlu ve zaman uyumsuz modları arasında eşliği sağlamak amacıyla kullanıma sunulmuştur. 

| Özellik geliştirmesi | Commerce sürümü | Özellik ayrıntıları |
|---|---|---|
| Müşteri bilgileri kanal veritabanından alınırken performans iyileştirmeleri | 10.0.20 ve üzeri | Performansın artırılmasına yardımcı olmak için, müşteri varlığı daha küçük varlıklara bölünür. Sistem daha sonra yalnızca kanal veritabanından gerekli bilgileri alır. |
| Ödeme sırasında zaman uyumsuz olarak adres oluşturma yeteneği | 10.0.22 ve üzeri | <p>Özellik anahtarı: **Müşteri adresleri için zaman uyumsuz oluşturmayı etkinleştir**</p><p>Özellik ayrıntıları:</p><ul><li>Commerce Headquarters'a gerçek zamanlı servis çağrıları yapmadan adres ekleme yeteneği</li><li>Kayıt kodu (**RecId** değeri) kullanmadan kanal veritabanındaki adresleri benzersiz olarak tanımlama yeteneği</li><li>Adres oluşturma için zaman damgalarını izleme</li><li>Commerce Headquarters'da adreslerin eşitlenmesi</li></ul><p>Bu özellik hem zaman uyumlu müşterileri hem de zaman uyumsuz müşterileri etkiler. Adresleri zaman uyumsuz oluşturmaya ek olarak adreslerin zaman uyumsuz olarak düzenlenmesi için, **Zaman uyumsuz modda müşterileri düzenlemeyi etkinleştir** özelliğini etkinleştirmeniz gerekir.</p> |
| Zaman uyumlu ve zaman uyumsuz müşteri oluşturma arasında eşliği etkinleştirin. | 10.0.24 ve üzeri | <p>Özellik anahtarı: **Gelişmiş zaman uyumsuz müşteri oluşturmayı etkinleştir**</p><p>Özellik ayrıntıları: Müşteri zaman uyumsuz olarak oluşturulurken, başlık, varsayılan müşteriden gelen ilişkiler ve ikincil ilgili kişi bilgileri (telefon numarası ve e-posta adresi) gibi ek bilgileri yakalayabilme</p> |
| Kullanıcı dostu hata iletileri | 10.0.28 ve üzeri | Bu geliştirmeler, eşitleme işlemi sürerken bir kullanıcı bilgileri hemen düzenleyemiyorsa kullanıcı dostu hata iletilerini geliştirmeye yardımcı olur. Bu geliştirmeleri, Commerce site oluşturucuda **Site ayarları \> Uzantılar** bölümünde **Belirli kullanıcı arabirimi öğelerinin zaman uyumsuz müşteri tarafından değiştirilemez olmasını sağla** ayarını kullanarak etkinleştirebilirsiniz. |
| Müşteri bilgilerini zaman uyumsuz olarak düzenleme yeteneği | 10.0.29 ve üzeri | <p>Özellik anahtarı: **Zaman uyumsuz modda müşterileri düzenlemeyi etkinleştir**</p><p>Özellik ayrıntıları: Müşteri verilerini zaman uyumsuz olarak düzenleme yeteneği</p><p>Müşteri bilgilerini zaman uyumsuz olarak düzenlemeyle ilgili sorunlar hakkındaki genel soruların yanıtları için bkz. [Zaman uyumsuz müşteri oluşturma modu hakkında SSS](async-customer-mode-faq.md).</p> |

### <a name="feature-switch-hierarchy"></a>Özellik anahtarı hiyerarşisi

Özellik anahtarlarının hiyerarşisi nedeniyle, **Zaman uyumsuz modda müşterileri düzenlemeyi etkinleştir** özelliğini etkinleştirmeden önce, aşağıdaki özellikleri etkinleştirmeniz gerekir: 

- **Müşteri siparişleri ve müşteri hareketleri için performans iyileştirmeleri** - Bu özellik, Commerce sürüm 10.0.28'in yayınlanmasından bu yana zorunlu hale getirilmiştir. 
- **Gelişmiş zaman uyumsuz müşteri oluşturmayı etkinleştirme**
- **Müşteri adresleri için zaman uyumsuz oluşturmayı etkinleştir**

Genel sorun giderme sorularına yanıtlar için bkz. [Zaman uyumsuz müşteri oluşturma modu hakkında SSS](async-customer-mode-faq.md). 

Daha önce bahsedilen özellikleri etkinleştirdikten sonra zaman uyumsuz müşterilerin Commerce genel merkezinde zaman uyumlu müşterilere dönüştürülmesi için **P işi**, **Zaman uyumsuz modundan müşteri ve iş ortaklarını eşitle** işi ve **1010** işi için yinelenen bir toplu iş oluşturup planlamanız gerekir.

### <a name="customer-creation-in-pos-offline-mode"></a>POS Çevrimdışı modunda müşteri oluşturma

Daha önce bahsedildiği gibi, POS çevrimdışı olduğunda zaman uyumsuz müşteri oluşturma modu devre dışı bırakılsa bile sistem otomatik olarak müşterileri zaman uyumsuz olarak oluşturur. Bu nedenle, Commerce genel merkezi yöneticilerinin zaman uyumsuz müşterilerin Commerce genel merkezinde zaman uyumlu müşterilere dönüştürülmesi için **P işi**, **Zaman uyumsuz modundan müşteri ve iş ortaklarını eşitle** işi ve **1010** işi için yinelenen bir toplu iş oluşturup planlaması gerekir.

> [!NOTE]
> **Paylaşılan müşteri veri tablolarını filtrele** seçeneği, **Commerce kanal şeması** sayfasında **Evet** olarak ayarlanmışsa (**Perakende ve Commerce \> Genel merkez kurulumu \> Commerce Planlayıcı \> Kanal veritabanı grubu**), müşteri kayıtları POS çevrimdışı modunda oluşturulmaz. Daha fazla bilgi için bkz. [Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Ek kaynaklar

[Mağazalardaki müşteri yönetimi](customer-mgmt-stores.md)

[Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürme](convert-async-to-sync.md)

[Müşteri öznitelikleri](dev-itpro/customer-attributes.md)

[Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
