---
title: Kiralama ekleme veya kopyalama (Önizleme)
description: Bu makalede, Varlık kiralamada kiralamaya ilişkin bilgi girerek veya mevcut bir kiralamadaki bilgileri kopyalayarak yeni bir kiralama oluşturma açıklanmaktadır.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880946"
---
# <a name="add-or-copy-leases-preview"></a>Kiralama ekleme veya kopyalama (Önizleme)

[!include [banner](../includes/banner.md)]

Bu makalede, Varlık kiralamada sıfırdan kiralama oluşturma ve mevcut bir kiralamayı kopyalayarak kiralama oluşturma yöntemleri açıklanmaktadır. Sıfırdan kiralama oluşturma işlemi, yeni kiralamaya ilişkin bilgilerin girilmesini ve sonra bir kiralama planlamasının oluşturulmasını içerir. En az bir kiralama ayarladıktan sonra, bilgileri mevcut bir kiralamadan kopyalayıp daha sonra yeni bir kiralama oluşturmak için bu bilgileri düzenlemeniz daha kolay olabilir.

## <a name="create-a-lease"></a>Kiralama oluşturma

Varlık kiralamada kiralama oluşturmak için bu adımları izleyin.

1. **Kiralama özeti** sayfasındaki Eylem bölmesinde **Yeni**'yi seçin.
2. Kiralama bilgilerini girin. Gerekli alanların kırmızı kenarlıkları vardır.

Kira ödemesi başlangıç tarihi, kira başlangıç tarihinden önce olamaz. Kira ödemesi için kiralamanın başlangıç tarihinden önceki bir başlangıç tarihi girerseniz bir hata iletisi alırsınız.

Varsayılan olarak **Kira ayrıntıları** sayfasının **Genel** hızlı sekmesindeki **Ödeme tutarının dökümü** seçeneği, **Varlık ira parametreleri** sayfasında **Ödeme dökümüne izin ver** seçeneği **Evet** olarak ayarlanmışsa **Hayır** olarak ayarlanmıştır. 

**Ödeme tutarı dökümü** seçeneği **Evet** olarak ayarlanmışsa, **Ödeme planı satırları** hızlı sekmesindeki **Ödeme tutarı** alanı kilitlenir. Bu, daha sonra **Ödeme tutarı dökümü** kataloğunda girilen ödeme tutarlarının toplamına ayarlanır.

Listelenen ödeme tiplerini ekleyebileceğiniz bir sayfa açmak için **Ödeme tutarı dökümü** seçin. **Ödeme tutarına toplam ekle** düğmesi toplamları, **Ödeme tutarı** alanına taşır.

> [!NOTE]
> Bir dökümü bulunan ödeme tutarı ekler ve sonra **Esc** tuşunu seçerseniz, girilen tutarlar **Ödeme planı satırları** hızlı sekmesindeki **Ödeme tutarı** alanına eklenmez. Bunun yerine, bunlar **Ödeme tutarı dökümü** iletişim kutusunda depolanır. İletişim kutusunun toplam tutarı göstermesini istiyorsanız, **Tutar** sütununu seçin, seçip basılı tutun (veya sağ tıklayın) ve sonra **Bu sütunun toplamını** seçin. 

**Satır kopyala** düğmesi, listelenen ödeme dökümünü kopyalar.

## <a name="create-a-lease-schedule"></a>Kiralama planı oluşturma

Kiralamaya ilişkin bilgileri girmeyi tamamladıktan sonra, kiralama planı oluşturmak için aşağıdaki adımları izleyin.

> [!NOTE]
> Mali boyutlar özel mali boyutlara göre değişebilir.

1. Kiralama defterleri oluşturmak için **Planlama oluştur**'u seçin. Kiralama defterleri arasında ödeme, itfa, amortisman ve gider planlamaları yer alır.
2. Kiralama defterlerine erişmek ve yeni oluşturulan planlamaları görüntülemek için **Defterler** sekmesini seçin.

    **Defter ayrıntıları** sayfası, kiralamaya tahsis edilmiş olan defterlerde kiralamanın nasıl hesaplandığını gösterir. Buradan, kira planlamalarını görebilirsiniz.

    Ödeme planı, **Kiralama ekle** sayfasındaki **Ödeme planı satırları** sekmesinden alınan girişleri içerir. Her ödeme tutarını ve değişken ödemeyi değiştirmeye devam edebilirsiniz. Kiralama yükümlülüğü değiştirilen ödeme planına göre hesaplanır.

    > [!NOTE]
    > Kira ödemesi başlangıç tarihi, kiralamanın başlangıç tarihiyle aynı veya daha ileri bir tarih olmalıdır. Ödeme başlangıç tarihi, kiralamanın başlangıç tarihinden önceki bir tarihse bir hata iletisi alırsınız. 

