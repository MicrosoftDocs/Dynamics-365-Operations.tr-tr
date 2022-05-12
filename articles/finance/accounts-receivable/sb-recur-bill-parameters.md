---
title: Yinelenen sözleşme faturalama parametreleri
description: Bu konu, Yinelenen sözleşme faturalaması için oluşturulan ödeme zamanlamalarına yönelik varsayılan değerlerin nasıl ayarlanacağını açıklar. Ayrıca, fatura zamanlama gruplarının nasıl oluşturulduğu da açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 4c52095aa49962cbfc577faf71ab0d71929a386b
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629446"
---
# <a name="recurring-contract-billing-parameters"></a>Yinelenen sözleşme faturalama parametreleri

Yinelenen sözleşme faturalaması için oluşturulan faturalama zamanlamalarının varsayılan değerlerini ayarlamak için **Yinelenen sözleşme faturalama parametreleri** sayfasını kullanın. Oluşturduğunuz tüm fatura zamanlamaları, başlangıçta bu varsayılan değerleri kullanır. Ancak, her faturalama planı için gerekli değerleri gerektiği gibi değiştirebilirsiniz.

## <a name="general-tab"></a>Genel sekmesi

1. **Yinelenen sözleşme faturalama parametreleri** sayfasında, **Genel** sekmesinde, **Faturalama zamanlama grubu** alanında bir ödeme çizelgesi grubu seçin. Faturalama zamanlama gruplarını ayarlamak hakkında daha fazla bilgi için bu konunun sonraki bölümündeki [Fatura zamanlaması grupları](#set-up-billing-schedule-groups) bölümüne bakın.
2. **Sonlandırma türü** alanında, ödeme planı sona erdirilmiş durumda son faturanın nasıl hesaplanacağını seçin:

    - **Zamanlamayı ayarla** – Sonlandırma tarihinde faturalama zamanlamasıyla kesin, zamanlamanın durumunu **Son faturalama** olarak değiştirin ve artık tanınmaması gereken tutarı ters çevirerek ilişkili erteleme zamanlamasını ayarlayın. Faturalama başlangıç tarihi bitiş tarihinden sonraysa kalan faturalama dönemleri kaldırılır.
    - **Kalan fatura**: Faturalama zamanlaması için kalan tutarı sonlandırma dönemine ekleyin ve zamanlamanın durumunu **Son faturalama** olarak değiştirin ve erteleme zamanlamasını güncelleştirin. Faturalama başlangıç tarihi bitiş tarihinden sonraysa kalan tüm faturalama dönemlerinin toplam tutarı faturalama dönemine eklenir ve kalan faturalama dönemleri kaldırılır.
    - **Düzeltme yok**: Sonlandırma tarihinde faturalama zamanlamasını sonlandırın. Faturalama planında herhangi bir düzeltme yapılmaz.

3. **Benzersiz zamanlama türü** alanında, müşterilerin tek bir fatura planla sınırlı olduğunu belirtmek için **Yok** seçeneğini belirleyin. Müşterilerin benzersiz bir planla sınırlı olduğunu belirtmek üzere **Müşteri başına** veya **Son kullanıcı başına**'yı seçin.
4. Fatura zamanlaması ayrıntı satırlarını faturalama zamanlamasının oluşturulduğu veya güncelleştirildiği ayın sonuyla uyumlu hale getirmek için **Aya uyumlu hale getir** seçeneğini **Evet** olarak ayarlayın. Artımlı tarihleri kullanmak için **Hayır** olarak ayarlayın.
5. Dönemdeki gün sayısını temel alarak fatura tutarları tahsis etmek için **Eşit dağıtma kısmi dönemler** seçeneğini **Evet** olarak ayarlayın. Gün sayısına bakmaksızın, her faturalama döneminde eşit tutar almak için **Hayır** olarak ayarlayın.
6. **Eşit dağıtım kısmi dönemler** seçeneğini **Evet** olarak ayarlarsanız, tutarları dönemdeki gün sayısına göre dağıtmak için **Eşit dağıtma yöntemi** alanını **Günlük** olarak ayarlayın. Her ay eşit tutarı olacak şekilde **Aylık** olarak ayarlayın.
7. Yeni oluşturulan fatura zamanlamalarının varsayılan olarak tutuluyor olarak belirtir.

    > [!NOTE]
    > Faturalama planında ayrı tutmayı kaldırmak için kullanıcı, bir kullanıcı grubunun parçası olmalıdır. **Ayrı tutmayı kaldır** seçeneğinin etkin olduğu bir kullanıcı grubu ayarlamak için, **Ayrı tutmayı kaldır kullanıcı grubu geçersiz kılma** seçeneğini belirleyin.

8. **Fatura hareket türü** alanında, yeni ödeme zamanlamaları için varsayılan fatura hareket tipini seçin.
9. İlgili erteleme zamanlamasını ödeme zamanlamasıyla aynı tarihleri kullanacak şekilde hizalamak için, **Ertelemeyi faturalama ile hizala** seçeneğini **Evet** olarak ayarlayın. Farklı tarihler kullanmak için **Hayır** olarak ayarlayın.
10. Gelir ayırma özelliğini kullanıyorsanız, bir ödeme planına maddeler eklendiğinde **Gelir ayrımını otomatik olarak oluştur** seçeneğini **Evet** olarak ayarlayın. Madde gelir tablosu olarak ayarlanmışsa, ödeme planlama satırında **Gelir bölünmesi** onay kutusu otomatik olarak seçilir. **Gelir bölünmesi** onay kutusunu el ile seçmek istiyorsanız, bu seçeneği **Hayır** olarak ayarlayın.
11. Satış siparişi oluşturma alanlarını ayarlayın:

    - Faturalar döneme, müşteriye veya maddeye göre birleştirilebilir. Herhangi bir **Evet** ve **Hayır** değeri ayarlanabilir. Faturalar aynı zamanda madde grubuna göre bölünebilir.
    - Faturalar için aşağıdaki deftere nakil seçenekleri kullanılabilir:

        - **Satış siparişi oluştur** – Yalnızca satış siparişi oluşturur.
        - **Deftere nakil faturasını göster** – Satış siparişini faturalayın ve faturayı el ile deftere nakledebileceğiniz bir sayfa açın.
        - **Ücret metni faturası oluştur** – Serbest metin faturalarını kullanıyorsanız bu seçeneği belirleyin.
        - **Faturayı otomatik olarak deftere naklet** – Satış siparişini faturalayın ve otomatik olarak deftere nakledin.

    - Faturalama başlangıç tarihi ve bitiş tarihi içeren bir açıklama eklemek için, **Madde açıklamasına fatura tarihlerini ekle** seçeneğini **Evet** olarak ayarlayın.
    - **Sıfır dışı tüketimi hariç tut** seçeneğini **Evet** olarak ayarlayıp tüketimi olmayan fatura zamanlama satırlarını hariç tutun. Bu satırları satış siparişine eklemek için **Hayır** olarak ayarlayın.
    - Satış siparişine bölünen bir gelirin alt maddelerini yazdırmak istemiyorsanız, **Alt öğeleri yazdırma** seçeneğini **Evet** olarak ayarlayın. Yalnızca üst madde faturada görüntülenir. (Gizli) alt maddelerin net tutarı sıfır olmayan bir toplam ise, üst satırın net tutarı alt satırların bir özetini gösterir. Bu seçeneği, satış faturasındaki üst öğenin altındaki tüm alt öğeleri yazdırmak için **Hayır** olarak ayarlayın.

12. Destek ve yenilemeler için alanları ayarlayın:

    - Bir satış siparişindeki destek ve yenileme özelliğini otomatik olarak kullanmak için, **Desteği otomatik etkinleştir ve yenile** seçeneğini **Evet** olarak ayarlayın.
    - **Destek ve yenileme düzeyi** alanında, varsayılan destek ve yenileme düzeyini seçin.
    - **Destek ve yenileme miktarı** alanında, varsayılan destek ve yenileme miktarını seçin.
    - **Varsayılan destek ve yenileme başlangıç tarihi** alanında, destek ve yenilemeler için varsayılan başlangıç tarihi olarak kullanılacak tarihi belirtin:

        - **Hareket tarihi** – Hareket tarihini başlangıç tarihi olarak kullanın.
        - **Geçerli ayın başlangıcı** – Başlangıç tarihi olarak geçerli ayın ilk gününü kullanın.
        - **Sonraki ayın başlangıcı** – Başlangıç tarihi olarak sonraki ayın ilk gününü kullanın. Hareket tarihi ayın ilk günüyse, geçerli ayın ilk günü kullanılır.
        - **15 Kuralı** – Hareket tarihi, ayın ilk günü ile on beşinci günü arasındaysa başlangıç tarihi olarak geçerli ayın ilk gününü kullanın. Hareket tarihi herhangi bir ayın on altıncı günü veya daha sonraysa sonraki ayın ilk günü başlangıç tarihidir.

    - İndirim tutarını destek veya yenileme tutarına dahil etmek için, **Hesaplamaya indirimi dahil et** seçeneğini **Evet** olarak ayarlayın. İskonto tutarını hariç bırakmak için **Hayır** olarak ayarlayın.
    - **Destek frekansı** ve **Yenileme sıklığı** alanlarında, destek ve yenileme maddeleri bir faturalama planına eklendiğinde kullanılacak sıklığı seçin: **Günlük**, **Aylık**, **Üç aylık**, **Altı aylık** veya **Yıllık**.
    - Madde grubuna göre yeni maddelerin başlangıç ve bitiş tarihlerini varolan maddelere göre hizalamak için **Madde grubuna göre hizala** seçeneğini **Evet** olarak ayarlayın.
    - Yenileme başladıktan sonra, bir sonraki faturalanmamış dönemin tarihini temel alarak yenileme öğesinin hizalama tarihini belirlemek için, **Sonraki faturalandırılmamış döneme hizala** seçeneğini **Evet** olarak ayarlayın.
    - Madde seri numarasını başlangıç satış siparişi satırından ilgili ödeme çizelgesi satırına kopyalamak için **Seri numarasını kopyala** seçeneğini **Evet** olarak ayarlayın.

13. Faturalama planında ilerletme kullanıyorsanız, tüketici fiyat endeksi hesaplaması için kullanılan yöntemi seçin.
14. Ödeme çizelgesi satırlarında fiyat değişikliği kaydı istiyorsanız **Fiyat değişikliğini izle** seçeneğini **Evet** olarak ayarlayın. Bir faturalama çizelgesi satırı standarttan düz arasında el ile değiştirilirse ve yeni fiyat girilirse, denetim bilgileri ödeme çizelgesi satırında izlenir. Bu değişiklikleri izlemek istemiyorsanız seçeneği **Hayır** olarak ayarlayın.
15. **Fatura oluştur** sayfasında varsayılan olarak başlangıç tarihine mı, yoksa bitiş tarihine göre mi filtre uygulanıp uygulanmayacağını belirtin.
16. **Faturalanmayan gelir** özelliğini kullanırsanız, kullanılan seçenekleri belirtin:

    - Yevmiye defterinin aynı anda oluşturulmasını ve deftere nakledilmesini istiyorsanız, **Yevmiye defterini otomatik olarak deftere naklet** seçeneğini **Evet** olarak ayarlayın. Genel günlüğü oluşturmak ve sonra el ile deftere nakletmek istiyorsanız bunu **Hayır** olarak ayarlayın.
    - **Varsayılan günlük adı** alanında, yevmiye defteri oluşturulduğunda kullanılacak varsayılan günlük adını seçin.
    - **Kısa vadeli faturalanmayan yöntem** alanında, kullanıyorsanız, kısa vadeli fatura edilmemiş yöntemini seçin. **Hiçbiri**'ni seçerseniz, kısa vadeli işlevi faturalanmayan gelirle kullanılmaz. Kalan mali yılı kullanmak için her zaman 12 ay veya **Sabit yıl** kullanmak üzere **Toplama dönemlerini** seçin.

17. Bir faturalama zamanlaması ve bu satırların satırları sonlandırıldıktan sonra kullanılan seçenekleri belirtin:

    - **Alacak faturası düzenle**: Faturalama zamanlaması veya faturalama zamanlama satırı sonlandırıldığında bir alacak dekontu oluşturun.
    - **Kredi düzeltmesi**: Bir satır sonlandırıldığında faturalama zamanlaması için bir kredi düzeltmesi oluşturun. Kredi düzeltmesi, faturalama zamanlaması için gelecekteki bir faturalama döneminde görüntülenir. Alacak düzeltmesi ayrıca, kredinin faturalama zamanlamasına uygulanması bitene kadar bir sonraki faturalama dönemi için fatura tutarını güncelleştirir.
    - **Kredi yok**: Faturalama zamanlaması veya faturalama zamanlama satırı sonlandırıldığında kredi düzeltmesi veya alacak dekontu oluşturmayın. Bu seçenek yalnızca bir faturalama zamanlamasını sonlandırmak için **Düzeltme yok** seçeneği kullanıldığında değerlendirilebilir.

## <a name="sequence-number-tab"></a>Sıra numarası sekmesi

Faturalama zamanlama numaraları için varsayılan değeri ayarlamak üzere, **Yinelenen sözleşme faturalama parametreleri** sayfasındaki **Sıra numarası** sekmesini kullanın. **Numara serileri** sayfasında varsayılan değerler ayarlanır (**Organizasyon yönetimi \> Numarası serileri \> Numara serileri**).

## <a name="set-up-billing-schedule-groups"></a>Faturalama planlama gruplarını ayarla

Yinelenen sözleşme faturalaması için bir ödeme çizelgesi grubu oluşturmak üzere **Ödeme çizelgesi grubu** sayfasını kullanın. Yeni bir faturalama çizelgesi oluşturulduğunda ve buna bir faturalama zamanlama grubu uygulandığında, **Faturalama zamanlama grubu** sayfasında tanımlanan değerler, ödeme planı için varsayılan değerler olarak girilir. Oluşturduğunuz belirli fatura planının herhangi bir varsayılan değerini değiştirebilirsiniz. Birden fazla faturalama çizelgesi grubu ayarlayıp, **Yinelenen sözleşme faturalama parametreleri** sayfasında varsayılan faturalama zamanlama grubu olarak bunlardan birini atayabilirsiniz.

Yinelenen sözleşme faturalaması için bir ödeme çizelgesi grubu oluşturmak üzere aşağıdaki adımları izleyin.

1. **Faturalama zamanlama grubu** sayfasında, bir ödeme çizelgesi grubu oluşturmak için **Yeni**'yi seçin.
2. **Faturalama zamanlama grubu** alanına, benzersiz bir tanımlayıcı girin.
3. **Açıklama** alanına bir açıklama girin.
4. **Faturalama sıklığı** alanında, faturalama zamanlamasının müşteriye ne kadar sıklıkla faturalanacağı belirtilir: **Bir kerelik**, **Günlük**, **Aylık**, **Üç aylık**, **Altı aylık** veya **Yıllık**.
5. **Faturalama aralığı** alanına bir faturalama aralığı girin. Örneğin, **Faturalama sıklığı** alanını **Aylık** olarak, **Faturalama aralığı** alanını da her iki ayda bir faturalamak üzere **2** olarak ayarlayın.
6. **Fiyatlandırma yöntemi** alanında, faturalama zamanlamasındaki maddeler için varsayılan fiyatlandırma yöntemi:

    - **Standart** – Birim fiyatı, girilen toplam miktara dayalı olarak hesaplayın ve ürün bilgileri yönetimindeki **Serbest bırakılmış ürünler** sayfasından standart fiyatlandırmayı kullanır.
    - **Düz** – Ödeme planı satırına girilen bir düz fiyatı uygulayın.
    - **Katman** – Farklı fiyatlandırma katmanları içinde sabit bir miktar kullanarak birim fiyatı hesaplayın. Bir sonraki fiyatlandırma ayracının taşınmadan önce her katmanın doldurulması gerekir.
    - **Düz Katman** – Farklı fiyatlandırma katmanları içinde sabit bir miktar ve kapsamlı fiyat tutarları kullanarak birim fiyatı hesaplayın. Bir ödeme döneminde masraflandırılan fiyat, faturalama miktarının bulunduğu katmana karşılık gelen genişletilmiş fiyatı kullanır.

7. **Madde türü** alanında, faturalama grubu için madde tipini seçin:

    - **Standart** – Miktar statikse bu değeri seçin.
    - **Kullanım** – Ölçümlenen veya tüketim türünde maddeler için bu değeri seçin. Bu değeri seçerseniz, bir ölçüm veya aygıttaki ödeme dönemi değerini (okuma) girmek için **Kullanım okuma seçeneği** alanını **Okumaya** göre ayarlayın. Tüketilen değer önceki faturalama dönemine ve girdiğiniz geçerli okumaya göre hesaplanır.
    - **Kilometre taşı** – Aşama bazında faturalama işlevini kullanmak için bu değeri seçin. Bu değeri seçerseniz, **Kilometre taşı şablonu** alanında, kullanıyorsanız, kilometre taşı şablonunu seçin.
    - **Tüketim** - Fatura dönemi için tüketilen değeri girmek üzere bu değeri seçin.

8. Aynı müşteri için konsolide edilmiş faturaların ve ayrı faturaların birleşimini oluşturmak üzere **Ayrı fatura** seçeneğini **Evet** olarak ayarlayın. Örneğin, bir müşterinin beş faturalama planı vardır. Bunlardan üçü tek bir faturada konsolide edilir, ancak diğerinin her biri ayrı bir fatura gerektirir. Müşteri için yalnızca bir konsolide fatura oluşturmak için **Hayır** seçeneğini ayarlayın.
9. Fatura oluşturulduğunda sonraki faturalama dönemi için yenilenen faturalamayı otomatik olarak yenilemek üzere **Otomatik olarak yenile** seçeneğini **Evet** olarak ayarlayın. Faturalama zamanlamasını el ile yenilemek için **Hayır** olarak ayarlayın. **Yenileme başına eklenecek satırlar** alanına, her yenileme için eklenecek satır sayısını belirtin.
10. *İlerleme* (fiyat artışları) ile bu ödeme çizelgesi grubuyla ilişkilendirilmiş ödeme çizelgelerinizi uygulamak için **İlerletme** seçeneğini **Evet** olarak ayarlayın.
