---
title: Borç hesapları deftere nakilleri
description: Bu konu, deftere nakillerin Borç hesaplarında nasıl konfigüre edildiğini açıklar ve deftere nakil konfigürasyonlarının örneklerini sağlar.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb3ebad31c9f41e405b9fc31a0f71df05fa1cc60
ms.sourcegitcommit: 10b85a09e8a550155a69aa2a8877a7c88b887242
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/20/2022
ms.locfileid: "8014473"
---
# <a name="accounts-payable-posting"></a>Borç hesapları deftere nakli

[!include [banner](../includes/banner.md)]

**Borç hesapları** modülü için birincil deftere nakil profili satıcı deftere nakil profilidir. Bu deftere nakil profili, satıcı bakiyeleri genel muhasebeye nakledilirken kullanılan özet hesabı belirler. Özet hesabı bir ana hesaptır. Ayrıca, Borç hesapları ticari hesabı olarak da anılır.

Daha fazla bilgi için [Satıcı deftere nakil profilleri](../accounts-payable/vendor-posting-profiles.md) konusuna bakın.

Satıcı deftere nakil profilinin yanı sıra, Borç hesaplarında da bulunan çeşitli deftere nakil yapılandırmaları. Aşağıdaki bölümler bu diğer deftere nakil konfigürasyonları hakkında daha fazla bilgi sağlar.

## <a name="methods-of-payment-posting-accounts"></a>Ödeme yöntemleri deftere nakil hesapları

Ödeme yöntemleri bir ödemenin genel muhasebeye nasıl nakledileceğini tanımlar. Ayrıca ödeme çıktısının davranışını da kontrol ederler. Genellikle, kuruluşunuzun yaptığı her ödeme türü (örneğin, nakit, çek, kredi kartı, para siparişi ve havale) için tek bir ödeme yöntemi oluşturulur.

**Ödeme yöntemleri** sayfasındaki **Genel** hızlı sekmesindeki **Deftere nakil** bölümündeki alanlar ( **Borç hesapları > Ödeme Kurulumu > Ödeme yöntemleri**) bir ödemenin genel muhasebeye nasıl nakledileceğini kontrol eder. Önce **Hesap türü** alanında bir değer seçmeniz gerekir. Seçtiğiniz hesap türü **Ödeme hesabı** alanının davranışını denetler. **Hesap türü** alanında **Banka**'yı seçmenizi ve sonra da **Ödeme hesabı** alanında banka hesabını seçmenizi öneririz. Yaklaşımın yararı, sistemin ödemeyi ve diğer nakit ilişkili işlemleri destekleyen banka genel muhasebeye nakletmesini sağlar. Aşağıdaki tabloda, **Nakit ve banka yönetimi** modülünü kullanıyorsanız, deftere nakil profili konfigürasyonuyla ilgili bir örnek gösterilmektedir.

| Deftere nakil türü | Hesap türü | Ödeme hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Banka | Banka | Bank of America | Bir kıymete bağlı banka hesabı | Borç | Hayır | Her ödeme yöntemi için, ana hesabı **Ödeme hesabı** alanına girin. |

Nakit ve banka yönetimini kullanmayı planlamıyorsanız, **Hesap türü** alanında **Genel muhasebe**'yi seçmeniz ve sonra **Ödeme hesabı** alanında ana hesabı seçmeniz gerekir. Aşağıdaki tabloda, Nakit ve banka yönetimi **kullanmıyorsanız**, deftere nakil profili konfigürasyonuyla ilgili bir örnek gösterilmektedir.

| Deftere nakil türü | Hesap türü |Ödeme hesap örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Genel muhasebe | Genel muhasebe | 100100: Bank of America | Varlık | Borç | Hayır | Her ödeme yöntemi için, ana hesabı **Ödeme hesabı** alanına girin. |

## <a name="bridging-accounts"></a>Bağlantı hesapları

Bağlantı deftere nakli, ödemeler deftere nakledilirken kullanılan iki adımlı bir işlemdir. Bu, örneğin, sıfır bakiye banka hesaplarıyla kullanılabilen isteğe bağlı bir özelliktir. Daha düzgün ve güncel banka mutabakat süreci sağlamaya yardımcı olabilir. İlk adımda, bir ödeme geçici bir hesaba (bağlantı hesabı) nakledilir. İkinci adımda, deftere nakledilen giriş ters kaydedilir ve ödeme onaylandığında banka hesabına nakledilir. Aşağıdaki tabloda, bağlantı deftere nakli için deftere nakil profili konfigürasyonunda bir örnek gösterilmektedir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Genel muhasebe günlüğü | 130725 | Onaylanmamış Nakit | Pasif | Borç | Evet | Her ödeme yöntemi için, ana hesabı **Bağlantı hesabı** alanına girin. |

