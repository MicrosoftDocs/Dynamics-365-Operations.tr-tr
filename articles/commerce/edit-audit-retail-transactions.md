---
title: Perakende mağaza hareketlerini düzenleme ve denetleme
description: Bu konuda, mağaza hareketlerini düzenleme ve denetleme işlevi açıklanır.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004401"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Perakende mağaza hareketlerini düzenleme ve denetleme

[!include [banner](includes/banner.md)]



Dynamics 365 Commerce müşterileri, birinci taraf ve üçüncü taraf satış noktası (POS) uygulamalarını kullanır. Birinci taraf POS uygulamasıyla, mağaza hareketleri bir toplu işlem aracılığıyla kanallardan Genel Merkez'e çekilir. Üçüncü taraf uygulamalarla, hareketler tümleştirme yoluyla Genel Merkez'e çekilir. Her iki durumda da, hareketler Genel Merkez'e çekildikten sonra, yalnızca başarılı şekilde doğrulanmış hareketlerin Genel Merkez'de deftere nakledilecek ekstreye çekilmesi için hareketler üzerinde birden fazla doğrulama çalıştıran bir tutarlılık denetimi işleminin yürütülmesi gerekir. 

Commerce hareketleri çeşitli nedenlerle doğrulamadan başarılı şekilde geçmeyebilir. Örneğin, tümleştirme kodundaki bir hata veya POS uygulamasındaki bir hata ya da bir ürünü kanalla eşitlendikten sonra silmek veya ilgili döneme ait hareketleri deftere nakletmeden bir mali dönemi kapatmak gibi bir kullanıcı hatası tutarsız verilere neden olabilir.

Bu hareketler, bayrakla işaretlenip ekstrelerden hariç tutulmasa da müşterinin günlük satışları mali öğelere nakletme sürecinde kesintiye neden olabilir.

Commerce'te, doğrulamada başarısız olan belirli hareketleri düzenleyebilir ve denetimi tüm değişiklikler için korumaya devam edebilirsiniz. 

## <a name="edit-and-audit-transactions"></a>Hareketleri düzenleme ve denetleme

Retail 10.0.5 sürümünde, düzenlenebilecek hareketler yalnızca satış ve iadeler gibi peşin hareketlerdir. Müşteri siparişlerini veya çevrimiçi siparişleri düzenleme işlemi desteklenmez. Retail 10.0.6 ve üstü sürümlerde, nakit yönetimi hareketlerini düzenleme işlemi de desteklenmektedir.

1. Dynamics Excel Eklentisi'ni yükleyin.

2. **Mağaza mali öğeleri** çalışma alanına gidin. **Hareket doğrulama hataları** kutucuğu, bir veya daha fazla doğrulama kuralının başarısız olduğu hareket formunun ön filtre uygulanmış görünümünü sunar.
 
3. Formu açın. Doğrulamada başarısız olan kayda tıklayın, **Office Eklentisi**'ne ve ardından **Seçili hareketi düzenle**'ye tıklayın. Seçili hareket ayrıntılarını içeren ve aşağıdaki çalışma sayfalarına sahip bir Excel dosyası açılır:

    - Satırlar: Bu çalışma sayfasında başlık ile ürün satırları ve hareketle ilgili veriler bulunur.
    - Ödemeler: Bu çalışma sayfasında harekete ilişkin ödeme satırlarının ayrıntıları yer alır.
    - İskontolar: Bu çalışma sayfasında harekete ilişkin iskontoyla ilgili ayrıntılar bulunur.
    - Vergiler: Bu çalışma sayfasında harekete ilişkin vergiyle ilgili ayrıntılar bulunur.
    - Masraflar: Bu çalışma sayfasında harekete ilişkin masraflarla ilgili veriler bulunur.

4. Excel dosyasında uygun alanları değiştirebilir ve Dynamics Excel Eklentisi'nin yayımla işlevini kullanarak verileri yeniden Genel Merkez'e yükleyebilirsiniz. Yayımlandıktan sonra değişiklikler sisteme yansıtılır. Yayımlama sırasında, kullanıcıların yaptığı değişiklikler üzerinde doğrulama yapılmaz.

5. Değişikliklerle ilgili eksiksiz bir denetim kılavuzunu, başlık düzeyindeki değişiklikler için **Perakende hareketi** başlığında ve ilgili hareket sayfasındaki ilgili bölüm veya kayıtta **Hesap denetimi kılavuzunu görüntüle**'ye tıklayarak görüntüleyebilirsiniz. Örneğin, satış satırlarıyla ilgili değişiklikler **Satış hareketleri** sayfasında, ödemelerle ilgili değişiklikler **Ödeme hareketleri** sayfasında vb. görünür. Değişiklikler için tutulan denetim ayrıntıları aşağıdaki gibidir.

   - Değiştirilme tarihi ve saati
   - Alan 
   - Eski değer
   - Yeni değer
   - Değiştiren

