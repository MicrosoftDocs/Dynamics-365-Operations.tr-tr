---
title: Konum stoklama sınırları
description: Bu konu, konum stoklama limitlerinin işlevini açıklamaktadır.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e336b54b894669f8a49091473314e1d7d2639e5f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216993"
---
# <a name="location-stocking-limits"></a>Konum stoklama sınırları

[!include [banner](../includes/banner.md)]

Fiziksel ürünlerin volümetrik hesaplamaları için daha gelişmiş işlemleri kullanmak sorunda kalmadan ambar konumlarındaki yük kapasitesini denetlemek amacıyla **Konum stoklama limitleri** sayfasını (**Ambar yönetimi \> Kurulum \> Ambar \> Konum stoklama limitleri**) kullanabilirsiniz.

Konum stoklama limitlerinin amacı, bir konumun içerebileceği maksimum miktarı değerlendirmektir. Özelliği, her biri **Konum stoklama limitleri** sayfasında kendi sekmesi bulunan üç düzeyden herhangi birine ayarlayabilirsiniz:

- Ürünler
- Ürün çeşitleri
- Konteyner türleri

Her düzey için farklı alan değerleri tanımlayabilirsiniz. Sistem her satırın **Miktar** ve **birim** değerlerini esas alarak belirli bir konumun kapasitesini değerlendirir. İlk olarak en ayrıntılı eşleşen kaydı seçer. Örneğin, **Konum profil kodu** alanında değeri olan bir satır, yalnızca **Ambar** alanında değeri olan bir satırdan önce değerlendirilir. Kullanılan konum stoklama limiti kaydı için **Miktar** değeri temel alınarak, kalan kapasite de değerlendirilir.

Bu sayfanın **Ürünler** bölümünde, konum stoklama limitleri araması için aşağıdaki alan değerlerini tanımlayabilirsiniz:

- Ambar
- Yerleşim profili kodu
- Yer
- Paket boyutu kategorisi kodu
- Madde kodu
- Birim

> [!NOTE]
> Her konum stoklama limiti kaydı için bir **Birim** değeri tanımlamanız gerekmez. Konum kapasitesi hesaplamaları, stok birimi miktarlarını temel alacaktır. Kullanılan bir değer için birim dönüştürme tanımlanmamışsa, konum stoklama limiti kaydı, kendisi için başka bir **Madde numarası** değeri tanımlanmış gibi atlanacaktır.

## <a name="example--purchase-order-receiving"></a>Örnek: Satın alma siparişi teslim alma

Bu örnek, aşağıdaki değerlerin **Konum stoklama limitleri** sayfasının **Ürün çeşitleri** sekmesinde ayarlandığı, temiz bir *USMF* demo veri kümesine dayanır.

| Ambar | Yerleşim profili kodu | Madde kodu | Boyut | Miktar | Birim |
|-----------|---------------------|-------------|------|----------|------|
| 24        | KAT               | D0013       | P    | 300      | Her   |
| 24        | KAT               | D0013       | L    | 240      | Her   |
| 24        | KAT               | D0013       | C    | 360      | Her   |

Ürünler için farklı ölçü birimi ürün çeşitleri ayarlanır. Bu çeşitler üç palet (PL) için konum stoklama limitleriyle hizalanır:

- **M Boyutu:** 1 PL = her biri 100 (Ea)
- **L Boyutu:** 1 PL = 80 Ea
- **S Boyutu:** 1 PL = 120 Ea

Bu nedenle, **Konum profili kodu** değerinin *KAT* olarak ayarlandığı her konum D *0013* madde numarasından *3* *PL* içerebilir.

### <a name="prepare-for-the-example"></a>Örneğe hazırlık

Bu örnekte, iki satır için bir satın alma siparişi teslim alma akışı çalıştırırsınız. Ancak, konumların karışık maddelerin taşınmasına izin verdiğinden, yalnızca *FL-002* ile *FL-004* arasındaki boş konumların kullanıldığından ve açık bir gelen iş bulunmadığından emin olmak için öncelikle demo verilerini aşağıdaki şekilde güncelleştirmeniz gerekir.

1. *FL-001* konumu için **Konum profili** alanının değerini *KAT* yerine *KAT-05* olarak değiştirin.
1. *KAT* konumu profili için **Karışık maddelere izin ver** seçeneğini *Evet* olarak ayarlayın.
1. Aşağıdaki iki satıra sahip satın alma siparişi oluşturun:

    | Ambar | Madde kodu | Boyut | Miktar | Birim |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | C    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Örneği işleme

Önce *S* boyutunda *4* birim *PL* miktarı alacak ve oluşturulan iş için yerine koyma satırı konumlarını gözden geçireceksiniz. Daha sonra *L* boyutunda *4* birim *PL* miktarı alacak ve oluşturulan iş için yerine koyma satırı konumlarını gözden geçireceksiniz.

1. Ambar uygulamasında, kullanıcı kimliği *24* ve parola olarak *1*'i kullanarak oturum açın.
1. **Gelen** \> **Satın Alma Teslim Alma**'ya gidin.
1. Madde numarası *D0013*'ten *S* boyutunda *4* *PL* alır.
1. Oluşturulan yerine koyma işini gözden geçirin. Aşağıdaki sonucu görmeniz gerekir:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Madde numarası *D0013*'ten *L* boyutunda *4* *PL* alır.
1. Oluşturulan yerine koyma işini gözden geçirin. Aşağıdaki sonucu görmeniz gerekir:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Sonuçlara göre, sistemin doğru yerine koyma konumlarını tahsis edemediği sonucuna varabilirsiniz. Değilse, sistem son adımda *FL-003* konumuna *L* boyutundan neden yalnızca *1* *PL* ekleyip *2* *PL* eklemedi? Yani, bu konuma yerine koyma için neden toplam *3* *PL* yok?

Bu görünür hatayı açıklamak için konum stoklama limitlerinin seçim ölçütünü anlamanız gerekir. Sistem en ayrıntılı eşleşen kaydı seçer. Bu örnekte, en ayrıntılı eşleme kaydı **Boyut** değerinin *L* olduğu, **Miktar** değerinin *240* olduğu ve **Birim** değerinin de *Ea* olduğu satırdır. *S* boyutundan önceki *120* *Ea* miktarı girişten açık işiniz olduğu için kalan kapasite *240* – *120* = *120* *Ea* olarak hesaplanır. Bu nedenle, kalan kapasite yalnızca *1* *PL* *80* *Ea* taşıyabilir

> [!NOTE]
> Aynı konumda farklı miktarları olan maddelerin stok yenilemesini denetlemek için konum stoklama limitlerini kullanamazsınız. Bu durumda, bir *stok yenileme şablonu* kullanın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]