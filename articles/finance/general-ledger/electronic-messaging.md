---
title: Elektronik mesajlaşma
description: Bu konu, Microsoft Dynamics 365 Finance içinde elektronik mesajlaşma için kurulum bilgisi ve genel bakış sağlar.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 339e0c811a70ca6b722d8967c2df103500578664
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433731"
---
# <a name="electronic-messaging"></a>Elektronik mesajlaşma

[!include [banner](../includes/banner.md)]

Bu konu, **Elektronik iletiler** (EM) işlevine genel bakış ve kurulum bilgileri sağlar.

Yakın zamanda çeşitli ülkelerin ve bölgelerin hükümetleri ve mevzuatları, bu ülkelerde ve bölgelerde kayıtlı olan şirketler için raporlama gereksinimleri belirlemiştir. Gereksinimlerin amacı, bu şirketlerden verilerin elektronik biçimde, doğrudan tutuldukları, işlendikleri ve hesaplandıkları sistemlerden alınabilmesidir.

Microsoft Dynamics 365 Finance'taki EM işlevi, Finance ile hükümetler ve yasama otoritelerinin resmi bilgiyi raporlama, gönderme ve alma sistemleri arasında birlikte çalışabilirliği desteklemektedir.

EM işlevi, **Elektronik Raporlama** (ER) modülüne tümleşiktir. Elektronik iletiler için ER biçimlerini ayarlayabilirsiniz. Daha fazla bilgi için bkz: [Elektronik raporlamaya (ER) genel bakış](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>EM işlevi için temel kavramlar

EM işlevi aşağıdaki varlıkları temel alan bir işlevdir:

- **Elektronik ileti** – Bir vergi dairesine gönderilen rapor gibi dahili olarak rapor edilmesi veya iletilmesi gereken bir rapor veya beyanname.
- **Elektronik mesaj öğeleri** - Raporlanan mesaja dahil edilmesi gereken kayıtlar.
- **Elektronik ileti işleme** - Veri toplama, rapor oluşturma ve Azure Blob depolama içerisinde veri depolama, raporları sistem dışına aktarma, sistem dışından yanıtlar alma ve alınan bilgiye dayalı olarak veritabanını güncelleştirmek için çalıştırılması gereken bir eylem zinciri. Zincirdeki eylemler bağlı olabilir veya olmayabilir.

Aşağıdaki örnekte, Em için veri akışı gösterilmektedir.

![Elektronik ileti veri akışı.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>EM işlevi tarafından desteklenen senaryolar

EM işlevi, aşağıdaki senaryoları destekler:

- Çeşitli türlerdeki dışarı aktarma ER biçimlerini temel alan iletileri ve raporları el ile oluşturma. Bu türler arasında Microsoft Excel, XML, JavaScript Nesne Gösterimi (JSON), PDF, metin ve Microsoft Word bulunur.
- Bir otorite tarafından ilişkilendirilmiş bir içe aktarma ER biçimi aracılığıyla talep edilen veya alınan bilgiye dayalı iletileri otomatik olarak oluşturma ve işleme.
- Bir veri kaynağından bilgileri mesaj öğeleri olarak toplama ve işleme. Veri kaynağı bir Finance tablosudur.
- Ek bilgiler depolama, tanımlanmış çeşitli yürütülebilir sınıfları mesajlar veya mesaj öğelerine ilişkin değerlendirme.
- Mesaj öğelerinde toplanan bilgiyi bir araya getirme, bu bilgiyi mesaj ile bölme ve ER raporlama biçimlerinde ilişkilendirilmiş raporlar oluşturma.
- Azure Key Vault'ta depolanan bilgiyi kullanarak oluşturulan raporları bir web hizmetine aktarma.
- Bir web hizmetinden bir yanıt al, yanıtı yorumla ve Finance içindeki veriyi uygun biçimde güncelleştir.
- Oluşturulan tüm raporları depola ve gözden geçir.
- Bir mesaj veya mesaj öğesi için çalıştırılmış olan eylemlere ilişkin tüm kayıt bilgisini depola ve gözden geçir.
- Çeşitli mesaj durumları ve mesaj öğesi durumları ile işlemeyi kontrol et.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>EM işlevi tarafından desteklenen ülkeye özel mevzuat özellikleri

Aşağıdaki tablo, EM işlevi tarafından desteklenen ülkeye özel bazı mevzuat özellikleri hakkında bilgi sağlar.

| Ülke     | Özellik adı | Özellik demo kaydı |
|-------------|--------------|------------------------|
| İspanya       | [KDV'de Anında Bilgi Sağlama (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Macaristan     | [Çevrimiçi faturalama sistemi](../localizations/emea-hun-online-invoicing.md) | |
| Birleşik Krallık | [Vergiyi Dijital Hale Getirme (MTD) - KDV beyannamesi gönderme](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: UK Dijital Vergi - Dynamics 365'te KDV Beyannamesi](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litvanya   | [i.SAF raporlama](../localizations/emea-ltu-isaf.md) | |
| Polonya      | [Kayıtlarla KDV beyannamesi (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK KDV Denetim Kayıtları](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Hollanda | [Hollanda için KDV beyannamesi](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Çek Cumhuriyeti | [KDV beyannamesi](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brezilya      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rusya      | [KDV beyannamesi](../localizations/rus-vat-declaration.md) | |
| Rusya      | [Elektronik biçimde muhasebe raporlama](../localizations/rus-accounting-reporting.md) | |
| Rusya      | [Kazanç vergisi beyannamesi](../localizations/rus-profit-tax-declaration.md) | |
| Rusya      | [Değerlendirilmiş vergi beyannamesi](../localizations/rus-assessed-tax-declaration.md) | |
| Rusya      | [Taşıma vergisi beyannamesi](../localizations/rus-transport-tax-declaration.md) | |
| Rusya      | [Arazi vergisi beyannamesi](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

