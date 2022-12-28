---
title: Genel muhasebe kapatma özelliği ile yıl sonu sonrası kapanışı arasındaki farka duyarlılık
description: Bu makalede, Genel muhasebe yıl sonu kapanışı çalıştırıldıktan sonra genel muhasebe kapatmaları arasındaki algılamanın nasıl kullanılacağı açıklanır.
author: kweekley
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 7efa9d652d74bd836f51b5b1c5f6bfaf8934ea40
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832183"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close"></a>Genel muhasebe kapatma özelliği ile yıl sonu sonrası kapanışı arasındaki farka duyarlılık

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-after-year-end-close"></a>Yıl sonu kapanışı sonrasında genel muhasebe kapatma Farkındalık özelliği için hazırlanma

**Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık** özelliğindeki (**Farkındalık** özelliği) temel bir değişiklik, genel muhasebe kapatılması mali yıllar arasında yapılamaz. Bu çapraz yıl sınırlaması yalnızca genel muhasebe kapanışıyla ilgilidir, Alacak hesaplarına veya Borç hesaplarına ait hesap kapatmalarını desteklemez.

**Farkındalık** özelliğini etkinleştirmeden önce, yıl sonu kapanışının üzerine gitmesi gereken mali yılın mali yıllara göre kapatılan genel muhasebe hareketleri olmamalıdır. Özellikle, mali yılda deftere nakledilen tüm hareketlerin, farklı bir mali yılda deftere nakledilen hareketlerden kapatılmamış olması gerekir. Hareketler, aynı mali yıl içindeki hareketlere göre yeniden kapatılabilir.

Bu makalede, mali yıl boyunca kapatılan genel muhasebe hareketlerini tanımlamak, kapatmak ve yeniden kapatmak için gerekli adımlar açıklanır. Sağlanan örnekte, 2022 mali yılı kapatılmıştır. Odak, 2023 yıl sonu kapanışı çalıştırılmadan önce genel muhasebe kapatma hareketlerini hazırlamaktır.

## <a name="example-setup"></a>Örnek kurulumu

Aşağıdaki şekilde, ana hesap 110190 için deftere nakledilen hareketler gösterilir. Yeşil renkteki genel muhasebe hareketleri, aynı mali yıl içinde genel muhasebede kapatılmıştır ve değiştirilmesi gerekmez. Kırmızı renkle yapılacak hareketler genel muhasebe ile kapatılmıştır, ancak hareket tarihleri farklı mali yıllara dahil edilir. Bu hareketler tanımlanmalıdır ve genel muhasebe kapanışının ters işlem yapılması gerekebilir.

![Genel muhasebe hareketleri.](./media/afterYEC1.png)

## <a name="example"></a>Örnek

Kuruluşunuz mali yıl 2022 için yıl sonu kapanışını çalıştırdıktan sonra **Farkındalık** özelliğini kullanmak isterse, bu adımları izleyin.

> [!NOTE]
> 2022 ve önceki mali yılların yıl sonu kapanışı, yalnızca mali yıl 2022 veya önceki sürümlerde yeni hareketler deftere nakledildiyse yeniden çalıştırılmalıdır. Aşağıdaki yordamı tamamladığınızda, 2022'ye hiçbir yeni hareket nakledilemez. Bu nedenle, yıl sonu kapatma işleminin yeniden çalıştırılması gerekmez.
>
> Mali yıllarda kapatılan genel muhasebe hareketleri, 2023 veya daha ileri bir sürümde deftere nakledilen bir harekete karşı kapatılmadığından, genel muhasebe kapatma olarak kalabilir. Örneğin, 2019 ve 2020 geneli hareketlerini kapatmışsanız, bunlar kapatılmış durumda kalabilir.

