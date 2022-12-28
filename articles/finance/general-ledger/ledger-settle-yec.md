---
title: Genel muhasebe kapatma özelliği ile yıl sonu öncesi kapanışı arasındaki farka duyarlılık
description: Bu makalede, Genel muhasebe yıl sonu kapanışları çalıştırıldıktan önce genel muhasebe kapatmaları arasındaki algılamanın nasıl kullanılacağı açıklanır.
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
ms.openlocfilehash: c79b6f50296560e1534be0621bb2aa8eaa2c1dc8
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832182"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close"></a>Genel muhasebe kapatma özelliği ile yıl sonu öncesi kapanışı arasındaki farka duyarlılık

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-before-year-end-close"></a>Yıl sonu kapanışı öncesinde genel muhasebe kapatma Farkındalık özelliği için hazırlanma

**Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık** özelliğindeki (**Farkındalık** özelliği) temel bir değişiklik, genel muhasebe kapatılması mali yıllar arasında yapılamaz. Bu çapraz yıl sınırlaması yalnızca genel muhasebe kapanışıyla ilgilidir, Alacak hesaplarına veya Borç hesaplarına ait hesap kapatmalarını desteklemez.

**Farkındalık** özelliğini etkinleştirmeden önce, yıl sonu kapanışının üzerine gitmesi gereken mali yılın mali yıllara göre kapatılan genel muhasebe hareketleri olmamalıdır. Özellikle, mali yılda deftere nakledilen tüm hareketlerin, farklı bir mali yılda deftere nakledilen hareketlerden kapatılmamış olması gerekir. Hareketler, aynı mali yıl içindeki hareketlere göre yeniden kapatılabilir.

Bu makalede, mali yıl boyunca kapatılan genel muhasebe hareketlerini tanımlamak, kapatmak ve yeniden kapatmak için gerekli adımlar açıklanmaktadır. Sağlanan örnekte, 2021 mali yılı kapatılmıştır ve mali yıl 2022 yıl sonu kapanışını çalıştırmaya hazırlanıyorsunuz.

## <a name="example-setup"></a>Örnek kurulumu

Aşağıdaki şekilde, ana hesap 110190 için deftere nakledilen hareketler gösterilir. Yeşil renkteki genel muhasebe hareketleri, aynı mali yıl içinde genel muhasebede kapatılmıştır ve değiştirilmesi gerekmez. Kırmızı renkle yapılacak hareketler genel muhasebe ile kapatılmıştır, ancak hareket tarihleri farklı mali yıllara dahil edilir. Bu hareketler tanımlanmalıdır ve genel muhasebe kapanışının ters işlem yapılması gerekebilir.

![Genel muhasebe hareketleri.](./media/YEC1.png)

## <a name="example"></a>Örnek

Kuruluşunuz mali yıl 2022 için yıl sonu kapanışını çalıştırdıktan önce **Farkındalık** özelliğini kullanmak isterse, bu adımları izleyin.

> [!NOTE]
> 2021 ve önceki mali yılların yıl sonu kapanışı, yalnızca mali yıl 2021 veya önceki sürümlerde yeni hareketler deftere nakledildiyse yeniden çalıştırılmalıdır. Aşağıdaki yordamı tamamladığınızda, 2021'ye hiçbir yeni hareket nakledilemez. Bu nedenle, yıl sonu kapatma işleminin yeniden çalıştırılması gerekmez.
>
> Mali yıllarda kapatılan genel muhasebe hareketleri, 2022 veya daha ileri bir sürümde deftere nakledilen bir harekete karşı kapatılmadığından, genel muhasebe kapatma olarak kalabilir. Örneğin, 2019 ve 2020 geneli hareketlerini kapatmışsanız, bunlar kapatılmış durumda kalabilir.

