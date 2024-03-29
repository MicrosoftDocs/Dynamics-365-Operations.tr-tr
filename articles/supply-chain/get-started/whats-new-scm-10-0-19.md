---
title: Dynamics 365 Supply Chain Management sürüm 10.0.19'teki yenilikler ve değişiklikler (Haziran 2021)
description: Bu makalede, Dynamics 365 Supply Chain Management 10.0.19'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de9d20ba7ffc0bc5201ccafc2157a13983923249
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2022
ms.locfileid: "9125037"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Dynamics 365 Supply Chain Management sürüm 10.0.19'teki yenilikler ve değişiklikler (Haziran 2021)

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Supply Chain Management sürümü 10.0.19'teki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.837 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Nisan 2021
- **Sürüm genel kullanılabilirliği (kendi kendine güncelleştirme):** Haziran 2021
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Haziran 2021

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürümde yer alan özellikler yer almaktadır. *Özellik* sütunu, her bir özellik için resmi kullanıma sunma tarihlerini görebileceğiniz [kullanıma sunma planına](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) bağlantılar sağlar. *Ek bilgi* sütunu, ilgili belgelerin diğer ayrıntılrını ve/veya bağlantılarını sağlar.

Bu özelliklerin çoğunun kullanılabilmesi için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanılarak etkinleştirilmesi gerekir.