1. **Farkındalık** özelliği etkin olmadan 2022 için yıl sonu kapanışını tamamlayın.
2. İsteğe bağlı: 2022 için yıl sonu kapanışı tamamlandıktan sonra **Farkındalık** özelliğini etkinleştirin. Tüm ayarlamalar deftere nakledildiğinde ve yıl sonu kapatma işlemi tekrar çalıştırılmayacaksa, yıl sonu kapanışı tamamlandı olarak kabul edilir.

    > [!IMPORTANT]
    > 2022 için yıl sonu kapanışı tekrar çalıştırıldığında, **Farkındalık** özelliği etkinleştirilmemelidir. Özelliği şimdi etkinleştirmenin yararı, kullanıcıların farklı mali yıllara nakledilen genel muhasebe hareketlerini kapatma işlemi yapmasını engellemesidir.

    Yıl sonu kapanışı tamamlanmadıysa, **Farkındalık** özelliğini etkinleştirmeden sonraki adımları yine de tamamlayabilirsiniz. Aşağıda belirtildiği gibi sonraki bir adımdaki özelliği etkinleştirmelisiniz.

3. **Genel muhasebe kapatma** sayfasında, 2022 ve 2023 mali yılları arasında kapatılan tüm hareketlerin toplamını tanımlayın. 2022 hareketlerine karşı kapatılan 2021 hareketleri, 2022 için yıl zaten kapalı olduğundan ilgili olmadığını unutmayın. Bu hareketler kapalı kalabilir.

    1. Tüm mali yıl 2022 için bir tarih aralığı belirtin. Örneğin, mali yıl olarak bir takvim yılı kullanıyorsanız, 1 Ocak 2022 ile 31 Aralık 2022 arasında bir sayı belirtin.
    2. **Durum** alanında, **Kapatıldı**'yı seçin.
    3. Bir seferde bir genel muhasebe hesabı üzerinde filtreleme.

        - Genel muhasebe kapanışının gerçekleştiği her genel muhasebe hesabı için bu adımları tekrarlamak zorunda olacaksınız.
        - Genel muhasebe hesabı için artık başka genel muhasebe hesapları ayarlanmamışsa, bunları genel muhasebe kapatma kurulumuna geçici olarak geri eklemeniz gerekebilir. Daha sonra, bu genel muhasebe hesaplarının 2022 veya önceki hareketlere karşı kapatılan 2023'te hareketler varsa, bu adımları tamamlayın.

    4. **Durum** sütununda seçin ve basılı tutun (veya sağ tıklayın) ve sonra bu sütuna göre gruplamak için seçin.
    5. **Bu hareket para biriminde tutar** sütununu seçin ve basılı tutun (veya sağ tıklayın) ve sonra toplamları göstermek için bu sütun için toplamı seçin.

        - Hareketleri yalnızca 2022'de kapatıyorsanız toplam 0 (sıfır) olur.
        - Mali yıllara kapatılan hareketler varsa, toplam 0 (sıfır) olmaz.

    6. **Kapatma tarihi** değerine filtre uygulayarak 2022 ve 2023 arasında hangi hareketlerin kapatılacağını tanımlayın. 1 Ocak 2023 ile 31 Aralık 2023 arasında bir kapanış tarihine filtre seçtiyseniz, genel muhasebe 2022 ve 2023 arasında Kapatılan hareketlerin toplamı olan $700 alırsınız.

    ![Toplam 2022 genel muhasebe hareketleri.](./media/afterYEC2.png)

4. 2023 mali yılı için 3. adımı yineleyin. 2024 hareketlerle aynı 2023 hareket kapatılmadığından, toplam 2022'den $700 ile eşleşmelidir.

    ![Toplam 2023 genel muhasebe hareketleri.](./media/afterYEC3.png)

