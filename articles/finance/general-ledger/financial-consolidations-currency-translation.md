---
title: Mali konsolidasyonlar ve para birimi dönüştürmeye genel bakış
description: Bu konuda, genel muhasebede mali konsolidasyonlar ve para birimi çevirme açıklanır.
author: aprilolson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 87bb31d6456356342773f38699a412aa72ea458e
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193917"
---
# <a name="financial-consolidations-and-currency-translation-overview"></a>Mali konsolidasyonlar ve para birimi dönüştürmeye genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, hem Microsoft Dynamics 365 Finance hem de Finansal raporlamada birleştirmeler için kullanılan yaklaşımı size açıklar. Birden fazla şirket raporlamasını, toplamasını, eliminasyonunu ve azınlık hissesini içeren senaryoları tanımlar. Ayrıca tüzel kişiliklerin farklı mali dönemlere veya hesap planlarına sahip olduğu senaryolar gibi özel durumların nasıl yönetileceğini açıklar.

Bu konu, kullanıcılar ve işlev danışmaları için yazılmıştır. Okuyucuların Finance ve Mali raporlama hakkında genel bilgi sahibi olduklarını varsayar. Temel kurulum açıklanmaz.

> [!NOTE]
> *Tüzel kişilik* terimi, Finance'ta kullanılır ve *şirket* terimi Mali raporlamada kullanılır. Bu konuda her iki terim de kullanılır. Ancak bu konunun amaçları açısından anlamları aynıdır.

## <a name="audience"></a>Hedef Kitle
Bu konu birden fazla şirket ve birden fazla para birimi verilerini konsolide etmek için Finance and Reporting ve Mali raporlamayı kullanmak isteyen finans ve muhasebe kullanıcıları ve uygulama danışmanları içindir.

## <a name="approach"></a>Yaklaşım
Finance konsolidasyon işlemi için ayrı bir tüzel kişilik kullanır. Tek örnek konsolidasyona olanak tanır ama diğer kaynaklardaki verileri getirmek için bir seçenek sunar. Konsolidasyon işlemi, kaynak tüzel kişilikte değişikliklerin yapıldığı tüm zamanlarda çalıştırılmalıdır.

Mali raporlama, rapor oluşturma sırasında birden fazla şirketi konsolide edebilir. Veriler bir veri reyonunda depolanır, sürüm oluşturulur ve dışarı aktarılabilir; ancak kaynak şirket, verilerin sahibi ve konteyneridir. Rapor herhangi bir zamanda, hatta (örneğin) her dakika çalıştırılabilir. Tüm şirketler ve boyutlar için detaya gitme yeteneği gibi birçok ek kazanç sağlar.

Kullanıcılar; Çevrimiçi Olarak Konsolide Et, Mali raporlama veya ikisini bir arada kullanabilir. Seçim, şirketin ihtiyaçlarına ve denetçilerin tercihlerine bağlıdır.

## <a name="consolidations"></a>Konsolidasyonlar
**Konsolidasyonlar** modülü, konsolidasyon işlemi sırasında birden fazla tüzel kişiliği konsolide etme ve şirket bakiyesini içe veya dışa aktarma seçeneklerini içerir. Ayrıca eliminasyonları ayarlayabilir ve eleme günlüklerini deftere nakledebilirsiniz.

## <a name="benefits-of-using-consolidate-online"></a>Çevrimiçi olarak konsolide et özelliğini kullanmanın avantajları
**Konsolidasyonlar** modülünü kullanan müşteriler çeşitli avantajlar elde eder:

- **Veri derinliği**: Hem hesap düzeyinde hem boyut düzeyinde fiili verileri ve bütçe verilerini bir araya getiren konsolide raporlar oluşturabilirsiniz.
- **Dinamik konsolidasyonlar**: Konsolidasyonlar birden fazla kez işlenebilir.
- **Denetim yetenekleri**: Boyutlar ve hesaplar, analiz ve denetim için tutulur ve bakiyeler tarihe göre oluşturulur.
- **Para birimi çevirme**: Kaynak şirketin muhasebe para biriminden konsolidasyon şirketinin muhasebe para birimine dönüştürmek için hesap aralıkları ve oranlarını oluşturabilirsiniz.
- **Konsolide veya eliminasyon şirketinde işlem eliminasyonları**: Konsolidasyon sırasında tek bir işlem olarak eliminasyonları işleyebilir ve deftere nakledebilirsiniz. Alternatif olarak, bir teklifi ayrı olarak çalıştırabilirsiniz.