| Özellik alanı | Özellik | Daha fazla bilgi |
|---|---|---|
| Stok&nbsp;ve&nbsp;lojistik | [Satıcının gönderdiği banka ayrıntılarını onaylama ve kaydetme](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Satıcı banka hesabı bilgilerini koruma](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Stok ve lojistik | [İlgili kişi veri varlığını dışa aktarma optimizasyonu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Bu özellik Etkinleştirildiğinde, başvurulan verilerde yapılan değişiklikler ilgili kişilerin sonraki artımlı dışa aktarma işlemine eklenmesine neden olmaz. Bu özellik devre dışı bırakıldığında, başvurulan verilerde yapılan değişiklikler ilgili kişilerin sonraki artımlı dışa aktarma işlemine eklenmesine neden lur. |
| Stok ve lojistik | [Ölçek birimlerine sahip ambar yürütme yeteneği için artımlı geliştirmeler](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[İleti işlemci iletileri](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Ambar stoku düzeltmesi](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Stok ve lojistik | [Satış teklifi sayfasındaki Belge giriş ve Belge sonuç alanları için arama özelliği](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Bu özellik, **Satış teklifi** sayfasındaki **Belge giriş** ve **Belge sonuç** alanları için arama özelliği ekler.<br><br>Varsayılan olarak bu özellik etkindir. |
| Stok ve lojistik | [Özel donanımınızda uç ölçek birimleriyle ambar yürütme](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Özel donanımda LBD kullanarak kenar ölçek birimleri dağıtma](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| İmalat | [Özel donanımınızda uç ölçek birimleriyle üretim yürütme](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Özel donanımda LBD kullanarak kenar ölçek birimleri dağıtma](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planlama | Sorgu temelli planlı sipariş kesinleştirme | [Kesinleşmiş planlı siparişler](../master-planning/planning-optimization/planned-order-firming.md) |
| Ürün bilgileri yönetimi | [Çeşit önerileri sayfa geliştirmeleri](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Önceden tanımlanmış ürün çeşitleri oluşturma](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde yer alan özellik iyileştirmeleri yer almaktadır. Bunların her biri varolan bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca geliştirmeler olduğundan, [sürüm planında](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmezler. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe). Bu özelliklerden herhangi birini kullanmak istiyorsanız, bunları [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'nde açıkça etkinleştirmeniz gerekir.

| Modül | Özellik&nbsp;yönetiminde&nbsp;özellik&nbsp;adı | Daha fazla bilgi |
|---|---|---|
| Satış ve pazarlama | Satış geçmişi temizleme performansı iyileştirmeleri | Satış geçmişi temizleme, yüksek satış güncelleştirmeleri hacmine sahip ortamlarda seyrek çalıştırılırsa uzun sürebilir. Süreyi azaltmak ve güvenilirliği artırmak için bu özellik temizlemeyi sınırlı bir süre çalışan toplu işlere böler. Mümkün olduğunda, kilitlemeyi en aza indirmek ve temizleme sırasında işlem tablolarını birleştirmekten kaçınmak için veritabanı yeteneklerinden yararlanılacaktır. Daha fazla bilgi için bkz. [Satış geçmişi verilerini temizleme işlemini zamanlama](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| Satış ve pazarlama | Talep edilen giriş tarihini, şirketlerarası siparişlerin Onaylanan tarihiyle güncelleştir | Bu özellik, şirketlerarası doğrudan teslimat kullanırken satış ve satınalma tarihi alan değerlerine ne olacağını denetlemenizi sağlar. Sistemin istenen tarihleri güncelleştirip güncelleştirmeyeceğini veya güncelleştirmeyi atlayıp atlamayacağını seçebilirsiniz. Güncelleştirmeyi atlarsanız, istenen tarihler müşterinin isteklerini temsil eder. Güncelleştirmeyi etkinleştirirseniz, istenen tarihler (teslimat tarihi denetimini kullanırken) yalnızca başlangıçta müşterinin istediğini temsil eder. Teslim tarihi denetimi, *Yok*'dan farklı olduğunda, başlangıçta isteneni geçersiz kılar. Bu seçeneği, şirketlerarası satıcı veya müşteri ayarlarında **Onaylanan tarih ayarıyla yeni İstenen giriş tarihini güncelleştir**'i kullanarak ayarlayabilirsiniz.<br><br>Özellik devre dışı bırakılırsa, sistem teslimat tarihi denetim kuralına göre orijinal satış siparişlerinde istenen giriş tarihinin üzerine yazar, ancak istenen sevkiyat tarihi olduğu gibi kalır. |
| Ambar yönetimi | Ambara serbest bırakırken miktarları en yakın satış birimine indirgenecek şekilde yuvarla | Bu özellik, serbest bırakıldığındaki sipariş miktarlarını ambara kısıtlayabilecek bir seçenek ekler. Etkinleştirildiğinde, sipariş miktarları en yakın tüm satış birimine yuvarlanır ve birden az satış birimi için miktar içeren siparişler serbest bırakılmak üzere reddedilir. |
| Ambar yönetimi | Kuruluşu genelindeki "İş oluşturmayı planla" dalga yöntemi | Bu özelliği etkinleştirmek, *İş oluşturmayı planlama* dalga yöntemi (), tüm yasal varlıklarda paralel çalışacak şekilde eklenir ve yapılandırılır. Birkaç ek ayar da etkilenecektir. Tüm ayrıntılar için bkz. [Dalga sırasında iş oluşturmayı zamanlama](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki yardım makalelerini yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Önceki bölümde listelendiği gibi, bunların bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez ancak var olan özelliklerden daha fazla bilgi almanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş makaleler |
|---|---|
| Mühendislik değişikliği yönetimi | [Mühendislik değişim yönetimi hakkında SSS](../engineering-change-management/change-management-faq.md) |
| Tedarik ve kaynak atama | [Satıcılardan gelen kategori istekleri](../procurement/category-requests-from-vendors.md) |
| Ürün bilgileri yönetimi | [Ölçü birimini yönetme](../pim/tasks/manage-unit-measure.md)<br><br>[Ürün yapılandırma modeli hesaplamaları](../pim/config-model-calculations.md) |
| Üretim denetimi | [İş kimlikleri için birleşik numara serisi](../production-control/unified-job-ids.md) |
| Taşıma yönetimi | [LTL sınıfları](../transportation/ltl-class.md)<br><br>[NMFC kodları](../transportation/nmfc-codes.md) |
| Ambar yönetimi, dalga oluşturma ve işleme | [Dalga oluşturma ve işleme](../warehousing/wave-processing.md)<br><br>[Dalga işleme için ambar parametreleri](../warehousing/wave-warehouse-parameters.md)<br><br>[Dalga şablonları](../warehousing/wave-templates.md)<br><br>[Dalga tahsisatı](../warehousing/wave-allocation-method.md)<br><br>[Dalga sırasında iş oluşturmayı zamanlama](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Konteyner kullanımı](../warehousing/wave-containerization.md)<br><br>[Dalga yürütme bildirimleri](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve operasyon uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.19 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamalarının 10.0.19 sürümü için platform güncelleştirmeleri (Haziran 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.19'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415) görüntüleyin.

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 sürüm dalgası 1 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365: 2021 sürüm dalgası 1 planını](/dynamics365-release-plan/2021wave1/) inceleyin. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) makalesi Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