1. İsteğe bağlı: **Farkındalık** özelliğini geçici olarak etkinleştirin.

    - Özelliği etkinleştirmeyi seçerseniz, sonraki adımlarda belirtilen şekilde devre dışı bırakmanız gerekir. Özelliği şimdi etkinleştirmenin yararı, kullanıcıların farklı mali yıllara nakledilen genel muhasebe hareketlerini kapatma işlemi yapmasını geçici olarak engellemesidir.
    - Özelliği etkinleştirmeetmeyi seçerseniz, takımınızı mali yıllara ait olarak kapatma konusunda sizi sormanız önerilir. Bu adımlar tamamlandıktan sonra yılları arası kapatma gerçekleşirse, genel muhasebe hareketlerini tanımlamak ve kapatmak için gereken adımları tekrarlamanız gerekir.

2. **Genel muhasebe kapatma** sayfasında, 2021 ve 2022 mali yılları arasında kapatılan tüm hareketlerin toplamını tanımlayın.

    1. Tüm mali yıl 2021 için bir tarih aralığı belirtin. Örneğin, mali yıl olarak bir takvim yılı kullanıyorsanız, 1 Ocak 2021 ile 31 Aralık 2021 arasında bir sayı girin.

        **Farkındalık** özelliği etkinse, kapatılmış bir mali yıl için hareketlerin kapatılmadığı veya kapatılmadığı uyarısı alırsınız. Bu adımda kapatma veya kapatma gerçekleşmediği için uyarı uygun değil.

    2. **Durum** alanında, **Kapatıldı**'yı seçin.
    3. Bir seferde bir genel muhasebe hesabı üzerinde filtreleme.

        - Genel muhasebe kapanışının gerçekleştiği her genel muhasebe hesabı için bu adımları tekrarlamak zorunda olacaksınız.
        - Genel muhasebe hesabı için artık başka genel muhasebe hesapları ayarlanmamışsa, bunları genel muhasebe kapatma kurulumuna geçici olarak geri eklemeniz gerekebilir. Daha sonra, bu genel muhasebe hesaplarının başka bir mali yılda hareketlere karşı kapatılan 2022'de hareketler varsa, bu adımları tamamlayın.

    4. **Durum** sütununda seçin ve basılı tutun (veya sağ tıklayın) ve sonra bu sütuna göre gruplamak için seçin.
    5. **Bu hareket para biriminde tutar** sütununu seçin ve basılı tutun (veya sağ tıklayın) ve sonra toplamları göstermek için bu sütun için toplamı seçin.

        - Hareketleri yalnızca 2021'de kapatıyorsanız toplam 0 (sıfır) olur.
        - Mali yıllara kapatılan hareketler varsa, toplam 0 (sıfır) olmaz.

        Aşağıdaki çizimde, $525,00 bir bakiye vardır. Bu bakiye, farklı bir mali yıldaki hareketlere karşı Kapatılan hareketlerin toplamına karşılık alınır. Toplama işlemi 2021 ve 2022 arasında Kapatılan hareketler ile 2022 ve 2023 arasında kapatılan hareketler dahil olabilir.

        ![Genel muhasebe hareketleri 2021-2022.](./media/YEC2.png)

    6. **Kapatma tarihi** değerine daha da filtre uygulayarak 2020 ve 2021 arasında hangi hareketlerin kapatılacağını tanımlayın. 1 Ocak 2021 ile 31 Aralık 2021 arasında bir tarih aralığı filtresi belirtin. 2021'e nakledilen hareketlerle ilgili 2020 hareket kapatılmadığından hiçbir hareket gösterilmez.
    7. **Kapatma tarihi** değerinde tarih filtresini değiştirerek 2021 ve 2022 arasında hangi hareketlerin kapatılacağını tanımlayın. 1 Ocak 2022 ile 31 Aralık 2022 arasında bir tarih aralığı filtresi belirtin. Hareketler tekrar gösterilir ve tüm hareketler 2021 ile 2022 arasında kapatılmış olduğundan toplam $525,00'dir.