5. 2. adımdaki **Farkındalık** özelliğini etkinleştirdiyseniz, adım 6'ya geçmeden önce bu özelliği devre dışı bırakın. Sonraki adımlarda, mahsup mali yıllardaki genel muhasebe kapanışına ters işlem göstereceğiz. **Farkındalık** özelliği etkinleştirildiğinde, mali yıl 2022 için genel muhasebe hesabı tersine çevrilemez. Bu nedenle devam etmeden önce bu özelliği devre dışı bırakmanız gerekir.
6. **Farkındalık** özelliği devre dışı bırakıldıktan sonra, ayrıntılı hareketlerin genel muhasebe ile kapanışlarını tersine çevirmek için, **Genel muhasebe kapatma** sayfasında aynı filtreleri kullanın.

    1. **Genel muhasebe kapatma** sayfasına dönün ve 2023 için hareket tarihlerine filtre uygulayın. Sonra $700 toplamını oluşturan ayrıntılı hareketleri bulun. Bu bilgiler için filtre uygulama işlemi kolay olmayabilir. Değerlendirmek için verileri Microsoft Excel'e göndermeniz gerekebilir.
    2. Hareket listesini aldıktan sonra, **Genel muhasebe kapatma** sayfasında genel muhasebe hareketlerini seçin ve **Seçileni işaretle**'yi seçin. Kapatılan genel muhasebe hareketlerinin her iki tarafını da görmek zorunda değilsiniz. Borç veya alacak olarak işaretlerseniz, aynı **Kapatma numarası** değerine sahip her şey ters kaydedilir ve **İşaretli tutar** değeri **0** (sıfır) değilse bile değişir.
    3. Hareketlerin kapatılacağı işlemleri geri almak için **İşaretli hareketleri ters çevir**'i seçin.

    ![Hareketleri tersine çevir.](./media/afterYEC4.png)

7. 2023 için açılış bakiyesini iki tutara bölmek üzere bir düzeltme genel günlüğünü deftere nakledin: 2022 mali yılı harekete ve henüz 2023 değiştirilmemiş olan bölüme göre kapatılan bölüm.

    - **Önceki yıla kapatılan açılış bakiyesi bölümü:** İlk tutar, 2022 ve 2023 genelinde kapatılan toplamlara göre ilk tutar $700'dür.
    - **Önceki yıla kapatılmayan açılış bakiyesinin bölümü:** İkinci tutar, açılış bakiyesi ile $525 ilk tutarı arasındaki farktır. Kalan tutar: $1.700 – $700 = $1.000.

    Bu şekilde, 2023 hareket işlemini, başlangıçta 2022 harekete karşı kapatılan $700 karşı değiştirebilirsiniz. Genel muhasebe kapatma için kısmi kapatma yapılmasına izin vermediği için bu adım gereklidir.

    1. Yevmiye defterine gidin ve ayarlamayı deftere nakledin. Kuruluşunuz, 2023'te açık olan dönemlere göre, hangi hareket tarihinin kullanılacağına karar vermeye çalışacaktır.
    2. **Ana hesap** sayfasında **El ile giriş yapma** parametresine izin verme özelliğini geçici olarak kapatmanız gerekebilir. Ana hesap el ile girişe izin vermiyorsa bu ayarlama deftere nakledilemez.

    ![Düzeltme deftere nakledilmez.](./media/afterYEC5.png)

8. Kapatılmamış hareketleri yeniden tasfiye edebilirsiniz. **Genel muhasebe kapatmaları** sayfasına dön ve tarih aralığını 1 Ocak 2022'den 31 Aralık 2022'ye kadar olarak sınırlayın. Aşağıdaki çizimde artık mevcut olan kapatılmamış hareketler gösterilir.

    ![Kapatılmamış hareketler.](./media/afterYEC6.png)

    - $1.700 açılış bakiyesi, -$1.700 için ayarlamaya kapatılabilir.
    - -$700 için kapatılmış olan ayrıntılı hareketler, $700,00 ayarlamasına karşı kapatılabilir.

9. **Farkındalık** özelliğini yeniden etkinleştirin.
10. **Farkındalık** özelliği etkinleştirildikten sonra, mali yıllar için genel muhasebe hesabı tersine çevrilemez. 2023 içindeki yeni hareketlere karşı işlem yapabilmeniz için, önce kalan $1.000 bakiyesini daha küçük tutarlarda bölmeniz gerekebilir. Bazı müşteriler, $1.000 kapatılan 2022 hareketleri temsil edecek şekilde, bu ayrıntıyı 8 numaralı adımda deftere nakletmeye devam ederler. Bu yaklaşım, yalnızca geçerli yıl için **Farkındalık** özelliğinin ne yaptığını taklit eder. Sonraki yıl, genel muhasebe kapatma kurulumunda **Ayrıntıları koru** ayarı kullanılarak otomatik olarak gerçekleştirilir.
