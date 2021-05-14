---
title: Dynamics 365 Finance'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Finance'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 93d025759f86ffeb0ee1f1e6e6e2aeb3ab341b75
ms.sourcegitcommit: 4ba25601eba295bd9057f7fb5e85f1f6764f5a27
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/30/2021
ms.locfileid: "5965322"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance'ta kaldırılan veya artık kullanılmayan özellikler

[!include [banner](../includes/banner.md)]

Bu konu Dynamics 365 Finance'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](/dynamics/s-e/global/axtechrefrep_61) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Finance 10.0.20 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="rtir-query-invoice-data-request-hu-format-configuration"></a>RTIR Sorgusu Fatura Ayrıntısı İsteği (HU) biçimi yapılandırması

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Macarca çevrimiçi faturalama sistemiyle birlikte çalışabilirlik elektronik ileti işleme işlemi dışında bırakıldı |
| **Başka bir özellikle mi değiştirildi?**   | No |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 15 Nisan 2022 itibarıyla, "RTIR Sorgusu Fatura Verileri İsteği (HU)" biçimi yapılandırması desteğini sonlandırmayı planlıyoruz. |


## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Finance 10.0.17 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>Elektronik raporlama yapılandırmaları için depolama seçeneği olarak LCS deposu

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni Regulatory Configuration Service (RCS) genel deposu ile değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Dynamics 365 Finance, Supply Chain Management ve Project Operations ürünleri|
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Nisan 2022 tarihinden itibaren Microsoft Dynamics Lifecycle Services (LCS) deposunu Elektronik raporlama (ER) yapılandırmaları için bir depolama seçeneği olarak desteklememeyi planlıyoruz. Yeni Microsoft ER yapılandırmaları Global depodan özel olarak indirilmek üzere yayımlanacaktır. Global depoya Dynamics 365 ürünlerinden ve RCS'den erişilebilir. Daha fazla bilgi için bkz. [ER yapılandırmalarını RCS'den içe aktarma](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Finance 10.0.16 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>Çek Cumhuriyeti için "KDV beyannamesi (CZ)" ve "Denetim ifadesi dışarı aktarma (CZ)" elektronik raporlama biçimleri

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni biçimlerle değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 22 Ocak 2022 tarihine kadar "KDV beyannamesi (CZ)", "Denetim ifadesi dışarı aktarma (CZ)" elektronik raporlama (ER) biçimleri için desteği kaldırmayı planlıyoruz. Bunun yerine yeni KDV beyannamesi XML'i (CZ), KDV beyanname Excel'i (CZ), KDV denetim ekstresi XML'i (CZ) biçimleri, "Vergi beyanı" modeli altında sunulmaktadır. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"Genel muhasebe defteri hareketi dışarı aktarma biçimi (BE)" Belçika için elektronik raporlama biçimi ve ilgili "Genel muhasebe defteri hareketi dışarı aktarma (BE)" modeli

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | "Standart Denetim Dosyası (SAF-T)" modeli altındaki yeni ER biçimi ile değiştirildi.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Aralık 2021'e kadar "Genel muhasebe defteri hareketi dışarı aktarma biçimi (BE)" Elektronik raporlama biçimi ve ilgili "Genel muhasebe defteri hareketi dışarı aktarma (BE)" modeli için sunduğumuz desteği kaldırmayı planlıyoruz. "Standart Denetim Dosyası (SAF-T)" modeli kapsamında, bunun yerine "Genel muhasebe veri modeli eşleme" ile birlikte yeni bir "Genel muhasebe veri dışarı aktarma (BE) biçimi" sunulmuştur. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>Birleşik Krallık için SSRS biçiminde "KDV 100" raporu

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | "Vergi beyannamesi modeli" kapsamında yeni ER biçimi - "KDV Beyannamesi Excel (UK)" biçimi ile değiştirilmiştir.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Aralık 2021'e kadar, SSRS biçimindeki "KDV 100 raporu" için sunduğumuz desteği kaldırmayı planlıyoruz. [MTD KDV özelliğinde](../localizations/emea-gbr-mtd-vat-integration.md) "Vergi beyanı modeli" kapsamında yeni bir "KDV Beyannamesi Excel (UK)" biçimi kullanıma sunulmuştur. |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Finance 10.0.15 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 için Internet Explorer 11 desteği kullanım dışı bırakılmıştır

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aralık 2020 itibarıyla geçerli olmak üzere, tüm Dynamics 365 ürünleri için Microsoft Internet Explorer 11 desteği kullanım dışı, bırakılacaktır ve Internet Explorer 11, Ağustos 2021'den sonra desteklenmeyecektir.<br><br>Bu, Internet Explorer 11 arabirimi aracılığıyla kullanılmak üzere tasarlanmış olan Dynamics 365 ürünlerini kullanan müşterileri etkileyecektir. Ağustos 2021'den sonra, Internet Explorer 11, bu tür Dynamics 365 ürünleri için desteklenmeyecektir. |
| **Başka bir özellikle mi değiştirildi?**   | Müşterilerin Microsoft Edge'e geçiş yapması önerilir.|
| **Etkilenen ürün alanları**         | Tüm Dynamics 365 ürünleri |
| **Dağıtım seçeneği**              | Tümü|
| **Durum**                         | Kaldırıldı. Internet Explorer 11 Ağustos 2021'den sonra desteklenmeyecektir.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance 10.0.12 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Kullanımdan kaldırılmadı: Lehçe SSRS raporları: Satış KDV kaydı, Satınalma KDV kaydı, AB Özeti KDV kaydı – Özellik referansı PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yasal olarak gerekli değildir.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet (KDV beyannamesiyle Standart Denetim Dosyası için Excel biçimi - JPK_VDEK) |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırılmadı: 27 Nisan 2021 itibarıyla, SSRS raporlarını desteklemeye devam etmeyi planlıyoruz: **Satış KDV kaydı, Satınalma KDV kaydı, AB Özet KDV kaydı – Özellik referansı PL-00014**. Bunun yerine, KDV beyannamesi ile Standart Denetim Dosyası (JPK_VDEK) için Excel biçiminde bir örnek kullanıma sunuldu. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance 10.0.11 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="norwegian-standard-main-accounts"></a>Norveç Standart ana hesapları

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeniden tasarla  |
| **Başka bir özellikle mi değiştirildi?**   | Evet (ER biçimi uygulamaya özgü parametreleriyle değiştirildi) |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Nisan 2021 itibarıyla Standart ana hesaplarla ilgili işlevleri desteklememeyi planlıyoruz: Referans alanı, ilgili tablo, veri varlığı. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance 10.0.7 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>İş akışı isteği değişikliği iletişim kutusu artık kullanıcı seçimi açılan listesini içermiyor

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Hesap grupları seçimine sahip özellik olarak değiştirildi.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | İş Akışı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Aralık 2020 itibarıyla, Hesap grupları seçimi içermeyen Çince fiş türleri kurulumunu desteklememeyi planlıyoruz. [10.0.7'deki Yenilikler](whats-new-changed-10-0-7.md)'de yeni tasarım hakkında daha fazla bilgi bulabilirsiniz. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) bakın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
