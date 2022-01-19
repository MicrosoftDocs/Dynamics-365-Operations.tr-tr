---
title: Mühendislik değişikliği yönetimine genel bakış (video içerir)
description: Bu konuda, ürün sürümü oluşturma ve yönetme, ürün yaşam döngüleri ve mühendislik değişikliklerini yönetmenize yardımcı olan mühendislik değişikliği yönetimine genel bir bakış sağlanmaktadır.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d667aef827addcf7c34075b08afffffe3fd71935
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952610"
---
# <a name="engineering-change-management-overview"></a>Mühendislik değişikliği yönetimine genel bakış

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Özellik özeti

Günümüzde üreticiler; ürün yaşam döngülerinin giderek daha da kısaldığı, kalite ve güvenilirlik gereksinimlerinin arttığı ve ürün güvenliğine daha da fazla yoğunlaşıldığı bir dünyada başarılı olmak için güçlü ürün verileri yönetimi, sürüm denetimi ve mühendislik değişikliği yönetimine ihtiyaç duymaktadır.

Mühendislik değişikliği yönetimi, ürün veri yönetimi sürecine yapı ve disiplin katar ve ürünlerin iş akışları tarafından desteklenen denetimli bir şekilde tanımlanmasını, sunulmasını ve gözden geçirilmesini sağlar. Ürün sürümleri ve mühendislik değişikliği yönetimi aracılığıyla, mühendislik değişikliklerinin etkisini değerlendirebilir ve bu değişiklikleri ürün yaşam döngüsü boyunca uygulayabilirsiniz.

Mühendislik değişikliği yönetimi, ürün sürümü oluşturma ve yönetme, ürün yaşam döngüleri ve mühendislik değişikliklerini yönetmenize yardımcı olur. Temel özelliklerinin listesi aşağıdadır:

