---
title: Serbest metin faturası oluşturma
description: Bu konuda, serbest metin faturalarının nasıl oluşturulacağı açıklanmaktadır.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 726d4979059417871a00626c55da32fa4286cb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991129"
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
    * Faturayı yazdırmak için seçeneği **Evet** olarak ayarlayın.
    * Faturayı deftere nakletmek için seçeneği **Evet** olarak ayarlayın. Faturayı nakletmeden yazdırabilirsiniz.

19. **Tamam**'ı seçin.

## <a name="copy-lines"></a>Satırları kopyala
Serbest metin faturasında satırları kopyalamak için bir veya birden fazla satırı seçin ve **Seçili satırları kopyala** seçeneğini belirleyin. Alınacak kopya sayısını belirtebilir, notları ve ekleri de kopyalayabilirsiniz. Dağıtımları kopyalayabilir veya deftere naklederken yeniden oluşturulmalarına izin verebilirsiniz.

Satırları kopyaladıktan sonra bilgilerde ihtiyacınız olan düzenlemeleri yapabilirsiniz.

## <a name="create-a-free-text-invoice-from-a-template"></a>Şablondan serbest metin faturası oluşturma
Şablondan serbest metin faturası oluşturabilirsiniz. **Fatura** sekmesinde **Şablondan yeni** öğesini seçtiğinizde yeni serbest metin faturası için bir şablon adı ve müşterinin hesabını seçebilirsiniz. Müşterinin ödeme yöntemi ve ödeme koşulları gibi varsayılan değerler, müşteriden otomatik olarak doldurulabilir veya şablonda kaydedilmiş değerleri kullanabilirsiniz.

Yeni bir serbest metin faturası oluşturulur ve ihtiyacınız olan değerleri düzenleyebilirsiniz.