## <a name="supported-consolidation-scenarios"></a>Desteklenen konsolidasyon senaryoları
Çevrimiçi olarak konsolide et özelliğinin desteklediği konsolidasyon senaryolarından bazıları:

- Tüzel kişilikler arasındaki tek düzeyli konsolidasyonlar
- Elemeleri içeren konsolidasyonlar
- Azınlık hissesi (Bu senaryo için şirkette el ile hesaplama ve giriş kullanılmalıdır.)
- Tüzel kişilikler arasındaki birden fazla hesap planları
- Birden fazla tüzel kişilik arasındaki farklı mali takvimler
- Birden fazla raporlama para birimi içeren konsolidasyonlar

## <a name="legal-entity-setup"></a>Tüzel kişilik kurulumu
Bir konsolidasyonu işlemeden önce tüzel kişiliği ayarlamanız gerekir. Konsolidasyonu ihtiyacınız olduğu sayıda çalıştırabilirsiniz ve tüm veriler kaynak şirketin muhasebe para biriminden konsolidasyon şirketi için tanımlı para birimine dönüştürülür. Bu nedenle aşağıdaki organizasyon yapısı için, tüm Kuzey Amerika şirketlerini önce ABD dolarına (USD) ve sonra ana şirketin para birimi olan avroya (EUR) dönüştürmek zorundaysanız en az iki konsolidasyon şirketiniz olmalıdır.

![Kuruluş yapısı](./media/organizational-structure.png "Kuruluş yapısı")

Önceki organizasyon yapısında Kuzey Amerika konsolidasyonu için bir tüzel kişiliğe sahip olmalısınız çünkü konsolidasyonlar daima kaynak şirketin muhasebe para biriminden konsolidasyon şirketinin para birimine konsolide edilir. Örnek olarak tüm şirketler tek bir konsolidasyona dahilse Meksika'daki yan kuruluş Meksika pesosunu (MXN) USD'ye ve sonra EUR'ye değil, doğrudan EUR'ye dönüştürür.

Tüzel kişiliği oluştururken şirketin konsolidasyon işlemiyle eliminasyon işleminin her ikisi için mi yoksa bu işlemlerden sadece birisi için mi kullanılacağını belirtebilirsiniz. Aşağıdaki çizimde şirket her iki işlem için kullanılmaktadır. Konsolidasyon şirketinde günlük defterleri nakledemeyeceğinizi ancak onları bir eliminasyon şirketinde deftere nakledebileceğinizi unutmayın. Bu nedenle farklı bir eliminasyon şirketinizin olmasını isteyebilirsiniz.

![Hem konsolidasyon hem de eleme için kullanılan tüzel kişilik](./media/sep-elimination-company.png "Hem konsolidasyon hem de eleme için kullanılan tüzel kişilik")

## <a name="main-accounts-and-consolidation-account-groups"></a>Ana hesaplar ve konsolidasyon hesabı grupları
Yapmanız gereken seçim, hesap planlarınızı nasıl konsolide etmek isteyeceğinizdir. Konsolidasyon işlemi sırasında ana hesapları konsolide etmek için üç seçeneğiniz vardır.

İlk seçenek, ana hesapları kaynak şirketlerden kullanmaktır. Bu durumda tüm şirketlerden gelen her hesap konsolide edilir. Örneğin nakit, USMF şirketinde 100000 hesabı ve DEMF şirketinde 1100 hesabıysa konsolidasyon şirketi her iki hesabı da dahil eder. Her hesabın kendi bakiyesi olur.

İkinci seçenek, **Ana hesaplar** sayfasında bir varsayılan konsolidasyon hesabı belirtmektir. Böylece hesap, konsolidasyon hesabına eşlenir. Bu seçenek farklı hesap planlarına sahip olduğunuzda veya genel merkez tarafından tanımlanan bir şemaya eşlemek zorunda olduğunuzda yararlı olabilir.

![Ana hesaplar sayfasında belirtilen varsayılan konsolidasyon hesabı](./media/main-accounts.png "Ana hesaplar sayfasında belirtilen varsayılan konsolidasyon hesabı")

