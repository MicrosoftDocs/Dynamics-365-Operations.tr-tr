---
title: Otomatik hareketler için hesaplar
description: Bu konu, otomatik hareketler için hesapların Microsoft Dynamics 365 ile deftere nakil için nasıl kullanıldığını açıklar ve otomatik hareketler için anahtar hesaplar için örnekler sağlar.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cecbeb769235e525390cc7a66800a9b0d55d78a9
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014084"
---
# <a name="accounts-for-automatic-transactions"></a>Otomatik hareketler için hesaplar

**Otomatik hareketler için hesaplar** sayfasında (**Genel muhasebe &gt; Deftere nakil ayarı &gt; Otomatik hareketler için hesap**), sistemdeki her bir nakil türü için kullanılan varsayılan ana hesabı belirlemek için kullanılır. Bir modüle özel veya özelliğe özgü bir sayfada birçok deftere nakil türü konfigüre edilebilir ancak, bazı deftere nakil türleri yalnızca **Otomatik hareketler için hesaplar** sayfasında konfigüre edilebilir.

Örneğin, **Müşteri bakiyesi** deftere nakli türü için kullanılan ana hesabı **Müşteri deftere nakil profili** sayfasındaki **Özet** alanında belirtebilir ve her bir müşteri profili için farklı bir ana hesap kullanabilirsiniz. Bu şekilde, nakiller üzerinde daha ayrıntılı denetiminiz olur. Diğer bir yandan, hata hesabını yalnızca **Otomatik hareketler için hesaplar** sayfasından belirleyebilirsiniz.

**Otomatik hareketler için hesaplar** sayfasını yeni bir tüzel kişilikte açtığınızda, hesap listesi boş olacaktır. **Varsayılan türleri oluştur** düğmesini seçerek sayfada konfigüre edilecek en genel deftere nakil tiplerini ekleyebilirsiniz. Böylece, her bir satır için **Ana hesap** alanında ana hesabı seçebilirsiniz. **Ana hesap** alanını bir deftere nakil için boş bırakırsanız ve modüle özel veya özelliğe özgü bir sayfada ana hesap konfigüre etmediyseniz, deftere nakil türünü kullanan bir hareketi deftere naklettiğinizde hata iletisi alırsınız. İleti genellikle, "\[Deftere nakil türü hesabı\] bulunamıyor" olur.

## <a name="default-posting-types"></a>Varsayılan deftere nakil türleri

Aşağıdaki tablo, **Otomatik hareketler için hesaplar** sayfasında **Varsayılan türleri oluştur** seçeneğini belirlediğinizde oluşturulan varsayılan deftere nakil türleri örneklerini gösterir. Örnek ana hesapları ve açıklamaları gösterir. "Borç/Alacak?" sütun, hareketin tipik olarak bir borç veya alacak mı deftere nakletmediğini gösterir. Bazı durumlarda, bir hareket bir borç veya alacak deftere nakledebilir. "Temizleme hesabı" sütunu, deftere nakil türünün bir temizleme hesabı olduğunu belirtir. Deftere nakil türü bir temizleme hesabı ise hesaba nakledilen tutar, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanacağını gösterir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Raporlama para birimi cinsinden kuruş farkı | 618160 | Sair Gider | Gider | İkisi birden | Hayır | Bu deftere nakil tipi bir döviz farkı, yabancı para birimindeki bir hareket tutarı raporlama para birimine çevrildiğinde ortaya çıktığında kullanılır. |
| Muhasebe para birimi cinsinden kuruş farkı | 618160 | Sair Gider | Gider | İkisi birden | Hayır | Bu deftere nakil tipi bir döviz farkı, muhasebe birimindeki bir hareket tutarı raporlama para birimine çevrildiğinde ortaya çıktığında kullanılır. |
| Hatalı hesap | 999999 | Hatalı Hesap | Gider | İkisi birden | Hayır | Bu deftere nakil türü, sistemde hata oluştuğunda kullanılır. Hesap, her dönemde doğrulanmalı ve tüm hatalar çözülmelidir. |
| Yıl sonu sonucu | 300160 | Yedek Akçe | Öz varlık | İkisi birden | Hayır | Bu deftere nakil türü, **Kar ve zarar** tipindeki hesap bakiyesini yıl sonu sonucu için seçilen ana hesaba taşımak amacıyla yıl sonu kapatma işlemi çalıştırıldığında kullanılır. |
| Müşteri nakit iskontosu | Geçerli değil | Geçerli değil | Geçerli değil | Geçerli değil | Hayır | **Otomatik hareketler için hesaplar** sayfasında tanımlanan deftere nakil tipi kullanılmaz. Nakit iskontoları alacak hesaplarında konfigüre edildiğinde bir ana hesap gereklidir.|
| Satıcı nakit iskontosu | Geçerli değil | Geçerli değil | Geçerli değil | Geçerli değil | Hayır | **Otomatik hareketler için hesaplar** sayfasında tanımlanan deftere nakil tipi kullanılmaz. Nakit iskontoları borç hesaplarında konfigüre edildiğinde bir ana hesap gereklidir. |

## <a name="additional-posting-types"></a>Ek deftere nakil türleri

Aşağıdaki tabloda, ilgili özellikleri kullanmayı planlıyorsanız konfigüre edilecek ek deftere nakil türü örnekleri gösterilmektedir. Bu deftere nakil türleri için başka bir modülde deftere nakil profili konfigürasyonu yok. "Borç/Alacak?" sütun, hareketin tipik olarak bir borç veya alacak mı deftere nakletmediğini gösterir. Bazı durumlarda, bir hareket bir borç veya alacak deftere nakledebilir. "Temizleme hesabı" sütunu, deftere nakil türünün bir temizleme hesabı olduğunu belirtir. Deftere nakil türü bir temizleme hesabı ise hesaba nakledilen tutar, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanacağını gösterir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Konsolidasyon farkı için bilanço hesabı | 801200 | Kazanç ve Kayıp - Yeniden değerleme | Gider | İkisi birden | Hayır | Para birimi yeniden değerlemesi içeren bir konsolidasyon gerçekleştirdiğinizde bu deftere nakil türü, yeniden değerleme sırasında gerçekleşen kuruş farkları olduğunda kullanılır. |
| Konsolidasyon farkları için kar ve zarar hesabı | 801200 | Kazanç ve Kayıp - Yeniden değerleme | Gider | İkisi birden | Hayır | Para birimi yeniden değerlemesi içeren bir konsolidasyon gerçekleştirdiğinizde bu deftere nakil türü, yeniden değerleme sırasında gerçekleşen kuruş farkları olduğunda kullanılır. |
| Birimler arası - borç | 133500 | Birimler Arası Alacak | Varlık | Borç | Hayır | Bu deftere nakil türü, **Genel muhasebe** sayfasında bir bilanço boyutu seçtiğinizde ve deftere nakledilen bir harekette boyut bakiyesi olmadığında kullanılır. |
| Birimler arası - alacak | 233500 | Birimler Arası Borç | Pasif | Kredi | Hayır | Bu deftere nakil türü, **Genel muhasebe** sayfasında bir bilanço boyutu seçtiğinizde ve deftere nakledilen bir harekette boyut bakiyesi olmadığında kullanılır. |