Daha fazla bilgi için bkz. [Bağlantı ödemeleri kurulumu ve işleme](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Müşteri nakit iskontoları deftere nakil hesapları

Kuruluşunuz, hızlı ödeme için iade edilen satıcılardan gelen nakit iskontoları alıyorsa nakit iskontosu kodlarını konfigüre etmelisiniz ve iskontoların genel muhasebeye nasıl nakledileceğini belirtmelisiniz. Bir müşteri nakit iskontosunu deftere nakletmek için kullanılan ana hesabı belirtmek için çeşitli seçenekler kullanılabilir.

Daha fazla bilgi için bkz. [Nakit iskontoları](../cash-bank-management/cash-discounts.md).

## <a name="payment-fee-posting-accounts"></a>Ödeme masrafı deftere nakil hesapları

Ödeme masrafları, bir dizi koşul geçerliyse otomatik olarak bir satıcı ödemesine ücret eklemenizi sağlar. Ödeme masrafları satıcıya ödenebilir veya bir masraf olarak banka hesabınıza nakledilebilir. Burada bazı örnekler verilmiştir:

- Kredi kartı kullanarak ödeme yaptığınızda, satıcı ödeme toplamının yüzde 3'ünü ücretlendirir.
- Yaptığınız her bir havale aktarımı için bankanızın ücreti $1,00'dır ve bu gider olarak gösterilir.

Bir satıcı ödeme ücreti konfigüre ettiğinizde, **Gider** alanını **Satıcı** olarak ayarlarsanız, **Ana hesap** alanı kullanılamaz hale gelir ve sistem masrafı deftere nakletmek için satıcı deftere nakil profilini kullanır. **Gider** alanını **Genel muhasebe** olarak ayarlarsanız, **Ana hesap** alanını ödeme masrafının deftere nakledileceği ana hesaba ayarlamanız gerekir. Genel olarak bu ana hesap bir gider hesabıdır. Aşağıdaki tabloda, ödeme ücreti deftere nakli için deftere nakil profili konfigürasyonunda bir örnek gösterilmektedir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Genel muhasebe günlüğü | 618190 | Banka Masrafı Gideri | Gider | Borç | Hayır | **Gider** alanında **Genel muhasebe** seçilmişse, **Ödeme ücreti** sayfasındaki **Ana hesap** alanında bu hesabı seçin. |

Daha fazla bilgi için bkz. [Satıcı ödeme ücretlerini tanımlama](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Masraf kodu deftere nakil hesapları

Satır maddelerine ek olarak satınalma tutarlarını izlemeniz gerekiyorsa, masraf kodlarını kullanabilirsiniz. Örneğin tedarikçiniz navlun ve işleme ücretleri uygulayabilir veya bazı navlun ve işleme ücretlerini dahili olarak gider diye gösterebilir. Bu tutarların gider hesaplarına nakledilip nakledilmeyeceğini veya maddelerin maliyetine eklenip eklenmeyeceğini belirtebilirsiniz.

Alacak hesapları ve Borç hesapları için masraf kodları oluşturabilirsiniz. Masraf kodu konfigüre ettiğinizde, deftere nakil işlemini tanımlamanız gerekir. Deftere nakil, hem borç hesabını hem de alacak hesabını denetler. Masraf kodları oluşturduğunuzda, her gider kodu için kullanılan deftere nakil türünü seçebilirsiniz. Aşağıdaki tabloda, masraf kodları sayfasında borç hesapları için tipik **Gider kodları** örnekleri verilmiştir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Satınalma bedeli | Alanı boş bırakın. | Geçerli değil | Ürün | Borç | Hayır | **Madde için satınalma ücreti örneği:** </p><ul><li>**Borç türü** alanı = **Madde**</li><li>  **Alacak türü** alanı = **Müşteri/Satıcı**.</li><li> Madde deftere nakli, stok deftere nakil profilinden ana hesabı kullanır. |
| Sipariş, navlun | 600120 | Navlun Giriş | Gelir | Borç | Hayır | **Satıcıya ödenen navlun örneği:** </p><ul><li>**Borç türü** alanı = **Genel muhasebe hesabı**</li><li> **Alacak türü** alanı = **Müşteri/Satıcı** |
| İndirim\* | 503160 | Satıcı İndirimi (Karşı SMM)| Gider | Kredi | Hayır | **Satıcı indirimi örneği:**</p><ul><li>**Borç türü** alanı = **Müşteri/Satıcı**</li><li>**Alacak türü** alanı = **Genel muhasebe hesabı** |

\* İndirim örneği için deftere nakil, yalnızca bir gider kodu bir satınalma siparişi başlığına veya satırına eklendiğinde kullanılır. Microsoft Dynamics 365 Supply Chain Management'ta bulunan gelişmiş indirim işlevleri, indirimler için daha fazla denetim ve otomasyon sağlar. Daha fazla bilgi için bkz. [Satıcı indirimleri](../../supply-chain//procurement/vendor-rebates.md).

Üstteki tabloda, masraf kodları için kullanılabilen üç genel deftere nakil türü örneği gösterilir. Bir kılavuz ve örnek koleksiyonu olarak kullanılmalıdır. Kullanılabilecek tüm olası kombinasyonlar veya deftere nakil türleri için kapsamlı bir liste sağlamaz.

Daha fazla bilgi için bkz. [Gider kodu oluşturma](../accounts-receivable/create-charges-codes.md).