- Ürün sürümü oluşturma
- Ürün ana verilerini tek bir tüzel kişilikte (mühendislik şirketi) korumanıza ve tamamıyla yapılandırılmış, piyasaya sunulmuş ürünü diğer tüzel kişiliklere yayımlamanıza olanak tanıyan geliştirilmiş ürün sürümü işlevleri
- Bir ürün sürümü etkinleştirilmeden önce gerekli bilgilerin girildiğini doğrulayan kurallar (hazırlık denetimleri)
- Piyasaya sunulan bir ürünün belirli iş süreçlerinde kullanılabileceği durumlarda ayrıntılı denetim aracılığıyla geliştirilmiş ürün yaşam döngüsü yönetimi
- İş akışları tarafından desteklenen mühendislik değişikliği istekleri
- İş akışları tarafından desteklenen mühendislik değişikliği siparişleri

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Önceki video ([Dynamics 365 Supply Chain Management'taki değişiklik yönetimi özellikleri](https://youtu.be/N313FqvRuBc)) YouTube'daki [Finance and Operations oynatma listesinde](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) yer almaktadır.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Sisteminiz için mühendislik değişikliği yönetimi özelliklerini açma

Mühendislik değişikliği yönetimini kullanabilmeniz için hem *Mühendislik Değişikliği Yönetimi* özelliğini hem de özelliğin yapılandırma anahtarını etkinleştirmeniz gerekir. Hareketlerdeki ürünlerin sürüm boyutunu da izlemek istiyorsanız (isteğe bağlı) hem *Ürün sürümü boyutu* özelliğini hem de özelliğin yapılandırma anahtarını etkinleştirmeniz gerekir. Bu önkoşullar gerektiği gibi ayarlandıktan sonra mühendislik değişikliği yönetiminin isteğe bağlı ek özelliklerini açabilirsiniz.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>Temel mühendislik değişikliği yönetimi özelliklerini açma

Önce aşağıdaki adımları izleyerek özelliği etkinleştirin.

1. [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanına gidin.
1. Güncelleştirmeleri denetleyin.
1. *Mühendislik Değişikliği Yönetimi* adlı özelliği açın.
1. Kullanmak istiyorsanız *Ürün boyutu sürümü* adlı özelliği de açın.

### <a name="turn-on-the-required-configuration-keys"></a>Gerekli yapılandırma anahtarlarını açma

Sonra, aşağıdaki adımları izleyerek yapılandırma anahtarını açın.

1. Sisteminizi [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım moduna alın.
1. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
1. **Ticaret** düğümünü genişletin.
1. **Mühendislik Değişim Yönetimi** onay kutusunu seçerek ana özellik için yapılandırma anahtarını etkinleştirin.
1. **Mühendislik Değişiklik Yönetimi** düğümünü genişletin ve aşağıdaki onay kutularını gerektiği gibi seçin veya temizleyin (kullanmak istediğiniz özelliklere bağlı olarak):

    - **Öznitelik arama** – [Öznitelik arama özelliğini](engineering-attributes-and-search.md) etkinleştirmek için bu onay kutusunu seçin. Bu özelliği etkinleştirmenizi öneririz ancak kullanmayacaksanız bu onay kutusunu temizleyebilirsiniz.
    - **Proses üretimi için değişiklik yönetimi** – Proses üretimi formüllerindeki değişiklikleri yönetmek için Mühendislik değişiklik yönetimi özelliklerini kullanmak istiyorsanız bu onay kutusunu seçin. Formülleri yönetmeniz gerek yoksa, bu onay kutusunu temizleyebilirsiniz. Daha fazla bilgi için bkz. [Formüllerde ve içeriklerindeki değişiklikleri yönetme](manage-formula-changes.md).

1. Sürüm boyutunu da kullanmak istiyorsanız **Ürün boyutu - Sürüm** onay kutusunu da seçin. (Bu onay kutusu listede daha aşağıdadır, **Mühendislik Değişim Yönetimi** düğümünün içinde değildir.)
1. [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım modunu kapatın.
1. Konfigürasyon anahtarlarının doğru şekilde etkinleştirildiğinden emin olmak için veritabanı eşitlemeyi çalıştırın.

> [!IMPORTANT]
> 2022 Nisan'dan itibaren, tüm yeni yüklemelerde **Mühendislik Değişim Yönetimi** ve **Ürün boyutu- Sürüm** için lisans anahtarları varsayılan olarak etkinleştirilir, ancak gerekirse bunları devre dışı bırakabilirsiniz.

### <a name="turn-on-additional-engineering-change-management-features"></a>Ek mühendislik değişikliği yönetimi özelliklerini açma

Mühendislik değişikliği yönetimi temel özelliklerini açtıktan ve yapılandırma anahtarlarını etkinleştirdikten sonra özellik yönetimine çeşitli ek ve isteğe bağlı mühendislik değişikliği yönetimi özellikleri eklenir. Bu özelliklerin her biri **Mühendislik değişikliği yönetimi** modülü altında listelenmiştir. Aşağıdaki tablo isteğe bağlı tüm özellikleri açıklar ve daha fazla bilgi için bağlantılar sağlar.

| Özellik yönetiminde özellik adı | Tanım |
|---|---|
| Mevcut ürünlerde değişiklik yönetimini etkinleştirme | <p>Bu özellik, mühendislik değişikliği yönetimini kullanarak yönetmeye başlayabilmeniz için var olan ürünleri mühendislik ürünlerine dönüştürmenizi sağlar.</p><p>Daha fazla bilgi için bkz. [Mevcut ürünlerde değişiklik yönetimini etkinleştirme](change-management-existing-products.md).</p> |
| Üretim bölümü için mühendislik bildirimleri | <p>Mühendislikte bir ürün değiştirildiğinde bu değişiklikler hakkında üretime bilgi vermek önemli olabilir. Bu şekilde, üretim çalışanları bileşen değiştirme, ürün reçetesi (BOM) değiştirme veya rota değiştirme gibi uygun önlemleri alabilir. Bu özellik, üretilmekte olan ürünlerde yapılan değişiklikler hakkında üretime bildirimde bulunmanızı sağlar.</p><p>Daha fazla bilgi için bkz. [Mühendislik ürünlerindeki değişiklikleri yönetme](engineering-change-management.md).</p> |
| Mühendislik Değişikliği Yönetimi'nde geliştirilmiş öznitelik devralma | <p>Bu özellik, bitmiş ürünler veya ara ürünlerin özniteliklerinin yönetimini basitleştirir. Bu özellik açık duruma getirildiğinde bir maddeye ait olan tüm öznitelikleri belirlemek daha kolaydır ve o maddeden ana maddeye yayılması gereken öznitelikleri seçebilirsiniz. Bu özellik, örneğin bitmiş bir ürünün bir bileşeni kırılabilir, zehirli veya yanıcı olduğunda kullanışlıdır çünkü kırılabilir, zehirli veya yanıcı özniteliği bu sayede kolayca tanımlayabilir ve bunu bitmiş ürüne yayabilirsiniz.</p><p>Daha fazla bilgi için bkz. [Mühendislik öznitelikleri ve mühendislik özniteliği araması](engineering-attributes-and-search.md).</p> |
| Ürün hazır olma denetimleri | <p>Bu özellik, standart (mühendislik dışı) ürünler için hazırlık denetimleri uygulamanıza olanak tanır. Ürün kullanılabilir duruma getirilmeden ve hareketlerde kullanılmadan önce her ürünün tam olarak tanımlandığından ve gerekli tüm ilkelerin yapılandırıldığından emin olmak için ürün hazırlık denetimleri kullanın. Bu özelliği bir süre kullandıktan sonra devre dışı bırakırsanız standart ürünler için var olan tüm hazırlık denetimleri silinir.</p><p>Daha fazla bilgi için bkz. [Ürün hazırlığı](product-readiness.md).</p> |
| Formüllerdeki ve formül içeriklerindeki değişiklikleri yönet | <p>Bu özellik, formül bileşenlerinde, ortak ürünlerde ve yan ürünlerde yapılan değişiklikleri izlemenizi sağlar.</p><p>Daha fazla bilgi için bkz. [Formüllerde ve içeriklerindeki değişiklikleri yönetme](manage-formula-changes.md).</p> |
| Mühendislik ürünleri için çeşit oluşturma | <p>Bu özellik, mühendislik ürünleri için kullanılabilir boyut değerlerine göre çeşitler oluşturmanıza olanak tanır.</p><p>Daha fazla bilgi için bkz. [Mühendislik ürünleri için çeşitler oluşturma](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
