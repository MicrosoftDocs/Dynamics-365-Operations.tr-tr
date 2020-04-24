---
title: Dynamics 365 Finance'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Finance'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175120"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance'ta kaldırılan veya artık kullanılmayan özellikler

[!include [banner](../includes/banner.md)]

Bu konu Dynamics 365 Finance'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance 10.0.12 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Lehçe SSRS raporları: Satış KDV kaydı, Satınalma KDV kaydı, AB Özeti KDV kaydı – Özellik referansı PL-00014

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yasal olarak gerekli değildir.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet (KDV beyannamesiyle Standart Denetim Dosyası için Excel biçimi - JPK_VDEK) |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Temmuz 2021 itibarıyla, SSRS raporlarını desteklememeyi planlıyoruz: **Satış KDV kaydı, Satınalma KDV kaydı, AB Özet KDV kaydı – Özellik referansı PL-00014**. Bunun yerine, KDV beyannamesi ile Standart Denetim Dosyası (JPK_VDEK) için Excel biçiminde bir örnek kullanıma sunulacaktır. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance 10.0.11 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="norwegian-standard-main-accounts"></a>Norveç Standart ana hesapları

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeniden tasarla  |
| **Başka bir özellikle mi değiştirildi?**   | Evet (ER biçimi uygulamaya özgü parametreleriyle değiştirildi) |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Nisan 2021 itibarıyla Standart ana hesaplarla ilgili işlevleri desteklememeyi planlıyoruz: Referans alanı, ilgili tablo, veri varlığı. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance 10.0.7 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>İş akışı isteği değişikliği iletişim kutusu artık kullanıcı seçimi açılan listesini içermiyor
|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Hesap grupları seçimine sahip özellik olarak değiştirildi.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | İş Akışı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Aralık 2020 itibarıyla, Hesap grupları seçimi içermeyen Çince fiş türleri kurulumunu desteklememeyi planlıyoruz. [10.0.7'deki Yenilikler](whats-new-changed-10-0-7.md)'de yeni tasarım hakkında daha fazla bilgi bulabilirsiniz. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) bakın.