3. **Genel muhasebe kapatma** sayfasında, 2021 ve 2022 mali yılları arasında kapatılan tüm hareketlerin toplamını tanımlayın.

    1. Tüm mali yıl 2022 için bir tarih aralığı belirtin. Örneğin, mali yıl olarak bir takvim yılı kullanıyorsanız, 1 Ocak 2022 ile 31 Aralık 2022 arasında bir sayı belirtin.
    2. **Durum** alanında, **Kapatıldı**'yı seçin.
    3. Bir seferde bir genel muhasebe hesabı üzerinde filtreleme.
    4. **Durum** sütununda seçin ve basılı tutun (veya sağ tıklayın) ve sonra bu sütuna göre gruplamak için seçin.
    5. **Bu hareket para biriminde tutar** sütununu seçin ve basılı tutun (veya sağ tıklayın) ve sonra toplamları göstermek için bu sütun için toplamı seçin.

        ![Genel muhasebe hareketi toplam tutarları.](./media/YEC3.png)

    6. **Kapatma tarihi** değerine ek bir filtre ekleyin. 1 Ocak 2022 ile 31 Aralık 2022 arasında bir tarih aralığı filtresi belirtin. Aynı $525,00 toplamı gösterilir. Bu sonuç, 2021 ve 2022 arasında kapatılan hareketlerin toplam tutarının $525,00 olduğunu doğrular.

        ![2022 ve 2023 kapatma tarihleri için genel muhasebe hareketleri.](./media/YEC4.png)

    7. **Kapatma tarihi** değerine ek filtresini değiştirin. 1 Ocak 2023 ile 31 Aralık 2023 arasında bir tarih aralığı filtresi belirtin. Yeni toplam $700 gösterilir. Bu toplam, 2022 ve 2023 arasında kapatılan hareketlerin toplam miktarıdır.
 
4. 2023 mali yılı için 3. adımı yineleyin. 2024 hareketlerle aynı 2023 hareket kapatılmadığından, toplam 2022'den $700 ile eşleşmelidir.
5. 1. adımdaki **Farkındalık** özelliğini etkinleştirdiyseniz, adım 6'ya geçmeden önce bu özelliği devre dışı bırakın. Sonraki adımlarda, mahsup mali yıllardaki genel muhasebe kapanışına ters işlem göstereceğiz. **Farkındalık** özelliği etkinleştirildiğinde, mali yıl 2021 için genel muhasebe hesabı tersine çevrilemez. Bu nedenle devam etmeden önce bu özelliği devre dışı bırakmanız gerekir.
6. **Farkındalık** özelliği devre dışı bırakıldıktan sonra, ayrıntılı hareketlerin genel muhasebe ile kapanışlarını tersine çevirmek için, **Genel muhasebe kapatma** sayfasında aynı filtreleri kullanın.

    1. **Genel muhasebe kapatma** sayfasına dönün ve 2021 için hareket tarihlerine filtre uygulayın. **Kapatma tarihi** değerine ek bir filtre ekleyin. 1 Ocak 2022 ile 31 Aralık 2022 arasından bir tarih aralığı filtresi belirtin. Sonra $525 toplamını oluşturan ayrıntılı hareketleri bulun. Bu bilgiler için filtre uygulama işlemi kolay olmayabilir. Değerlendirmek için verileri Microsoft Excel'e göndermeniz gerekebilir.
    2. Hareket listesini aldıktan sonra, **Genel muhasebe kapatma** sayfasında genel muhasebe hareketlerini seçin ve **Seçileni işaretle**'yi seçin. Kapatılan genel muhasebe hareketlerinin her iki tarafını da görmek zorunda değilsiniz. Borç veya alacak olarak işaretlerseniz, aynı **Kapatma numarası** değerine sahip her şey ters kaydedilir ve **İşaretli tutar** değeri **0** (sıfır) değilse bile değişir.
    3. Hareketlerin kapatılacağı işlemleri geri almak için **İşaretli hareketleri ters çevir**'i seçin.

    ![İşaretli hareketleri tersine çevir.](./media/YEC5.png)

7. 2022 ve 2023 arasında kapatılan hareketleri kapatma işlemini tersine çevirmek için 6.

    ![Genel muhasebe hareketlerini ters çevir.](./media/YEC6.png)

