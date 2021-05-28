---
title: Muhasebe veya raporlama para birimini değiştirme
description: Bu konuda, muhasebe veya raporlama para biriminin nasıl değiştirileceği ya da genel muhasebe kurulumuna raporlama para biriminin nasıl ekleneceği açıklanmaktadır.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 38b2cdb618d92dca7909a145e7fc07ddfc5f4d45
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017067"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Muhasebe veya raporlama para birimini değiştirme

[!include [banner](../includes/banner.md)]

Bu konuda, muhasebe veya raporlama para biriminin nasıl değiştirileceği ya da genel muhasebe kurulumuna raporlama para biriminin nasıl ekleneceği açıklanmaktadır.

## <a name="symptom"></a>Belirti

Muhasebe veya raporlama para birimini değiştirmek ya da genel muhasebe kurulumuna raporlama para birimi eklemek istiyorsunuz. Bu durum genellikle aşağıdaki senaryolarda ortaya çıkar:

- Tüzel kişilik ayarlanırken yanlış muhasebe veya raporlama para birimi belirtilmiş. Şimdi bu para birimini değiştirmek istiyorsunuz.
- Tüzel kişilik ayarlanırken raporlama para birimi belirtilmemiş. (Raporlama para birimi isteğe bağlıdır.) Şimdi bir raporlama para birimi eklemek istiyorsunuz.

Daha önce Çift para birimi özelliğini kullanmayan bir kuruluş bunu kullanmaya başlamak istiyor. Bu sorun genellikle aşağıdaki senaryolarda ortaya çıkar.

- Tüzel kişilik ayarlanırken raporlama para birimi belirtilmiş ancak kuruluş şimdi raporlama para birimini kaldırmak istiyor.
- Kuruluş, Microsoft Dynamics 365 Finance'e yükseltiyor veya geçiyor ve muhasebe ya da raporlama para birimini değiştirmek istiyor.

## <a name="resolution"></a>Çözüm

Dikkate alınması gereken en önemli nokta, işlemlerin (fiili veya bütçe) muhasebe kurulumu için tüzel kişilikte deftere nakledilip nakledilmediğidir. **İşlemler (fiili veya bütçe) tüzel kişilikte deftere nakledildiyse muhasebe veya raporlama para birimini değiştiremez ya da raporlama para birimi ekleyemezsiniz.** İşlemlerin deftere nakledilip nakledilmediğine bağlı olarak aşağıda bulunan bölümlerden birindeki adımları izleyin.

### <a name="no-transactions-have-been-posted"></a>Hiçbir işlem deftere nakledilmemiş

1. Para birimlerini güncelleştirdiğiniz tüzel kişilikte **Genel muhasebe \> Genel muhasebe kurulumu \> Genel muhasebe** bölümüne gidin.
2. **Genel muhasebe** sayfasında, **Düzenle**'yi seçin.
3. **Para Birimi** Hızlı Sekmesi'nde, tüzel kişilikte kullanılacak muhasebe para birimini ve raporlama para birimini seçin.
4. **Kaydet**'i seçin.

**Genel muhasebe** sayfasında muhasebe para birimi ve raporlama para birimi alanları kullanılamıyorsa tüzel kişilikte bir veya birden fazla işlem (fiili veya bütçe) deftere nakledilmiştir. Bu nedenle, para birimleri değiştirilemez. Bu durumda, sonraki bölümdeki adımları izleyin.

### <a name="transactions-have-been-posted"></a>İşlemler deftere nakledilmiş

**Tüzel kişilikte işlemler deftere nakledildiyse muhasebe ve raporlama para birimlerini değiştirmenin veya eklemenin tek yolu, doğru para birimleri olan yeni bir tüzel kişilik oluşturmaktır.** Bu işlemi yapmaya yardımcı olmak için sistemdeki Veri yönetimi, kurulum kayıtlarını ve ana kayıtları geçerli tüzel kişilikten yeni bir tüzel kişiliğe kopyalamanıza olanak sağlar.

Muhasebe ve raporlama para birimlerindeki değişiklikler sistem geneline yayılır. Yalnızca Genel muhasebeyi değil, ayrıca her yardımcı defteri (Alacak hesapları, Borç hesapları, Stok, Proje vb.), her bağımsız yazılım satıcısı (ISV) çözümünü ve tutarları depoladığınız uzantıları etkiler.

Her tutarı bulma ve farklı bir para birimine dönüştürme işlemi, hataya tabidir. Bu nedenle mühendislik ekibi, muhasebe ve raporlama para birimlerini değiştiren veya ekleyen bir betiği onaylamaz. Ek olarak, Microsoft Dynamics AX 2012 için kullanılabilen bir araç, muhasebe ve raporlama para birimlerini değiştirmenize veya eklemenize olanak sağlasa da bu araç, AX 2012 R3 ve Finance için kullanımdan kaldırılmıştır.

Kurulum verilerini ve ana verileri geçerli tüzel kişilikten yeni bir tüzel kişiliğe kopyalamak için aşağıdaki adımları izleyin.

1. **Çalışma Alanları \> Veri yönetimi**'ne gidin.
2. **İçeri/Dışarı Aktarma** grubu altında **Şablonlar**'ı seçin.
3. Şablonların kullanılabilir olduğundan emin olun. Kullanılabilir şablon yoksa **Varsayılan şablonları yükle**'yi seçin ve şablonların oluşturulmasını bekleyin.
4. **Veri yönetimi** çalışma alanına dönün.
5. **Tüzel kişiliğe kopyala**'yı seçin.
6. Bir grup adı ve açıklaması girin.
7. **Kaynak tüzel kişilik** alanında, verilerin kopyalanacağı tüzel kişiliği seçin.
8. **Hedef tüzel kişilikler** Hızlı Sekmesi'nde, kaynak tüzel kişilik verilerini kopyalayabileceğiniz yeni bir tüzel kişilik oluşturmak için **Tüzel kişilik oluşturma**'yı seçin. Verileri mevcut bir tüzel kişiliğe kopyalamak için **Var olanı seç** seçeneğini belirleyin.
9. İsteğe bağlı: **Numara serilerini kopyala** alanını **Evet** olarak ayarlayın. (Bu adım, verileri kopyaladığınızda önerilir.)
10. **Seçili varlıklar** alanında, **Şablon ekle**'yi seçin.
11. Kullanılacak şablonları seçin. Yeni tüzel kişilik için önerilen şablonlar arasında **025 - Genel Muhasebe** ve **Mali Öğeler** vardır. Bunlardan birinin gereksinimlerinize uygun olup olmadığını belirlemek için tüm kullanılabilir şablonları incelemenizi öneririz.
12. Seçili varlıkların oluşturulacağı bir toplu işlem başlatmak ve bu varlıkları hedef tüzel kişiliğe kopyalamak için **Tüzel kişiliğe kopyala**'yı seçin.
13. İşlem tamamlandıktan sonra işlemler deftere nakledilmeden önce genel muhasebeye gidin ve bu konuda daha önce açıklandığı gibi muhasebe ve raporlama para birimlerini güncelleştirin.

Muhasebe veya raporlama para birimini değiştirebilmek için yeni bir tüzel kişilik oluşturduysanız başlangıç bakiyelerinin eski tüzel kişiliğin para birimlerinden yeni para birimlerine çevrildiğini doğrulayın.

Önceki adımları gösteren bir video için bkz. [Tüzel Kişiliğe Kopyalama](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
