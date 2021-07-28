---
title: Stok yenileme stratejileri
description: Bu konu, stok yenileme stratejileri hakkında bilgi sağlar ve stok yenilemenin nasıl yapılacağını seçmek için dalga talep stok yenileme şablon satırlarındaki Stok yenileme stratejisi alanını nasıl kullanabileceğinizi açıklar.
author: mirzaab
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: a8ddc7022a1e9a7db14aaa67efcd442025b0f9d8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344491"
---
# <a name="replenishment-strategies"></a>Stok yenileme stratejileri

[!include [banner](../includes/banner.md)]

**Stok yenileme şablonları** sayfasında tanımlanan şablonlar, stok yenilemenin nasıl yapılacağını seçmenize izin veren dalga talep stok yenileme şablonu satırlarını içerir. Her satır artık bir **Stok yenileme stratejisi** alanı içerir.

*Dalga talep miktarı* stratejisi varsayılan stratejidir. Bu, **Stok yenileme stratejisi** alanının başlatılmasından önce kullanılan stok yenileme stratejisidir. Stok yenileme yapılabilecek konumları bulmak için stok yenileme konumu yol tariflerini kullanır. Daha sonra talep karşılanana kadar bu konumlarda stok yenileme yapar.

*Maksimum konum kapasitesi* stratejisi bazı yeni işlevler sunar. *Dalga talep miktarı* stratejisi gibi, bu strateji stok yenileme yapılabilecek konumları bulmak için stok yenileme konumu yol tariflerini kullanır ve talep karşılanana kadar bu konumlarda stok yenileme yapar. Tüm stok yenileme yapılan konumların konum stoklama limitleriyle tanımlandığı şekilde maksimum kapasitelerine kadar stok yenileme yapılması açısından *Dalga talep miktarı* stratejisinden farklıdır. *Maksimum konum kapasitesi* stratejisi, stok yenileme yapılan konumları doldurmak için istenen miktarı ve biraz ekstra miktarı getirmek için iş oluşturmaya çalışır. Ancak bazı durumlarda, bu girişim başarısız olabilir. Örneğin, toplu konumlarda ek miktarı karşılamak için yeterli stok olmayabilir. Bu gibi durumlarda, sistem hata algılar ve kurtarma işlemi yapmaya çalışır.

Yoğun sezon, *Maksimum konum kapasitesi* stratejisinin *Dalga talep miktarı* stratejisi yerine tercih edildiği durumlara bir örnektir. Yoğun sezonda, bazı maddeler yüksek hacimde satılıyor olabilir. Bu nedenle, stok yenileme için oluşturulan iş kimliklerinin sayısını azaltmak üzere ilgili malzeme çekme konumlarını mümkün olduğunca proaktif olarak doldurmak isteyebilirsiniz.

> [!IMPORTANT]
> *Maksimum konum kapasitesi* stratejisinden tam olarak yararlanmak için ilgili konumlarda stoklama limitlerini yeniden tanımlamanız gerekir. Aksi takdirde, bu strateji *Dalga talep miktarı* stratejisi gibi çalışır.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Stoklama limitlerine göre Maksimuma kadar stok yenileme özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Stoklama limitlerine göre maksimuma kadar yenile*

## <a name="set-up-replenishment-strategies"></a>Stok yenileme stratejilerini ayarla

Şablonlara erişmek için **Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları**'na gidin. **Genel Bakış** bölümünde, **Stok yenileme türü** alanının *Dalga talep* olarak ayarlandığı bir dalga talep stok yenileme şablonu seçin veya oluşturun. Ardından, **Stok yenileme şablonu ayrıntıları** bölümünde stok yenileme şablonu satırlarını ayarlayın. Her satır için **Stok yenileme stratejisi** alanında, kullanmak istediğiniz stok yenileme stratejisini seçin.

![Stok yenileme şablonları sayfası.](media/ReplenTempWaveDmdMaxLocCap.png "Stok yenileme şablonları sayfası")

**Stok yenileme stratejisi** sütunu, **Stok yenileme şablonu ayrıntıları** bölümünde ızgarada görünmüyorsa, özelliğin açık olduğundan ve seçili stok yenileme şablonunda stok türü olarak *Dalga talep*'in bulunduğundan emin olun.

> [!NOTE]
> *Dalga talep miktarı* stratejisi varsayılan stratejidir. Bu nedenle, bunun yerine *Maksimum konum kapasitesi* stratejisini kullanmak istediğiniz stok yenileme şablonu satırlarını güncelleştirmeniz gerekir.

## <a name="example-scenarios"></a>Örnek senaryolar

### <a name="example-1"></a>Örnek 1

Bu örnekte, yalnızca bir stok yenileme şablon satırı olan yalnızca bir stok yenileme şablonu vardır.