4. Ödeme planını incelemeyi tamamladıktan sonra **Planlamayı onayla**'yı seçin. Planlama onaylandıktan sonra kiralama, artık düzenlenemez.

    > [!NOTE]
    > Sistem, kiralama süresini **Kiralama ekle** sayfasındaki ödeme planı satırlarından otomatik olarak hesaplar.
    >
    > Kiralama süresini aylık olarak hesaplamak için sistem, belirli bir ödeme planı satırında başlangıç tarihi ile bitiş tarihi arasındaki farkı bulur. Ardından, sonraki ödeme planı satırına gider ve farkı tekrar bulur. Son olarak, sistem kiralama süresini aylık olarak belirlemek için tüm tutarları toplar.

5. Hesaplanan dönem içi faiz giderlerini görüntülemek için **Kira yükümlülüğü amortisman planlaması** sayfasını açın. Hesaplanan sabit amortismanı görüntülemek için **Varlık amortisman planlaması** sayfasını açın.
6. Hesaplanan tutarı incelemeyi tamamladıktan sonra **İlk kabul** sayfasında ilk kabul günlüğü girişinizi oluşturabilirsiniz. Günlüğün oluşturulduğunu bildiren bir ileti alırsınız.

    > [!NOTE]
    > Girişi el ile deftere nakledene kadar günlük girişi Genel muhasebeye nakledilmez.

7. Önerilen ilk kabul girişini deftere nakletmeden önce gözden geçirmek için **Varlık kiralama günlükleri**'ni seçin.

    > [!NOTE]
    > Varlık kiralama günlüğü el ile oluşturulamaz. Kiralama planları oluşturulduğunda otomatik olarak oluşturulur.

8. İlk kabul günlüğü girişini gözden geçirmeyi bitirdiğinizde ve deftere nakletmeye hazır olduğunuzda, kullanım hakkı (ROU) varlığını ve kiralama yükümlülüğünü Genel muhasebede tanımak için **Deftere nakil**'i seçin.

## <a name="copy-a-lease"></a>Kiralamayı kopyalama

Varlık kiralama, aynı bilgilere sahip olan yeni bir kiralama oluşturmak için kira ayrıntılarını kopyalamanızı sağlar. Daha sonra, kopyalanan kiralama için plan oluşturmadan önce kiralama alanlarını değiştirebilirsiniz.

1. **Kiralama özeti** sayfasında, kopyalanacak kirayı seçin ve sonra Eylem bölmesinde **Kiralamayı kopyala**'yı seçin.

    > [!NOTE]
    > Kiralama kodlarının numara sırası için **El ile** parametresi kapatılmışsa, dizideki bir sonraki numara otomatik olarak kopyalanan kiralamanın kiralama kodu olarak oluşturulur. **El ile** parametresi açıksa kiralamayı kopyalama işlemine devam etmeden önce kiralama kodunu girmenizi isteyen bir ileti alırsınız.

2. **Kopyala** seçeneğini belirleyin. Seçili kiralamadan alınan kiralama ayrıntıları yeni kiralamaya kopyalanır. Ardından, kaydetmeden önce yeni kiralamanın ayrıntılarını düzenleyebilir ve kira planlarını oluşturabilirsiniz.

## <a name="asset-leasing-journal"></a>Varlık kiralama günlüğü

Varlık kiralamada oluşturulan tüm günlük girişleri, Varlık kiralama günlüğünde yer alır. **Varlık kiralama günlüğü** sayfasında (**Varlık kiralama \> Günlük girişleri \> Varlık kiralama günlüğü**), deftere nakil durumuna göre filtre uygulayabilir, belirli günlük girişlerini ve fişleri görüntüleyebilir ve deftere nakledilmemiş günlük girişlerini deftere nakledebilirsiniz.

> [!NOTE]
> Varlık kiralama günlüğü el ile oluşturulamaz. Kiralama planları oluşturulduğunda otomatik olarak oluşturulur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
