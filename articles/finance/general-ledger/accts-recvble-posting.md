---
title: Alacak hesapları deftere nakli
description: Bu makalede, Alacak hesaplarında deftere nakillerin nasıl yapılandırıldığı açıklanır ve deftere nakil yapılandırmalarına örnekler verilir.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d679595a1f702c4e3ade138a87c817d245fcf79
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324344"
---
# <a name="accounts-receivable-posting"></a>Alacak hesaplarının deftere nakli

[!include [banner](../includes/banner.md)]

**Alacak hesapları** modülünün birincil deftere nakil profili müşteri deftere nakil profilidir. Bu deftere nakil profili, müşteri bakiyeleri genel muhasebeye nakledildiğinde kullanılan özet hesabı belirler. Özet hesabı bir ana hesaptır. Alacak hesapları ticari hesabı olarak da adlandırılır.

Müşteri ve genel muhasebe hesaplarının bakiyelerinin mutabakatına yardımcı olmak üzere deftere nakilden sonra **Müşteri - genel muhasebe mutabakatı** raporu kullanılabilir. Rapor, müşteri deftere nakil profili için özet hesapta bulunan bilgileri kullanır. Belge için oluşturulan muhasebeden özet hesabı kullanmaz. Hareketleri deftere naklettikten sonra müşteri deftere nakil profilinde veya müşteriye atanan müşteri grubunda değişiklik yaparsanız rapor, müşteri ve genel muhasebe hesabı bakiyesi arasındaki farkları görüntüleyebilir. Yalnızca farkları olan satırları ve müşteri hesaplarının ve genel muhasebe hesabının sıfır olduğu satırların tümünü görmek için raporu yazdırırken **Yalnızca farklar** parametresini seçin.

Daha fazla bilgi için [Müşteri deftere nakil profilleri](../accounts-receivable/customer-posting-profiles.md) konusuna bakın.

Alacak hesaplarında, müşteri deftere nakil profilinin yanındaki çeşitli deftere nakil yapılandırmaları kullanılabilir. Aşağıdaki bölümler bu diğer deftere nakil konfigürasyonları hakkında daha fazla bilgi sağlar.

## <a name="posting-accounts-for-methods-of-payment"></a>Ödeme yöntemleri için deftere nakil hesapları

Ödeme yöntemleri bir ödemenin genel muhasebeye nasıl nakledileceğini tanımlar. Ayrıca ödeme çıktısının davranışını da kontrol ederler. Genellikle, kuruluşunuzun kabul ettiği her ödeme türü (örneğin, nakit, çek, kredi kartı, talimatlı ödeme ve banka havalesi) için bir ödeme yöntemi oluşturulur.

**Genel** hızlı sekmesindeki **Deftere Nakil** bölümündeki alanlar, bir ödemenin genel muhasebeye nasıl nakledileceğini denetler. Önce **Hesap türü** alanında bir değer seçmeniz gerekir. Seçtiğiniz hesap türü **Ödeme hesabı** alanının davranışını denetler. **Hesap türü** alanında **Banka**'yı seçmenizi ve sonra da **Ödeme hesabı** alanında banka hesabını seçmenizi öneririz. Bu yaklaşımın yararı, sistemin ödemeyi mutabakatı ve nakitle ilgili diğer süreçleri destekleyen Banka alt defteri'ne nakledecek olmasıdır. Aşağıdaki tabloda, **Nakit ve banka yönetimi** modülünü kullanıyorsanız, deftere nakil profili konfigürasyonuyla ilgili bir örnek gösterilmektedir.

| Deftere nakil türü | Hesap türü | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Banka | Banka | Bank of Contoso | Bir kıymete bağlı banka hesabı | Kredi | Hayır | Her ödeme yöntemi için, ana hesabı **Ödeme hesabı** alanına girin. |

Nakit ve banka yönetimini kullanmayı planlamıyorsanız **Hesap türü** alanında **Genel Muhasebe**'yi ve ardından **Ödeme hesabı** alanında ana hesabı seçmelisiniz. Nakit ve banka yönetimi kullanmıyorsanız aşağıdaki tabloda deftere nakil profili yapılandırmasına bir örnek gösterilmektedir.

| Deftere nakil türü | Hesap türü | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Genel muhasebe | Genel muhasebe | 100100: Bank of Contoso | Varlık | Kredi | Hayır | Her ödeme yöntemi için, ana hesabı **Ödeme hesabı** alanına girin. |

## <a name="bridging-accounts"></a>Bağlantı hesapları

Bağlantı deftere nakli, ödemeler deftere nakledilirken kullanılan iki adımlı bir işlemdir. Bu, örneğin, sıfır bakiye banka hesaplarıyla kullanılabilen isteğe bağlı bir özelliktir. Daha düzgün ve güncel banka mutabakat süreci sağlamaya yardımcı olabilir. İlk adımda, bir ödeme geçici bir hesaba (bağlantı hesabı) nakledilir. İkinci adımda, deftere nakledilen giriş ters kaydedilir ve ödeme onaylandığında banka hesabına nakledilir. Aşağıdaki tabloda, bağlantı deftere nakli için deftere nakil profili konfigürasyonunda bir örnek gösterilmektedir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Genel muhasebe günlüğü | 130725 | Onaylanmamış Nakit | Pasif | Borç | Evet | Her ödeme yöntemi için, ana hesabı **Bağlantı hesabı** alanına girin. |