A0001 maddesine ait 130 adetlik satış siparişi oluşturursunuz. Siparişi ambara serbest bırakmadan önce ambar aşağıdaki şekilde ayarlanır:

- Sadece bir toplu konum vardır ve eldeki stokta 500 adet vardır.
- Her biri 100 adetlik bir stoklama limitine sahip olan üç malzeme çekme konumu vardır. (*Maksimum konum kapasitesi* stratejisi için stoklama limitlerinin gerekli olduğunu unutmayın.)
- Stok yenileme yerine koyma konumları satış malzeme çekme konumları ile aynıdır.
- Stok yenileme birimi bir kutudur (1 kutu = 20 adet).

Sipariş sırasında, satış malzeme çekme konumlarında aşağıdaki stok eldedir:

- **Çekme-001:** 20 adet (1 kutu)
- **Çekme-002:** 0 adet
- **Çekme-003:** 0 adet

Başlangıçta, stok yenileme stratejisi *Dalga talep miktarı* olarak ayarlanır.

Satış siparişini ambara serbest bıraktıktan ve dalga işleme dalga için çalıştırıldıktan sonra aşağıdaki stok yenileme işini alırsınız:

- **Stok yenileme işi 1:** Toplu konumdan 4 kutu çekin ve bunları çekme-001 konumuna koyun.
- **Stok yenileme işi 2:** Toplu konumdan 2 kutu çekin ve bunları çekme-002 konumuna koyun.

İki konumda stok yenileme yapmanız gerektiği için iki stok yenileme işi kimliği edinebilirsiniz ve çoklu konumlar desteklenmez.

Bunun yerine stok yenileme stratejisini *Maksimum konum kapasitesi* olarak ayarlarsanız aşağıdaki stok yenileme işini alırsınız:

- **Stok yenileme işi 1:** Toplu konumdan 4 kutu çekin ve bunları çekme-001 konumuna koyun.
- **Stok yenileme işi 2:** Toplu konumdan 5 kutu çekin ve bunları çekme-002 konumuna koyun.

[![Örnek 1.](media/ReplenTemp_example_1.png "Örnek 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>Örnek 2

Bu örnek, toplu konumun fazladan miktarı karşılamak için yeterli stoğa sahip olmaması durumunda neler olacağını gösterir. Örnek 1 ile aynı senaryoyu kullanır, ancak toplu konumda 160 adet (8 kutu) vardır.

*Dalga talep miktarı* stratejisi, örnek 1'de oluşturduğu aynı işi oluşturur.

Ancak *Maksimum konum kapasitesi* stratejisi, örnek 1'de olduğu gibi iş kimliklerini oluşturmaya çalıştığından başarısız olabilir. Bu noktada, sistem kurtarma işlemi yapmaya çalışır.

Stok yenileme malzeme çekme için konum yönergelerindeki **Bölmeye izin ver** seçeneğinin ayarına bağlı olarak iki sonuç mümkündür:

- **Bölmeye izin ver** seçeneği *Evet* olarak ayarlanırsa aşağıdaki stok yenileme işi oluşturulur:

    - **Stok yenileme işi 1:** Toplu konumdan 4 kutu çekin ve bunları çekme-001 konumuna koyun.
    - **Stok yenileme işi 2:** Toplu konumdan 4 kutu çekin ve bunları çekme-002 konumuna koyun.

- **Bölmeye izin ver** seçeneği *Hayır* olarak ayarlanırsa aşağıdaki stok yenileme işi oluşturulur:

    - **Stok yenileme işi 1:** Toplu konumdan 4 kutu çekin ve bunları çekme-001 konumuna koyun.
    - **Stok yenileme işi 2:** Toplu konumdan 2 kutu çekin ve bunları çekme-002 konumuna koyun.

Sonuç, işi oluştururken kullanılabilen bilgiler nedeniyle farklıdır. **Bölmeye izin ver**, stok yenilemede malzeme için konum yönergelerinde *Evet* olarak ayarlandığında, 160 adet bulduğunuzdan emin olursunuz. Bu nedenle, bu miktar için iş oluşturabilirsiniz. Ancak **Bölmeye izin ver** seçeneği *Hayır* olarak ayarlandığında, 160 adetin mevcıt olup olmadığını bilemezsiniz. Stok yenilemek için kullanacağınız ekstra miktar 3 kutu olduğundan, bu ekstra miktarı düşürür ve orijinal miktarı yeniden denersiniz.

[![Örnek 2.](media/ReplenTemp_example_2.png "Örnek 2")](media/ReplenTemp_example_2_large.png)

Bu nedenle, stok yenileme yapılan konumlara maksimum miktarı almak için stok yenilemede malzeme çekme için konum yönergelerinde **Bölmeye izin ver** seçeneğini *Evet* olarak ayarlamanız gerekir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]