Üçüncü seçenek, konsolidasyon hesabı gruplarını kullanmaktır. İhtiyacınız kadar sayıda konsolidasyon hesabı grubu tanımlayabilirsiniz. Ardından, **İlave konsolidasyon hesapları** sayfasında sadece ana hesabı hesap planından bu grupta ihtiyacınız olan hesaba eşlersiniz.

![İlave konsolidasyon hesapları sayfasında eşleme](./media/additional-consolidation-accounts.png "İlave konsolidasyon hesapları sayfasında eşleme")

## <a name="consolidating-online"></a>Çevrimiçi olarak konsolide etme
Konsolidasyon bilgilerinin çevrimiçi olarak nasıl girildiğini öğrenmek için bkz. [Çevrimiçi mali konsolidasyonlar](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Konsolidasyon hareketlerini yönetme
Konsolidasyon sonuçlarını görüntülemek için birden fazla seçeneğiniz vardır:

- Konsolidasyon şirketine dair mali rapor oluşturun.
- Konsolidasyon şirketinde **Mizan** listesi sayfasını gözden geçirin.
- **Konsolidasyonlar** sayfasındaki konsolidasyon hareketleri listesinde, her dönemde her kaynak şirket için tarihe göre oluşturulan bakiyeleri görüntüleyin.

    ![Konsolidasyonlar sayfasındaki konsolidasyon hareketleri](./media/managing-consolidation-transactions.png "Konsolidasyonlar sayfasındaki konsolidasyon hareketleri")

Konsolidasyonu tekrar çalıştırmak için konsolidasyonu işlemeniz yeterlidir. Alternatif olarak, önce **Konsolidasyonlar** sayfasındaki **Hareketleri kaldır**'ı seçebilirsiniz.
Konsolide hesabınızdaki bakiyeler doğru değilse, bu bakiyeler **Kapanış dönemi ayarlamaları** sayfası kullanılarak düzeltilebilir.

## <a name="consolidate-with-import"></a>İçe aktarmayla konsolide et
İçe aktarmayla konsolide et işlevi, Çevrimiçi olarak konsolide et işlevi gibi çalışır. Tüzel kişilikleri seçerken, verileri içeren kaynak dosya dışına göz atarsınız.

## <a name="export-company-balances"></a>Şirket bakiyelerini dışa aktar
Şirket bakiyelerini dışa aktar işlevi de Çevrimiçi olarak konsolide et işlevi gibi çalışır. Tüzel kişilikleri seçerken çıktı için bir dosya yolu ayarlarsınız.

## <a name="elimination-rules"></a>Eleme kuralları
Şirketlerarası hareketleri elemek için bir eliminasyon kuralı oluşturabilirsiniz. Alternatif olarak, eliminasyon şirketi olarak belirlenen bir şirkette el ile eliminasyon girişi yapabilirsiniz. Bir eliminasyon kuralı oluşturursanız eliminasyon yöntemi için iki seçeneğiniz vardır: **Net değişiklik** ve **Sabit**.

### <a name="set-up-elimination-rules"></a>Eliminasyon kurallarını ayarlama
Finance'ta eliminasyon kuralları ayarlarken özel olarak eliminasyon için kullanılan bir mali boyut oluşturabilirsiniz. Müşterilerin çoğu bu mali boyuta **Ticari Ortak** veya benzer bir ad verir. Bir mali boyutu kullanmamaya karar verirseniz sadece şirketlerarası hareketler için kullanılan ana hesaplara sahip olacağınızı unutmayın.

Eliminasyonlar için ayarlamayı **Konsolidasyonlar** modülünün **Ayarlama** alanında bulabilirsiniz. Bir kural için açıklama girdikten sonra eleme günlüğünün deftere nakledileceği şirketi seçmeniz gerekir. Seçtiğiniz şirket, tüzel kişilik ayarlamasında **Mali eliminasyon işlemi için kullan** seçeneğinin işaretlenmiş olduğu bir şirket olmalıdır.

Eliminasyon kuralı etkin olduğunda ve tarih sona erdiğinde tarihi ihtiyaç duyduğunuz şekilde ayarlayabilirsiniz. Eliminasyon teklifi işleminde eliminasyon kuralının mevcut olmasını istiyorsanız **Etkin** seçeneğini **Evet** olarak ayarlamanız gerekir. **Eleme** türünün günlük adını seçin.

![Eliminasyon kuralının temel özellikleri](./media/ledger-elimination-rule-journal.png "Eliminasyon kuralının temel özellikleri")

Temel özellikleri tanımladıktan sonra fiili işleme kurallarını tanımlamak için **Satırlar**'ı seçin. Eliminasyonlar için iki seçenek vardır: Net para üstü tutarını elimine edebilir veya sabit bir tutar tanımlayabilirsiniz.

Kaynak hesaplarını seçin. Joker karakter olarak bir yıldız (\*) kullanabilirsiniz. Örneğin **1\**_, tahsisat için veri kaynağı olarak _* 1** ile başlayan tüm hesapları seçer.

Kaynak hesapları seçtikten sonra hedef şirketten kullanılan hesabı belirtmek için **Hesap belirtimi** alanını kullanın. Kaynak hesabında tanımlanan aynı ana hesabı kullanmak için **Kaynak**'ı seçin. **Kullanıcı tanımlı**'yı seçerseniz bir hedef hesap belirtmeniz gerekir.

![Genel muhasebe eliminasyon kuralı satırı sayfası](./media/ledger-elimination-rule-line.png "Genel muhasebe eliminasyon kuralı satırı sayfası")

**Boyut belirtimi** alanı, **Hesap belirtimi** alanı gibi çalışır. Hedef şirkette ve kaynak şirkette aynı boyutları kullanmak için **Kaynak**'ı seçin. **Kullanıcı tanımlı**'yı seçerseniz **Hedef boyutları**'nı seçerek hedef şirketteki boyutları belirtmeniz gerekir. Ardından, kaynak boyutlarını ve eliminasyon kaynağı olarak kullanılan mali boyutlar ile değerleri seçin.

### <a name="process-elimination-transactions"></a>Eliminasyon hareketlerini işleme koy
Eliminasyon hareketlerini işlemenin iki yolu vardır. Hareket, Çevrimiçi olarak konsolide et işlemi sırasında işlenebilir veya bir eleme günlüğü oluşturabilir ve eliminasyon teklifi işlemini çalıştırabilirsiniz. Bu bölüm ikinci seçenek üzerinde odaklanır.

Eliminasyon şirketi olarak tanımlanan bir şirkette **Konsolidasyonlar** modülünde **Eleme günlüğü**'nü seçin. Günlük adını seçtikten sonra **Satırlar**'ı seçin. Teklifi çalıştırmak için **Teklifler** \> **Eliminasyon teklifi**'ni seçin.

Konsolide edilen verilerin kaynağı olan şirketi seçin ve ardından işlemek için kuralı seçin. Eliminasyon tutarları için aranan tarih aralığını tanımlamak isterseniz başlangıç ve bitiş tarihlerini girin. **GM deftere nakil tarihi** alanı, genel muhasebe için günlüğü deftere nakletmek üzere kullanılan tarihi belirtir. **Tamam**'ı seçtikten sonra tutarları gözden geçirebilir ve günlüğü deftere nakledebilirsiniz.

> [!NOTE]
> Eleme günlüğü, muhasebe para birimindeki değil, orijinal hareketlerin para birimindeki hesap değerleri için tutarları gösterir. Eleme günlüğündeki tutarları gözden geçirirken bu davranışı kafa karıştırıcı bulabilirsiniz.

Daha fazla bilgi ve örnekler için bkz. [Eliminasyon kuralları](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Konsolidasyon şirketinde para birimi yeniden değerleme
Bir muhasebe para biriminden diğerine veri konsolide ederken döviz kurları değişirse para birimi yeniden değerleme işlemini hala çalıştırmanız gerekir, böylece hesap bakiyeleriniz doğru biçimde yeniden değerlenir. Başlangıçta verileri konsolide ederken konsolidasyon işlemi sırasında dönüştürme için kullanılması gereken ilk döviz kurlarını seçmek için **Para birimi çevirme** sekmesini kullanın. Yeni bir döviz kuru (örneğin, gelecek ay içinde) girildikten sonra hesap bakiyelerini yeniden değerlemek gerekir. Gerçekleşmemiş kazançlar veya zararlar sonrasında yeni döviz kuruna ve tarihe göre güncelleştirilir.

Bir konsolidasyon şirketinde para birimi yeniden değerleme işlemi hakkında daha fazla bilgi için bkz. [Bir konsolidasyon şirketinde para birimi yeniden değerleme işlemi](currency-revaluation-consolidation-company.md).

**Genel muhasebe** modülünde para birimi yeniden değerleme işleminin nasıl çalıştığı hakkında daha fazla bilgi için bkz. [Genel muhasebe için yabancı para birimi yeniden değerleme işlemi](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Ek bilgi
- Konsolidasyon işlenirken tüm deftere nakil katmanları konsolide edilir.
- Eleme günlükleri sadece geçerli katman için deftere nakledilebilir.
- Sadece işletim bakiyeleri konsolide edilir. Bu nedenle açılış bakiyelerini görmek için konsolidasyon şirketinde hala bir yıl sonu kapanışı çalıştırmanız gerekir.
- Günlüğü bir konsolidasyon şirketinde değil, eliminasyon şirketinde deftere nakledebilirsiniz.
- Bir konsolidasyon şirketinde bakiyelerin ayarlamaları yalnızca **Kapanış dönemi ayarlamaları** sayfası kullanılarak yapılabilir. 

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Mali konsolidasyonlar ve para birimi çevirme için Mali raporlamayı kullanma veya konsolide raporlama için Çevrimiçi olarak konsolide etmeyi tamamlamayı avantajları
Mali konsolidasyonlar ve para birimi çevirme için Mali raporlamayı veya konsolide raporlama için Çevrimiçi olarak konsolide etmeyi tamamlamayı kullanan müşteriler çeşitli kazançlar sağlar:

- **Veri derinliği**: Hem hesap düzeyinde hem boyut düzeyinde fiili verileri ve bütçe verilerini bir araya getiren konsolide raporlar oluşturabilirsiniz. Finance için bu veriler hem bütçe kontrolü hem bütçe planlamasından gelen verileri içerir.
- **Dinamik konsolidasyonlar**: Konsolidasyonlar. kuruluş hiyerarşisinde herhangi bir zamanda ve herhangi bir düzeyde yapılabilir.
- **Tam denetim yetenekleri**: Analiz ve denetim için tüm boyutlar, hesaplar ve hareket detayı tutulur. Buna ek olarak Mali raporlama, konsolide edilen herhangi bir tüzel kişilikteki orijinal hareket için tam detaya gitme sağlar.
- **Kolaylaştırılmış para birimi çevirme**: Finance'ta minimum ayarlamadan sonra herhangi bir Mali raporlama raporunu ayarlanan herhangi bir raporlama para birimine dönüştürebilirsiniz. Buna ek olarak sınırsız sayıda raporlama para birimi ayarlayabilirsiniz.
- **Kaynakta eliminasyonları deftere nakletme**: Eliminasyon hareketlerini doğrulamak için bir eliminasyon raporu oluşturabilir ve yazdırabilirsiniz. Böylece standart şirketlerarası hareketler olarak yeni eliminasyonları deftere nakledebilirsiniz. Tüzel kişiliğinizde istemediğiniz herhangi bir hareket için bir eliminasyon tüzel kişiliği de kullanabilirsiniz.

## <a name="supported-consolidation-scenarios-for-financial-reporting"></a>Financial Reporting için desteklenen konsolidasyon senaryoları

Mali raporlamanın desteklediği konsolidasyon senaryolarından bazıları:

- Tüzel kişilikler arasındaki tek düzeyli ve birden fazla düzeyli konsolidasyonlar
- Tüzel kişilikten oluşturulan kuruluş yapılarını kullanan konsolidasyonlar
- Elemeleri içeren konsolidasyonlar
- Azınlık hissesi
- Tüzel kişilikler arasındaki birden fazla hesap planları
- Birden fazla tüzel kişilik arasındaki farklı mali takvimler
- Birden fazla raporlama para birimi içeren konsolidasyonlar
- İş birimi konsolidasyonları

## <a name="generating-consolidated-financial-statements"></a>Konsolide mali tabloları oluşturma
Konsolide mali tabloları oluşturabileceğiniz senaryolar hakkında bilgi için bkz. [Konsolide mali tabloları oluşturma](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]