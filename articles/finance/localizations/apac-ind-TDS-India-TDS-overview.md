---
title: Hindistan Kaynakta Kesilen Vergi'ye (TDS) genel bakış
description: Bu konu, Hindistan Kaynakta Kesilen Vergi (TDS) hakkında ayrıntılı bilgiler sağlar. TDS belgeleri, bu özelliğin işlevselliğini kapsamaktadır.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 8064f10978712fc474dd72a5b5bdd9a445606d7a
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337733"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Hindistan Kaynakta Kesilen Vergi'ye (TDS) genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, Hindistan Kaynakta Kesilen Vergi (TDS) hakkında ayrıntılı bilgiler sağlar.

TDS belgeleri, bu özelliğin işlevselliğini kapsamaktadır. Ayrıca, TDS için temel kurulum yapma, hareketlerde TDS hesaplama, TDS kapatma işlecini tamamlama, TDS sertifika numaralarını kaydetme ve TDS sorguları, TDS deyimleri ve TDS sertifikaları oluşturma gibi konuları açıklar. Belgeler, aşağıdaki konuları içerir:

- [TDS için temel kurulum](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [TDS hesaplaması için kullanılan formül tasarımcısı ve eşik sınırı işlevi](apac-ind-TDS-Formula-designer.md)
- [Faturalardaki, ödemelerde, senetlerde ve şirketlerarası hareketlerde TDS hesaplanması](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Dönemsel TDS kapatma işlemi ve TDS tutarlarının TDS yetkili satıcılarına kapatılması](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [TDS sertifika numaraları ve tarihlerini kaydetme ve güncelleştirme](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>TDS'ye giriş

1961 tarihli Gelir Vergisi Kanunu'na göre vergiler, hizmeti alan kişi tarafından avans ödemesi veya alacağın muhasebesi (hangisi önce gerçekleşirse) sırasında kaynakta kesilir. Ödemeyi yapan kişi, vergi tutarını düşmeli ve yalnızca net bakiyeyi servis sağlayıcısına ödemelidir. TDS, devlet tarafından belirtilen hizmetlere uygulanır ve devletin bir dönem için belirttiği oranlar kullanılarak kesilir. Kesinti oranı, ödemeyi alan veya servisi sağlayan varlığın durumuna bağlıdır. Durumlar arasında şunlar yer alır: **Bağımsız**, **Hindu Bölünmemiş Aile** (**HUF**), **Şirket**, **Firma**, **Kişiler İştirakı** (**AOP**) **Kişiler Kuruluşu** (**BOI**) ve **Yerel makamlar**.

Aşağıdaki bölümlerde, Hindistan Hükümeti tarafından belirtildiği şekilde, TDS'nin uygulandığı hizmetler listesi verilmiştir.

**Yerleşik olanlar**

- Maaşlardan edilen gelir (Bölüm 192 altında)
- Menkul kıymet faizlerinden edilen gelir (Bölüm 193 altında)
- Temettülerden edilen gelir (Bölüm 194 altında)
- Faizden edilen gelir (Bölüm 194A altında)
- Şans oyunları veya bilmecelerden edilen gelir (Bölüm 194B altında)
- At yarışı vb. oyunlardan edilen gelir (Bölüm 194BB altında)
- Yükleniciler ve alt yükleniciler (Bölüm 194C altında)
- Sigorta komisyonu (Bölüm 194D altında)
- Ulusal tasarruf şeması altında yer alan depozitodan edilen gelir (Bölüm 194EE altında)
- Yatırım fonu veya UTI'den edilen gelir (Bölüm 194F altında)
- Satış veya şans oyunlarında Komisyon, Karşılık, Ödül vb. (Bölüm 194G altında)
- Komisyon veya aracılık ödemesi (Bölüm 194H altında)
- Kira (Bölüm 194I altında)
- Profesyonel hizmet (Bölüm 194J altında)
- Birimlerden edilen gelir (Bölüm 194K altında)
- Belirli gayrimenkul malın edinmesiyle ilgili ücret ödemesi (Bölüm 194LA altında)

**Yerleşik olmayanlar**

- Yerleşik olmayan sporculara veya spor birliklerine ödemeler (Bölüm 194E altında)
- Diğer toplamlar (Bölüm 195 altında)
- Yerleşik olmayan birimlerden edilen gelir (Bölüm 196A altında)

    - Yabancı para birimi tahvilleri veya Hint şirketi hisselerinden edilen gelir (Bölüm 196C altında)
    - Menkul değerlerin yabancı kurumsal yatırımlarından edilen gelir (Bölüm 196D altında)
    - Doğrudan gelirler altındaki maaş ve diğer tüm pozitif gelirler (Bölüm 192)
    - Menkul kıymetlerin faizi (Bölüm 193)
    - Menkul kıymet faizleri dışındaki faizler (Bölüm 194A)
    - Yükleniciler ve alt yüklenicilere ödemeler (Bölüm 194C)
    - Şans oyunları veya bilmecelerden kazanılanlar (Bölüm 194B)
    - At yarışı oyunlardan kazançlar (Bölüm 194BB)
    - Sigorta işinin tedariği için tüm ödemeleri kapsayan Sigorta Komisyonu (Bölüm 194D)
    - Şirket olmayan yerleşik olmayanlara veya yabancı bir şirkete menkul kıymet faizi dışında ödenecek faizler (Bölüm 195)
    - Yerleşik olmayan sporculara (spor birliği veya kuruluşu dahil) ödeme. Yerleşik olmayan sporcular söz konusu olduğunda Hint gazeteleri, dergileri ve benzeri yerlerde yayınlanması için oyun/sporlarla ilgili reklam ve yazı ödemeleri. dahil edilir (Bölüm 194E)
    - NSS \[Ulusal Tasarruf Şeması \] altında depozitolarla ilgili ödeme (Bölüm 194EE)
    - Yatırım Fonu veya UTI tarafından Birimlerin tekrar satınalımıyla ilgili ödeme (Bölüm 194F)
    - Komisyon veya aracılık ödemesi (Bölüm 194H)
    - Kira ödemesi (Bölüm 194I)
    - Profesyonel veya teknik servisler için ödenen ücretler (Bölüm 194J)
    - İlgili biletlerin karşılığı veya ödülleri dahil olmak üzere Şans oyunları biletlerinin Stokçularına, dağıtımcılarına, alıcılarına ve satıcılarına komisyon (Bölüm 194G)
    - Yabancı para birimi cinsinden satın alınan Birimlerden edilen gelir ve yabancı para birimi cinsinden satın alınan bu tür Birimlerin transferinden kaynaklanan uzun vadeli sermaye kazancı (Bölüm 196B)
    - Tahviller ve hisselerdeki faiz veya temettülerle ilgili olarak yerleşik olmayanlara ödenen tüm gelirler (Bölüm 196C)

TDS; satınalmalar, satış, satış iadeleri, kredi notları, sabit kıymet alımları, peşinatlar, avans ödemeleri, senetler, çalışma vergisi ve şirketlerarası hareketler üzerinde hesaplanır.

> [!NOTE]
> Geçerli Hindistan vergi senaryosunda, TDS satış hareketlerinde hesaplanmaz. Ancak sistem, özellikle şirketlerarası hareketler için satış hareketlerinde de TDS düşürülebilirlerinin hesaplanması için bir provizyon içerir.

TDS hesaplaması her zaman, TDS bileşeni için tanımlanan eşik ve istisna eşiğini dikkate alır.

Dönemsel TDS kapatma işlemi çalıştırılmalıdır ve TDS ödemeleri, TDS yetkili satıcılarına kapatılmalıdır.

Satıcılardan veya müşterilerden alınan TDS sertifikalarının sertifika numaraları ve tarihleri kaydedilebilir ve güncelleştirilebilir. Ek olarak, Form 26Q ve Form 27Q üç aylık ekstreleri ve TDS ile ilgili Form 16A Finance'de oluşturulabilir.

## <a name="setting-up-and-working-with-tds"></a>TDS'yi kurma ve TDS'yle çalışma

TDS kurulumu ve TDS'yle çalışma sürecine genel bakış:

1. **TDS kurulumu:**

    - Parametre kurulumu:

        - Genel muhasebe parametrelerinde, TDS ile ilgili parametreleri etkinleştirin.
        - Genel muhasebe parametrelerinde, stopaj vergisi ödemelerinin numara sırasını ayarlayın.
        - Borç hesapları ve Alacak hesaplarında parametreleri ayarlayın.

    - Temel kurulum:

        - Bir şirket, müşteriler ve satıcılar için TDS kayıt numaralarını ayarlayın.
        - TDS bileşeni gruplarını ayarlayın.
        - TDS bileşenlerini ayarlayın, bunlara TDS bileşen gruplarını iliştirin ve bunlar için eşiği ve istisna eşiğini tanımlayın.
        - TDS yetkililerini ayarlayın.
        - TDS kapatma dönemlerini ayarlayın.
        - TDS vergi kodlarını ayarlayın ve bunlara TDS bileşenlerini iliştirin.
        - TDS vergi gruplarını ayarlayın ve bunlara TDS vergi kodlarını iliştirin.
        - Formül tasarımcısında, TDS grubu için TDS hesaplamasını yapmak üzere bir formül tanımlayın.
        - TDS imtiyaz sertifikası numaralarını kaydedin.

    - Genel muhasebe hesapları ve şirket kurulumu:

        - TDS alacak ve borç genel muhasebe hesapları kurma:
        - Şirket için bir Vergi Kesintisi ve Tahsilat Hesap Numarası (TAN) ile bir kesinti türü kategorisi ayarlayın.

    - Diğer kurulum:

        - TDS tahsisatını içeren bir ödeme planı ayarlayın.
        - TDS yetkilisine yapılacak ödemeler için bir ödeme ücreti türü ayarlayın.
        - Satıcı ve müşteriler için TDS grupları, kalıcı hesap numaraları (PAN'lar) ve için TAN'lar ile ilgili bilgileri ayarlayın.

2. **Hareketlerde TDS hesaplaması:**

    - Faturalar ve ödemeler
    - Senetler
    - Avans ödemeleri
    - Ön ödemeler

3. **TDS kapanışı.**

    - Dönemsel TDS kapatma işlemi
    - TDS yetkili satıcılarına TDS ödemelerinin kapatılması ve TDS irsaliyesi oluşturma

4. **TDS sorguları, deyimleri ve sertifikaları:**

    - TDS sertifika numaraları ve tarihlerini kaydedin ve güncelleştirin.
    - TDS sorgusu ve deftere nakledilmiş TDS sorgusu oluşturun.
    - Form 27A, Form 26q ve Form 27Q TDS ve e-TDS üç aylık ekstreler oluşturun.
    - Form 16A TDS sertifikası oluşturun.