6. Değişiklikleriniz yapıldıktan ve yayımlandıktan sonra, yaptığınız değişikliklerin tutarlı ve geçerli olduğunu doğrulamak için **Mağaza hareketlerini doğrula** seçeneğini tekrar çalıştırın.

> [!NOTE]
> Yalnızca doğrulamanın başarısız olduğu hareketleri düzenleyebilirsiniz. Doğrulamayı geçen hareketleri düzenlemek istiyorsanız, değiştirmek istediğiniz hareketin doğrulama durumunu **Hata** veya **Hiçbiri** olarak değiştirip ardından hareketi düzenleyebilirsiniz. 


## <a name="bulk-edit-transactions"></a>Hareketleri toplu düzenleme

Retail 10.0.6 ve üstü sürümde, hareketleri ekstre düzeyinde toplu düzenleme seçeneği desteklenmektedir. 

1. Yukarıda belirtilen 1-3 arasındaki adımları kullanarak değişiklik yapmak istediğiniz hareketleri içeren bir ekstreyi açmak için Excel Eklentisi'ni kullanın.

2. Aşağıdaki seçeneklerden birini belirtin.

    - **Peşin hareketleri düzenle**. Bu seçenek, ekstreye dahil edilen tüm peşin hareketlerini düzenlemenize olanak tanır. Aşağıdaki Excel çalışma sayfaları kullanılabilir.
    
       - **Hareket**: Bu çalışma sayfası satış hareketleriyle ilgili tüm başlık düzeyindeki bilgileri içerir.
       - **Satış hareketi**: Bu çalışma sayfası satış hareketleriyle ilgili tüm satır düzeyindeki bilgileri içerir.
       - **Ödeme hareketleri**: Bu çalışma sayfası satış hareketleriyle ilgili tüm ödeme satırı bilgilerini içerir.
       - **İskonto hareketleri**: Bu çalışma sayfası satış hareketleriyle ilgili tüm iskonto satırı bilgilerini içerir.
       - **Vergi hareketleri**: Bu çalışma sayfası satış hareketleriyle ilgili tüm veri satırı bilgilerini içerir.
       - **Masraf hareketleri**: Bu çalışma sayfası satış hareketleriyle ilgili tüm masraf satırı bilgilerini içerir.

    - **Nakit yönetimi hareketlerini düzenle**. Bu seçenek, ekstreye dahil edilen tüm nakit yönetimi hareketlerini düzenlemenize olanak tanır. Aşağıdaki Excel çalışma sayfaları kullanılabilir.
     
       - **Hareket**: Bu çalışma sayfası nakit yönetimi hareketleriyle ilgili tüm başlık düzeyindeki bilgileri içerir.
       - **Banka ödemesi hareketleri**: Bu çalışma sayfası tüm bankaya para nakli hareketi ayrıntılarını içerir.
       - **Kasa ödemesi hareketleri**: Bu çalışma sayfası tüm kasaya para nakli hareketi ayrıntılarını içerir.
       - **Kasa sayımı**: Bu çalışma sayfası tüm kasa sayımı hareketi ayrıntılarını içerir.
       - **Gelir-gider hareketi**: Bu çalışma sayfası tüm gelir-gider hareketi satır ayrıntılarını içerir.
       - **Ödeme hareketleri**: Bu çalışma sayfası, gelir-gider hareketinin yanı sıra **Fatura öde** işlemi için ödemeyle ilgili tüm bilgileri içerir.

3.  Toplu düzenlenmiş hareketleri yayımladığınızda doğrulama gerçekleştirilmez. Tüm düzenlemelerinizin doğru olmasını ve çalışma sayfaları arasında verilerin doğrulunun korunmasını sağlamanız gerekir. Örneğin, açık hareketler için mali veya stok döneminin kapatıldığı senaryoları yönetmek üzere hareket tarihini değiştirmek istiyorsanız **İş tarihi** sütunu bulunan tüm Excel çalışma sayfalarında tarihi değiştirmeniz gerekir. Hareketleri düzenlendikten sonra doğrulamak için **Ekstreler** sayfasındaki **Hareketleri yeniden doğrula** seçeneğini kullanabilirsiniz.