Daha fazla bilgi için bkz. [Bağlantı ödemeleri kurulumu ve işleme](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Müşteri nakit iskontoları için deftere nakil hesapları

Kuruluşunuz hızlı ödeme karşılığında müşterilere nakit iskontosu sunuyorsa nakit iskonto kodlarını yapılandırmanız ve iskontoların genel muhasebeye nasıl nakledilmesi gerektiğini belirtmeniz gerekir. Bir müşteri nakit iskontosunu deftere nakletmek için kullanılan ana hesabı belirtmek için çeşitli seçenekler kullanılabilir.

Daha fazla bilgi için bkz. [Nakit iskontoları](../cash-bank-management/cash-discounts.md).

## <a name="posting-accounts-for-payment-fees"></a>Ödeme ücretleri için deftere nakil hesapları

Ödeme ücretleri, bir dizi koşul uygulandığında müşteri ödemesine otomatik olarak ücret eklemenize olanak tanır. Ödeme ücretleri müşteriden tahsil edilebilir veya masraf olarak banka hesabınıza nakledilebilir. Burada bazı örnekler verilmiştir:

- Kredi kartı kullanarak ödeme yapıldıysa, müşterilerden ödeme toplamının yüzde 3'ü kadar ücret alırsınız.
- Bankanız, işlediğiniz her havale için sizden 1,00 ABD doları ücret alır ve banka havalesi masrafı oluşur.

Bir müşteri ödeme ücreti yapılandırdığınızda, **Gider** alanını **Müşteri** olarak ayarlarsanız, **Ana hesap** alanı kullanılamaz hale gelir ve sistem ücreti deftere nakletmek için müşteri deftere nakil profilini kullanır. **Gider** alanını **Genel muhasebe** olarak ayarlarsanız, **Ana hesap** alanını ödeme masrafının deftere nakledileceği ana hesaba ayarlamanız gerekir. Genel olarak bu ana hesap bir gider hesabıdır. Aşağıdaki tabloda, ödeme ücreti deftere nakli için deftere nakil profili konfigürasyonunda bir örnek gösterilmektedir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Genel muhasebe günlüğü | 618190 | Banka Masrafı Gideri | Gider | Borç | Hayır |  **Gider** alanında **Genel Muhasebe** seçiliyse, ödeme ücreti için **Ana hesap** alanında bu hesabı seçin. |

Daha fazla bilgi için bkz. [Müşteri ödeme ücretleri geliştir](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Masraf kodları için deftere nakil hesapları

Satır maddelerine ek olarak satış tutarlarını izlemeniz gerekiyorsa masraf kodlarını kullanabilirsiniz. Örneğin, müşterilerinizden navlun ve taşıma ücretleri alabilir veya bazı navlun ve taşıma ücretlerini dahili olarak masraflandırabilirsiniz. Bu tutarların gider hesaplarına nakledilip nakledilmeyeceğini veya maddelerin maliyetine eklenip eklenmeyeceğini belirtebilirsiniz.

Alacak hesapları ve Borç hesapları için masraf kodları oluşturabilirsiniz. Masraf kodu konfigüre ettiğinizde, deftere nakil işlemini tanımlamanız gerekir. Deftere nakil, hem borç hesabını hem de alacak hesabını denetler. Oluşturduğunuz her masraf kodu için kullanılan deftere nakil türünü seçebilirsiniz. Aşağıdaki tabloda, alacak hesapları için gider kodlarının tipik örnekleri gösterilmektedir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Ödeme masrafı | 411400 | Gelir – Ücretler | Gelir | Kredi | Hayır | **Yeterli olmayan fonlar için örnek:** Borç Müşteri/Satıcı ve Alacak Defteri hesabı |
| Sipariş, navlun | 403500 | Gelir – Navlun | Gelir | Kredi | Hayır | **Ücreti müşteriden alınan navlun örneği:** Borç Müşteri/Satıcı ve Alacak Defteri hesabı |
| İndirim\* | 403200 | İskonto | Gelir | Borç | Hayır | **Müşteri indirimi örneği:** Borç Genel Muhasebe hesabı ve Alacak Müşteri/Satıcı |

\* İndirim örneği için deftere nakil, yalnızca bir gider kodu bir satınalma siparişi başlığına veya satırına eklendiğinde kullanılır. Microsoft Dynamics 365 Supply Chain Management'ta bulunan gelişmiş indirim işlevleri, indirimler için daha fazla denetim ve otomasyon sağlar. Daha fazla bilgi için bkz. [Müşteri indirimleri](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Üstteki tabloda, masraf kodları için kullanılabilen üç genel deftere nakil türü örneği gösterilir. Bir kılavuz ve örnek olarak kullanılmalıdır. Kullanılabilecek tüm olası kombinasyonlar veya deftere nakil türleri için kapsamlı bir liste sağlamaz.

Daha fazla bilgi için bkz. [Gider kodu oluşturma](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Komisyonlar için deftere nakil hesapları

İsteğe bağlı olarak, sistemi belirli bir satış siparişinde bir satış temsilcisi veya bir satış temsilcisi grubu için komisyonları hesaplamak üzere yapılandırabilirsiniz. Bu işlevi etkinleştirirseniz, komisyonu hesaplamak için kullanılan deftere nakil hesabını yapılandırmanız gerekir. Bu yapılandırma, **Satış ve pazarlama** modülündeki **Komisyon deftere nakli** sayfasında yapılır.

Daha fazla bilgi için bkz. [Satış komisyonu kurallarını ayarlama](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).
