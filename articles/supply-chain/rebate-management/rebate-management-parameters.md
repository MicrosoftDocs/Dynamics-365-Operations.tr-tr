---
title: İndirim yönetimi parametreleri
description: Bu konu, indirim yönetimi parametreleri sayfasını açıklar. Bu sayfa, deftere nakli, durum güncelleştirmelerini, numara serilerini ve diğer davranışı etkileyen ayarlar içerir.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0665ce41233308c814a514fccf3b73e20de64098
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576700"
---
# <a name="rebate-management-parameters"></a>İndirim yönetimi parametreleri

[!include [banner](../includes/banner.md)]

**İndirim yönetimi parametreleri** sayfası, **indirim yönetimi** modülü üzerinden uygulanan ayarları tanımlamak için kullanılır. Bu ayarlar deftere nakli, durum güncelleştirmelerini, numara serilerini ve diğer davranışı etkileyen ayarlar içerir. Bu sayfadaki kurulum yasal varlıklar genelinde paylaşılır ve uygun güvenlik izinlerine sahip kullanıcılar tarafından değiştirilebilir.

**İndirim yönetimi parametreleri** sayfasını açmak için **İndirim yönetimi \> Kurulum \> indirim yönetimi parametrelerine** gidin. Ardından, aşağıdaki alt bölümlerde açıklanan alanları ayarlayın.

## <a name="rebate-management-tab"></a>İndirim yönetimi sekmesi

Aşağıdaki tablo, **İndirim yönetimi parametreleri** sayfasının **İndirim yönetimi** sekmesinde kullanılabilen alanları tanımlar.

| Alan | Tanım |
|---|---|
| Varsayılan durum | Tüm yeni anlaşmalar için varsayılan durumu seçin. Seçim için kullanılabilen durum değerleri kümesini tanımlamak için [**indirim durumları** sayfasını kullanın](rebate-statuses.md). |
| Boyuta göre işleme | Provizyon, indirim ve gider yazma işlemlerinin mali boyut tarafından işlenip işlenmeyeceğini seçin. Bu seçenek etkinleştirildiğinde, sistem hedef hareketlerdeki kaynak hareketlerdeki finansal boyutları kullanır. |
| Daha önce nakledilip nakledilmediğini denetle | <p>Deftere nakledilmemiş indirim işlemleri aynı dönem için birden fazla kez işlenirse sistem davranışını seçin:</p><ul><li>**Uyarı**: Sistem, kullanıcıların orijinal işlem satırlarını geçersiz kılmasına izin verir, ancak bir uyarı görüntülenir.</li><li>**Hata**: Sistem kullanıcıların özgün işlem satırlarını geçersiz kılmasını engeller ve bir hata mesajı gösterilir. |
| Günlükleri otomatik olarak deftere naklet | Sistemin önerilen günlükleri otomatik olarak deftere nakletmesi gerekip gerekmeyeceğini seçin. Bu Günlükler, provizyonlar ve müşteri kesintileri için kullanılan günlük defterleri ve ayrıca satıcı vergi fatura günlüklerini içerir. |
| Serbest metin faturalarını otomatik olarak nakletme | Sistemin serbest metin faturalarını otomatik olarak deftere nakletmesi gerekip gerekmeyeceğini seçin. Bu seçenek yalnızca ödeme türü *vergi fatura müşteri kesintileri* olarak ayarlanan serbest metin faturalarına uygulanır. |
| İndirim maddesi sipariş referansı | İndirim işleminden oluşturulan satış siparişlerinde ve satın alma siparişlerinde (*hiçbiri*, *indirim yönetimi anlaşması*, *indirim yönetimi numarası*, *indirim hareket numarası* veya *belge notları*) kullanılacak indirim başvurusunu seçin. |
| Talep işlemini kullan | <p>Talepler işlemini kullanmak için bu seçeneği *Evet* olarak ayarlayın. Bu şekilde, indirim yönetiminin talep edilen veya talep edilmemiş olarak oluşturduğu işlemleri işaretleyebilir ve sonra yalnızca talep edilen işlemleri deftere nakledebilirsiniz.</p><p>Örneğin, bir aylık işlemlere ilişkin indirimleri hesaplıyorsunuz ancak müşteri iki günü talep etmemiş. Bu durumda, *işle* işlevini sonraki dönem için bir sonraki çalıştırmanızda talep edilmemiş işlemler yeniden oluşturulur.</p><p>Bu seçeneği *Hayır* olarak ayarlarsanız, tüm talep işlemleri nakledilir.</p> |
| Sipariş türü günlüğünü dahil et | İşlem türünün *Sipariş* olarak ayarlandığı anlaşmalar veya anlaşma satırları için Bu seçenek, *günlük* türünde bir satış siparişinin dahil edilip edilmeyeceğini denetler. Bir indirimin henüz uygulamamış olduğu senaryolarda bu tip siparişler kullanılıyorsa esneklik sağlar. |

## <a name="number-sequences-tab"></a>Numara serileri sekmesi

İndirim yönetiminin kullandığı farklı numara serilerine numara serisi kodları atamak için **indirim yönetimi parametreleri** sayfasındaki **numara serileri** sekmesini kullanın. Aşağıdaki tabloda bu numara serilerinin her birinin amacı açıklanmıştır. Numara serileri hakkında daha fazla bilgi için [Numara serilerine genel bakış](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) ve ilgili konularına bakın.

| Referans | Tanım |
|---|---|
| İndirim yönetimi anlaşması | Numara serisi, her indirim anlaşması için benzersiz bir anahtar değeri atar. Bu anahtar, anlaşmalar oluşturulduğunda kullanılır. |
| İndirim yönetimi numarası | Numara serisi, her indirim için benzersiz bir anahtar değeri atar. Bu anahtar indirim ilişkilerini tanımlamak için kullanılır. |
| İndirim işlem Numarası | Numara serisi, her indirim işlemi için benzersiz bir anahtar değeri atar. Bu anahtar indirim işlemlerini tanımlamak için kullanılır. |
| Vergi faturası | Numara serisi, her indirim faturası için benzersiz bir anahtar değeri atar. Bu anahtar, indirim günlükleri otomatik olarak deftere nakledildiğinde kullanılır. |

## <a name="feature-visibility-tab"></a>Özellik görünürlüğü sekmesi

İndirim yönetimi Microsoft Dynamics 365 Supply Chain Management'ta sık kullanılan birkaç sayfaya özellikler (alanlar ve işlevler) ekler. Bu sayfalar, satış siparişleri ve satış anlaşmaları ile ilgili sayfaları içerir. İndirim yönetimi kullanıyorsanız bu özelliklerden yararlanabilmeniz için bunları her yerde görünür hale getirmeniz gerekir. İndirim yönetimi kullanmıyorsanız özelliklerin sizi engellememesi için gizleyebilirsiniz.

**İndirim yönetimi parametreleri** sayfasının **Özellik görünürlüğü** sekmesinde, indirim yönetimi özelliklerini kullanılabilir oldukları her yerde görünür hale getirmek için **Etkinleştir** seçeneğini *Evet* olarak ayarlayın. **İndirim yönetimi** modülü dışındaki ortak sayfalarda gizlemek için *Hayır* olarak ayarlayın. Ancak seçenek *Hayır* olarak ayarlansa bile, **İndirim yönetimi parametreleri** sayfası da dahil olmak üzere modül, erişmek için uygun izinlere sahip kullanıcılar tarafından kullanılabilir olur.
