---
title: Serbest metin faturası oluşturma
description: Bu konuda, serbest metin faturalarının nasıl oluşturulacağı açıklanmaktadır.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6e9578d9b2d61f241ab5e92fc9740b88b80969f6
ms.sourcegitcommit: 411874545d7c326fc4aa877948a059371f0ccb3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392897"
---
# <a name="create-a-free-text-invoice"></a>Serbest metin faturası oluşturma

[!include [banner](../includes/banner.md)]

Bu konuda, serbest metin faturalarının nasıl oluşturulacağı açıklanmaktadır. Prosedür için **USMF** demo şirketini kullanın.

## <a name="create-a-free-text-invoice"></a>Serbest metin faturası oluşturma

1. **Alacak hesapları (veya Satış Muhasebe Defteri) \> Faturalar \> Tüm serbest metin faturaları**'na gidin.
2. **Yeni**'yi seçin.
3. **Müşteri hesabı** alanında bir değer seçin.

    * Varsayılan olarak müşteri hesabı olarak seçilen hesap fatura hesabı olarak kullanılır.
    * Fatura deftere nakledilmediyse muhasebe durumunun başlangıç değeri **İşlemde** olur.
    * Fatura numarası fatura deftere nakledildiğinde atanır.
    * Tek Euro Ödemeleri Alanı (SEPA) yönergelerini kullanıyorsanız otomatik ödeme yönergesi müşteri hesabını seçtiğinizde otomatik olarak girilir.

4. **Açıklama** alanında bir değer girin.
5. **Ana hesap** alanında, boyutları olmayan bir hesap numarası belirtin. Boyutları bu konunun ilerleyen bölümlerinde gireceksiniz.

    Ayrıca ana hesap için bir veya daha fazla karakter girebilir ve hesabı bulmak için arama özelliğini kullanabilirsiniz.

6. Ana hesaba boyutlar eklemek için **Satır ayrıntıları** hızlı sekmesini seçin.
7. **Mali boyutlar satırı** sekmesini seçin.

    * Boyutlar yalnızca seçilen satır için kullanılır.
    * Satış vergisi grubu, müşteriden doldurulur. Müşterinin satış vergisi grubu yoksa ana hesaptan alınan satış vergisi grubu kullanılır.
    * Madde satış vergisi grubu ana hesaptan doldurulur. Ana hesapta madde satış vergisi grubu yoksa, Genel muhasebe satış vergisi parametrelerinde belirtilen madde satış vergisi grubu kullanılır.

8. İsteğe bağlı: **Miktar** alanına bir sayı girin.
9. İsteğe bağlı: **Birim fiyatı** alanına bir sayı girin.

    Tutar, miktarla birim fiyatı çarpılarak hesaplanır. Ancak kendiniz bir tutar girerek hesabı geçersiz kılabilirsiniz.

10. Fatura için hesaplanan satış vergisini görüntülemek için **Satış vergisi** öğesini seçin.

    Bu sayfada satış vergisi tutarlarını görüntüleyebilir veya **Ayarlama** sekmesinde tutarları geçersiz kılabilirsiniz.