8. 2022 için açılış bakiyesini iki tutara bölmek üzere bir düzeltme genel günlüğünü deftere nakledin: 2021 mali yılı harekete ve henüz 2022 değiştirilmemiş olan bölüme göre kapatılan bölüm.

    - **Önceki yıla kapatılan açılış bakiyesi bölümü:** İlk tutar, 2021 ve 2022 genelinde kapatılan toplamlara göre ilk tutar $525'dür.
    - **Önceki yıla kapatılmayan açılış bakiyesinin bölümü:** İkinci tutar, açılış bakiyesi ile $525 kapatılan tutarı arasındaki farktır. Kalan tutar: $1025 – $525 = $500.

    Bu şekilde, 2022 hareket işlemini, başlangıçta 2021 harekete karşı kapatılan $525 karşı değiştirebilirsiniz. Genel muhasebe kapatma için kısmi kapatma yapılmasına izin vermediği için bu adım gereklidir.

    1. Yevmiye defterine gidin ve ayarlamayı deftere nakledin. Kuruluşunuz, açık olan dönemlere göre, hangi hareket tarihinin kullanılacağına karar vermeye çalışacaktır. Bu hareketler 2022 Ocak veya Şubat kapatma tarihi kullanılarak kapatılmış olabilir, ancak bu tek açık dönem ise ayarlamanın Aralık ayında deftere nakledilmesi gerekebilir.
    2. **Ana hesap** sayfasında **El ile giriş yapma** parametresine izin verme özelliğini geçici olarak kapatmanız gerekebilir. Ana hesap el ile girişe izin vermiyorsa bu ayarlama deftere nakledilemez.

    ![Düzeltme deftere nakledilmez.](./media/YEC7.png)

9. Kapatılmamış hareketleri yeniden tasfiye edebilirsiniz. **Genel muhasebe kapatmaları** sayfasına dön ve tarih aralığını 1 Ocak 2022'den 31 Aralık 2022'ye kadar olarak sınırlayın. Aşağıdaki çizimde artık mevcut olan kapatılmamış hareketler gösterilir.

    ![Kapatılmamış hareketler.](./media/YEC8.png)

    - $1.025 açılış bakiyesi, -$1.025 için ayarlamaya kapatılabilir.
    - -$400, -$50 ve -$75 için kapatılmış olan ayrıntılı hareketler, $525,00 ayarlamasına karşı kapatılabilir.

    ![Ayrıntılı hareketler.](./media/YEC9.png)

10. **Farkındalık** özelliğini etkinleştirin. Artık yıl sonu kapanışını çalıştırabilirsiniz.

    - Yıl sonu kapanışını çalıştırmadan önce, genel muhasebe kapatma kurulumundaki tüm bilanço hesapları için **Ayrıntıları koru** seçeneğini belirlemeyi düşünebilirsiniz. Bu adımı tamamlamanın yararları hakkında daha fazla bilgi için bkz. Farkındalık belgesi.
    - 2022 için yıl sonu kapanışını başlattığınızda, hareketler hala mali yıllar içinde kapatılmış durumda ise, yıl sonu kapatma işlemi hemen size bildirir.
    - 2021 ve 2022 hareketleri hala kapatılmışsa, **Farkındalık** özelliğini yeniden devre dışı bırakmanız ve bu hareketlerin kapatılması için önceki adımları tekrarlamanız gerekir. Bu yaklaşım, 2021 kapalı olduğundan ve hareketler kapatılan mali yılda kapatılamayacak şekilde gereklidir.
    - 2022 ve 2023 hareketleri hala kapatılmışsa, **Farkındalık** özelliğini devre dışı bırakmanıza gerek **yoktur**. 2022 veya 2023 hiçbirisi kapanmadığı için, önceki adımları kullanarak hareketleri geri alabilirsiniz.

2022 için yıl sonu kapatma başarıyla çalıştırıldıktan sonra, **Farkındalık** özelliğini şimdi etkin durumda bırakabilirsiniz.
