---
title: Muhasebe kaynağı gezgini
description: Bu makalede, genel muhasebe girişleri arkasındaki kaynak bilgilerinin ayrıntılı analizi için kullanabileceğiniz Muhasebe kaynağı gezgini sayfası hakkında bilgiler verilmektedir.
author: RyanCCarlson2
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806446"
---
# <a name="accounting-source-explorer"></a>Muhasebe kaynağı gezgini

[!include [banner](../includes/banner.md)]

Bu makalede, genel muhasebe girişleri arkasındaki kaynak bilgilerinin ayrıntılı analizi için kullanabileceğiniz **Muhasebe kaynağı gezgini** sayfası hakkında bilgiler verilmektedir.

**Muhasebe kaynağı gezgini** sayfası kaynak bilgilerini gösterir. Muhasebe kaynak gezginin, ister bir tek başına araç isterseniz de genel muhasebe defteri muhasebe girişleri arkasındaki ayrıntıları analiz etmek için bir araç olarak kullanabilirsiniz. Örneğin, sayfayı, Mizan içindeki bir bakiye veya fiş hareketindeki en ayrıntılı bilgiyi edinmek için kullanabilirsiniz. Ardından, bilgilerini Microsoft Excel programında ayrıntılı şekilde değerlendirmek (örneğin PivotTable raporu içinde veya üzerinde kullanmak) için **MS Excel'e Aktar** özelliğini kullanabilirsiniz.

**Muhasebe kaynağı gezgini** sayfası daima genel muhasebe hesabı için tutarı Genel defterde gösterildiği şekilde (örneğin Mizan) aynı olarak gösterir. Mizanda olduğu gibi segmentleri ayrı sütunlarda görüntüleyebilirsiniz. Sadece uygun mali boyut kümesini seçmeniz yeterlidir. 

Analiz için bir tarih aralığını tanımlamak için parametreleri kullanabilirsiniz. Bu işlev ayrıca Mizandaki işlevlere benzerdir.

Kaynak belge çerçevesini kullanan tüm belgeler için, **Muhasebe kaynak gezgini** sayfası, muhasebe dağılımlarına dayanarak ve mevcutsa, proje muhasebe dağılımlarına dayanarak ek bilgiyi gösterir. Bu bilgilere, **Parasal tutar türü**, **Proje**, **Faaliyet**, **Kategori** ve **Satır özelliği** değerleri dahildir. Burada, gerçekleştirebileceğiniz analizlere bazı örnekler verilmiştir:

- Satın alma emirleri ile satıcı faturaları arasındaki farklar, çünkü her bir fark örneğin masraf farkı vb. gibi bir parasal tutar türüyle temsil edilir
- Proje, ticari birim ve ana hesap başına faturalanabilir - faturalanamayan saatler ve masraflar karşılaştırması

Kaynak belgesi referans kimlikleri kavramını kullanan kaynak belgeler için, **Muhasebe kaynağı gezgini** sayfası örneğin **Müşteri**, **Satıcı**, **Çalışan**, **Ürün**, **Miktar**, **Birim metni** ve **Açıklama** değerleri gibi daha fazla ayrıntıyı gösterir. Burada, gerçekleştirebileceğiniz analizlere bazı örnekler verilmiştir:

- Bir mali dönem için maliyet raporlarına dayalı olarak ticari birim ve otel markası başına otel masrafları
- Satıcı, ürün, departman başına iskontolar

Bu belgeler için, **Muhasebe kaynağı gezgini** sayfasından ayrıca mevcut kaynak belgesine geçiş yapabilirsiniz.

> [!NOTE]
> Sürüm 10.0.31 itibariyle, Özellik yönetiminde yeni bir **Muhasebe kaynağı gezgini gelişmiş filtreleme** özelliği kullanıma sunulacaktır. Bu özellik, **Güncelleştir** düğmesinin yerini alır ve **Fiş hareketleri** sayfasında kullanılabilir olana benzeyen daha güçlü bir gelişmiş sorgu deneyimi sağlar. Gelişmiş filtre, **Fiş hareketleri sorgusu** sayfasında bulunanlara benzer alanları (**Genel muhasebe hesabı**, **İş birimi**, **Maliyet merkezi** ve **Departman** gibi) filtrelemenize olanak tanır. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