11. **Tamam**'ı seçin.
12. Faturanıza masraf eklemek için **Masraflar** öğesini seçin.
13. **Masraf kodu** alanına bir değer girin.
14. **Masraf değeri** alanına bir sayı girin.
15. Sayfayı kapatın.
16. Fatura ayrıntılarının ve toplamların bir özetini görüntülemek için **Toplamlar** öğesini seçin.
17. **Kapat**'ı seçin.
18. Faturayı deftere nakletmek için **Deftere naklet**'i seçin. Gerçekte deftere nakletmeden önce iptal etme olanağınız vardır.

    * Fatura yazdırmanın zamanlamasını değiştirebilirsiniz. Her faturayı güncelleştirildiğinde yazdırmak için **Geçerli**'yi seçin. Tüm faturalar güncelleştirildikten sonra yazdırmak için **Sonra**'yı seçin.
    * Fatura deftere nakledilmeden önce müşterinin kredi limitinin doğrulama yöntemini değiştirmek için **Kredi limiti türü** alanındaki değeri değiştirin.
    * **Alacak hesapları parametreleri** sayfasındaki **Güncelleştirmeler** sekmesinde hata oluştuğunda (**Alacak hesapları > Kurulum > Alacak hesapları parametreleri**), serbest metin faturası deftere naklini durdurmak için bunu seçebilirsiniz. Bir hata oluştuğunda serbest metin faturalarının deftere naklini durdurmak için **İlk hatada serbest metin faturalarının deftere naklini durdur** parametresi için **Evet**'i seçin. Bir toplu işte deftere nakil işlemi söz konusu ise, bir hata deftere nakil işlemini durdurur ve toplu iş durumu **Hata** olarak ayarlanır. Bu seçenek belirlenmezse, deftere nakil işlemi deftere nakil hatası bulunan bir faturayı atlar ve başka Faturalar deftere nakletmeye devam eder. Bir toplu işte deftere nakil işlemi söz konusu ise, deftere nakil hatası diğer faturaların deftere nakledilmesini engellemez. Toplu iş durumu **Sonlandırıldı** olur. Toplu iş geçmişinde gözden geçirilmek üzere ayrıntılı bir deftere nakil işlemi raporu kullanılabilir olacak.
    * Faturayı yazdırmak için seçeneği **Evet** olarak ayarlayın.
    * Faturayı deftere nakletmek için seçeneği **Evet** olarak ayarlayın. Faturayı nakletmeden yazdırabilirsiniz.

19. **Tamam**'ı seçin.

## <a name="copy-lines"></a>Satırları kopyala
Serbest metin faturasında satırları kopyalamak için bir veya birden fazla satırı seçin ve **Seçili satırları kopyala** seçeneğini belirleyin. Alınacak kopya sayısını belirtebilir, notları ve ekleri de kopyalayabilirsiniz. Dağıtımları kopyalayabilir veya deftere naklederken yeniden oluşturulmalarına izin verebilirsiniz.

Satırları kopyaladıktan sonra bilgilerde ihtiyacınız olan düzenlemeleri yapabilirsiniz.

## <a name="create-a-free-text-invoice-from-a-template"></a>Şablondan serbest metin faturası oluşturma
Şablondan serbest metin faturası oluşturabilirsiniz. **Fatura** sekmesinde **Şablondan yeni** öğesini seçtiğinizde yeni serbest metin faturası için bir şablon adı ve müşterinin hesabını seçebilirsiniz. Müşterinin ödeme yöntemi ve ödeme koşulları gibi varsayılan değerler, müşteriden otomatik olarak doldurulabilir veya şablonda kaydedilmiş değerleri kullanabilirsiniz.

Yeni bir serbest metin faturası oluşturulur ve ihtiyacınız olan değerleri düzenleyebilirsiniz.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>Serbest metin faturaları için iş akışı durumunu Kurtarılamaz'dan Taslağa sıfırlama
Kurtarılamayan bir hata nedeniyle durdurulan bir iş akışı örneği, iş akışı durumu **Düzeltilemez** olacaktır. Müşteri serbest metin faturası iş akışının durumu **Kurtarılamaz** ise iş akışı eylemlerinden **Geri çağır**'ı seçerek bunu **Taslak** olarak sıfırlayabilirsiniz. Sonra, müşteri serbest metin faturasını düzenleyebilirsiniz. **Özellik yönetimi** sayfasında **Müşteri serbest metin faturalarının iş akışı durumunu Düzeltilemez durumundan Taslak durumuna sıfırlama** parametresi açıksa bu özellik kullanılabilir.

**İş akışı geçmişi** sayfasını kullanarak iş akışı durumunu **Taslak** olarak sıfırlayabilirsiniz. Bu sayfayı **Serbest metin faturasından** veya **Ortak > Sorgular > İş akışı**'ndan açabilirsiniz. İş akışı durumunu **Taslak** olarak sıfırlamak için **Geri çağır**'ı seçin. Ayrıca, **Serbest metin faturası** veya **Tüm serbest metin faturaları** sayfasında **Geri çağır** eylemini seçerek iş akışı durumunu **Taslak**'a sıfırlayabilirsiniz. İş akışı durumu **Taslak** olarak sıfırlandıktan sonra, **Serbest metin faturası** sayfasında düzenlenmeye açık hale gelir.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
