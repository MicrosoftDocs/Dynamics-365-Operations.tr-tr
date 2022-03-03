---
title: Mühendislik değişikliği yönetimine genel bakış (video içerir)
description: Bu konuda, ürün sürümü oluşturma ve yönetme, ürün yaşam döngüleri ve mühendislik değişikliklerini yönetmenize yardımcı olan mühendislik değişikliği yönetimine genel bir bakış sağlanmaktadır.
author: t-benebo
ms.date: 01/11/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 54d91d009d70194dfc91c8c855e0088f9de01718
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103825"
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

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Önceki video ([Dynamics 365 Supply Chain Management'ta değişim yönetimi özellikleri](https://youtu.be/N313FqvRuBc)), [Finance ve Operations oynatma listesindedir](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) ve YouTube'da yer almaktadır.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Sisteminiz için mühendislik değişikliği yönetimi özelliklerini açma

Mühendislik değişikliği yönetimini kullanabilmeniz için hem *Mühendislik Değişikliği Yönetimi* özelliğini hem de özelliğin yapılandırma anahtarını etkinleştirmeniz gerekir. Hareketlerdeki ürünlerin sürüm boyutunu da izlemek istiyorsanız (isteğe bağlı) hem *Ürün sürümü boyutu* özelliğini hem de özelliğin yapılandırma anahtarını etkinleştirmeniz gerekir. Bu önkoşullar gerektiği gibi ayarlandıktan sonra mühendislik değişikliği yönetiminin isteğe bağlı ek özelliklerini açabilirsiniz.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Temel mühendislik değişikliği yönetimi özelliklerini açma veya kapatma

Temel mühendislik değişikliği yönetimi özelliklerini açma veya kapatmak için bu adımları izleyin. Supply Chain Management sürüm 10.0.25 itibarıyla *Mühendislik Değişiklik Yönetimi* özelliği varsayılan olarak açıktır.

1. [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanına gidin.
1. Güncelleştirmeleri denetleyin.
1. *Mühendislik Değişiklik Yönetimi* adlı özelliği gerektiği gibi açın veya kapatın.
1. Hareketlerdeki ürünlerin sürüm boyutunu izlemek istiyorsanız (isteğe bağlı) *Ürün sürüm boyutu* adlı özelliği açın.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Gerekli yapılandırma anahtarlarını açma veya kapatma

Sonra, aşağıdaki adımları izleyerek yapılandırma anahtarını açın. Bunlar varsayılan olarak açık değildir.

1. Sisteminizi [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım moduna alın.
1. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
1. **Ticaret** düğümünü genişletin.
1. **Mühendislik Değişiklik Yönetimi** onay kutusunu kullanarak ana özellik için yapılandırma anahtarını etkinleştirin veya devre dışı bırakın.
1. **Mühendislik Değişiklik Yönetimi** düğümünü genişletin ve aşağıdaki onay kutularını gerektiği gibi seçin veya temizleyin (kullanmak istediğiniz özelliklere bağlı olarak):

    - **Öznitelik arama** – [Öznitelik arama özelliğini](engineering-attributes-and-search.md) etkinleştirmek için bu onay kutusunu seçin. Bu özelliği etkinleştirmenizi öneririz ancak kullanmayacaksanız bu onay kutusunu temizleyebilirsiniz.
    - **Proses üretimi için değişiklik yönetimi** – Proses üretimi formüllerindeki değişiklikleri yönetmek için Mühendislik değişiklik yönetimi özelliklerini kullanmak istiyorsanız bu onay kutusunu seçin. Formülleri yönetmeniz gerek yoksa, bu onay kutusunu temizleyebilirsiniz. Daha fazla bilgi için bkz. [Formüllerde ve içeriklerindeki değişiklikleri yönetme](manage-formula-changes.md).

1. Sürüm boyutunu da kullanmak istiyorsanız **Ürün boyutu - Sürüm** onay kutusunu da seçin. (Bu onay kutusu, listenin altında bulunur, **Mühendislik Değişiklik Yönetimi** düğümü içinde değildir.) Bu özelliğe gereksinim duymuyorsanız, bu onay kutusunu temizleyebilirsiniz.
1. [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım modunu kapatın.
1. Veritabanı, yapılandırma anahtarlarının değişikliklerinizi yansıtmak üzere doğru şekilde etkinleştirildiğinden emin olmak için eşitlenmelidir. Üzerinde çalıştığınız ortamın türüne bağlı olarak aşağıdaki adımlardan birini gerçekleştirin:
    - **Katman 1 (geliştirme) ortamları için**: Projenizi Microsoft Visual Studio'da açın ve **Dynamics 365 \> Veritabanı eşitle \> Eşitle**'yi seçin.
    - **Katman 2 (ve daha yüksek) ortamlar için**: Ortamı bakım moduna geçirdikten sonra otomatik olarak eşitler, bu adımı atlayabilirsiniz.

### <a name="turn-on-additional-engineering-change-management-features"></a>Ek mühendislik değişikliği yönetimi özelliklerini açma

Mühendislik değişikliği yönetimi temel özelliklerini açtıktan ve yapılandırma anahtarlarını etkinleştirdikten sonra özellik yönetimine çeşitli ek ve isteğe bağlı mühendislik değişikliği yönetimi özellikleri eklenir. Bu özelliklerin her biri **Mühendislik değişikliği yönetimi** modülü altında listelenmiştir. Aşağıdaki tablo isteğe bağlı tüm özellikleri açıklar ve daha fazla bilgi için bağlantılar sağlar. Supply Chain Management sürüm 10.0.25 itibarıyla, tüm bu özellikler varsayılan olarak açıktır ancak yine de devre dışı bırakabilirsiniz.

| Özellik yönetiminde özellik adı | Açıklama | Özellik durumu |
|---|---|---|
| Mevcut ürünlerde değişiklik yönetimini etkinleştirme | <p>Bu özellik, mühendislik değişikliği yönetimini kullanarak yönetmeye başlayabilmeniz için var olan ürünleri mühendislik ürünlerine dönüştürmenizi sağlar.</p><p>Daha fazla bilgi için bkz. [Mevcut ürünlerde değişiklik yönetimini etkinleştirme](change-management-existing-products.md).</p> |
| Üretim bölümü için mühendislik bildirimleri | <p>Mühendislikte bir ürün değiştirildiğinde bu değişiklikler hakkında üretime bilgi vermek önemli olabilir. Bu şekilde, üretim çalışanları bileşen değiştirme, ürün reçetesi (BOM) değiştirme veya rota değiştirme gibi uygun önlemleri alabilir. Bu özellik, üretilmekte olan ürünlerde yapılan değişiklikler hakkında üretime bildirimde bulunmanızı sağlar.</p><p>Daha fazla bilgi için bkz. [Mühendislik ürünlerindeki değişiklikleri yönetme](engineering-change-management.md).</p> |
| Mühendislik Değişikliği Yönetimi'nde geliştirilmiş öznitelik devralma | <p>Bu özellik, bitmiş ürünler veya ara ürünlerin özniteliklerinin yönetimini basitleştirir. Bu özellik açık duruma getirildiğinde bir maddeye ait olan tüm öznitelikleri belirlemek daha kolaydır ve o maddeden ana maddeye yayılması gereken öznitelikleri seçebilirsiniz. Bu özellik, örneğin bitmiş bir ürünün bir bileşeni kırılabilir, zehirli veya yanıcı olduğunda kullanışlıdır çünkü kırılabilir, zehirli veya yanıcı özniteliği bu sayede kolayca tanımlayabilir ve bunu bitmiş ürüne yayabilirsiniz.</p><p>Daha fazla bilgi için bkz. [Mühendislik öznitelikleri ve mühendislik özniteliği araması](engineering-attributes-and-search.md).</p> |
| Ürün hazır olma denetimleri | <p>Bu özellik, standart (mühendislik dışı) ürünler için hazırlık denetimleri uygulamanıza olanak tanır. Ürün kullanılabilir duruma getirilmeden ve hareketlerde kullanılmadan önce her ürünün tam olarak tanımlandığından ve gerekli tüm ilkelerin yapılandırıldığından emin olmak için ürün hazırlık denetimleri kullanın. Bu özelliği bir süre kullandıktan sonra devre dışı bırakırsanız standart ürünler için var olan tüm hazırlık denetimleri silinir.</p><p>Daha fazla bilgi için bkz. [Ürün hazırlığı](product-readiness.md).</p> |
| Formüllerdeki ve formül içeriklerindeki değişiklikleri yönet | <p>Bu özellik, formül bileşenlerinde, ortak ürünlerde ve yan ürünlerde yapılan değişiklikleri izlemenizi sağlar.</p><p>Daha fazla bilgi için bkz. [Formüllerde ve içeriklerindeki değişiklikleri yönetme](manage-formula-changes.md).</p> |
| Mühendislik ürünleri için çeşit oluşturma | <p>Bu özellik, mühendislik ürünleri için kullanılabilir boyut değerlerine göre çeşitler oluşturmanıza olanak tanır.</p><p>Daha fazla bilgi için bkz. [Mühendislik ürünleri için çeşitler oluşturma](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
