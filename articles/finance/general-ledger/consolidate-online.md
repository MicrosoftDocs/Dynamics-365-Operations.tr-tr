---
title: Çevrimiçi mali konsolidasyonlar
description: Bu konuda, genel muhasebede çevrimiçi mali konsolidasyonlar açıklanmaktadır.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 91df786ed2298e21e7a3018b915c9bd5458efc32
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009255"
---
# <a name="online-financial-consolidations"></a>Çevrimiçi mali konsolidasyonlar

[!include [banner](../includes/banner.md)]

Bu konuda, genel muhasebede çevrimiçi mali konsolidasyonlar açıklanmaktadır. Bu konuyu okumadan önce [Mali konsolidasyonlar ve para birimi çevirmeye genel bakış](financial-consolidations-currency-translation.md) konusunu okuduğunuzdan emin olun.

Kurulumunuzu tamamladıktan sonra **Konsolide et [Çevrimiçi]** sayfasına konsolidasyon ayrıntılarını girin. Tamamladığınızda konsolidasyonu işlemek için **Tamam** veya **Toplu İş**'e tıklayabilirsiniz.

## <a name="criteria"></a>Ölçütler
**Konsolide et [Çevrimiçi]** sayfasının **Ölçütler** sekmesinde, konsolide edilen hesapları, dönemleri ve veri türünü tanımlayın.

![Ölçütler sekmesi](./media/criteria-consolidate-online.png "Ölçütler sekmesi")

Bu sekmedeki çeşitli alanların açıklaması aşağıdaki gibidir:

- **Açıklama**: Konsolide ettiğiniz dönem için daha net bir açıklama girin.
- **Ana hesap**: İşlenecek ana hesapları tanımlamak için bu bölümdeki alanları kullanın.

    - **Başlangıç** ve **Bitiş**: İşlenecek hesaplar için bir aralık belirtin. Bu alanları boş bırakırsanız tüm şirketlerdeki tüm hesaplar konsolidasyon şirketine taşınır. Bu nedenle, dört adet şirketi konsolide ediyorsanız ve her şirketin farklı bir hesap planı varsa bu dört şirketteki tüm hesaplar konsolidasyon şirketinde oluşturulur.
    - **Konsolidasyon hesabı kullan**: Bu seçeneği **Evet** olarak ayarlarsanız **Şuradan konsolidasyon hesabı seç:** alanı kullanılabilir duruma gelir. Bu alanda, tüm hesapların **Ana hesaplar** sayfasında ayarlanan konsolidasyon hesabına konsolide edilmesinin gerekip gerekmediğini veya hesabı konsolidasyon hesabı gruplarının birinden seçmek isteyip istemediğinizi belirleyebilirsiniz.
    - **Konsolidasyon hesap grubu**: Konsolidasyonda ana hesap eşlemesi için kullanılacak grubu seçin.

- **Konsolidasyon dönemi**: Konsolidasyon dönemini tanımlamak için bu bölümdeki alanları kullanın.

    - **Başlangıç** ve **Bitiş**: Konsolidasyon için bir tarih aralığı belirtin. Bu alanları boş bırakırsanız konsolidasyon şirket için genel muhasebe takviminde tanımlanan tüm dönemler için işlenir. Bu alanları boş bırakmanızı önermiyoruz.
    - **Gerçek tutarları dahil et**: Gerçek verilerinizi konsolide etmek için bu seçeneği **Evet** olarak ayarlayın.
    - **Bütçe tutarlarını dahil et**: Bütçe kaydındaki verileri konsolide etmek için bu seçeneği **Evet** olarak ayarlayın.
    - **Konsolidasyon işlemi sırasında bakiyeleri yeniden yapılandır**: Bu seçeneği **Evet** olarak ayarlamanızı önermiyoruz. Bunun yerine bakiyeleri ayrı bir toplu iş olarak yeniden yapılandırın.

- **Bütçe modelleri**: Bütçe verilerini konsolide etmeyi seçtiyseniz bütçe modellerini tanımlamak için bu bölümdeki alanları kullanın.

    - **Başlangıç** ve **Bitiş**: Kullanılacak model aralığını belirtin.
    - **Bütçe oran türü**: Bütçe verilerini para birimine çevirmek için kullanılacak bütçe oranı türünü seçin.

## <a name="financial-dimensions"></a>Mali boyutlar
**Mali boyutlar** sekmesinde konsolidasyon şirketine dahil edilmesi gereken boyutları tanımlayın. Boyut seçmek için **Belirtim** alanını **Boyut** olarak ayarlayın ve ardından konsolidasyon şirketinde boyut düzenini tanımlayın.

![Mali boyutlar sekmesi](./media/financial-dimensions-cons.png "Mali boyutlar sekmesi")

Tanımladığınız düzenden bağımsız olarak **Ana hesap** her zaman ilk segment olur.

## <a name="legal-entities"></a>Tüzel kişilikler
**Tüzel kişilikler** sekmesinde, konsolidasyon şirketine dahil edilmesi gereken şirketleri tanımlayın. Ayrıca bu şirketlerin sahiplik yüzdesini de tanımlayabilirsiniz. Yüzde 100'den az bir sahiplik yüzdesi belirtirseniz belirtilen yüzde konsolidasyon şirketinde toplanır. Dönüştürme farkları için **Dönüştürme farklarının hesap türü** alanı, **Otomatik hareketler için hesaplar** sayfasındaki kurulumdan ana hesabı seçmek üzere kullanılır.

![Tüzel kişilikler sekmesi](./media/legal-entities-cons.png "Tüzel kişilikler sekmesi")

![Otomatik hareketler için hesaplar sayfası](./media/accounts-for-automatic-cons.png "Otomatik hareketler için hesaplar sayfası")

## <a name="elimination"></a>Eleme
**Eleme** sekmesinde, elemeleri işlemek üzere üç seçeneğiniz bulunmaktadır:

- Eleme kuralını seçin ve ardından **Teklif seçenekleri** alanında **Yalnızca teklif** seçeneğini belirleyin. Bu seçenek, konsolidasyon işlemi sırasında elemeyi işler ancak her şeyi tek adımda deftere nakledemez. Daha sonra günlüğü deftere nakledebilirsiniz.
- Eleme kuralını seçin ve ardından **Teklif seçenekleri** alanında **Yalnızca deftere naklet** seçeneğini belirleyin. Bu seçenek, konsolidasyon işlemi sırasında elemeyi işler ve her şeyi tek adımda deftere nakleder.
- Eleme günlüğünü kullanılarak eleme teklifini konsolidasyon işleminden ayrı olarak çalıştırın.

![Eleme sekmesi](./media/elimination-cons-onl.png "Eleme sekmesi")

Elemeler hakkında daha fazla bilgi için bkz. [Eleme kuralları](./elimination-rules.md).

## <a name="currency-translation"></a>Para birimi çevirme
**Para birimi çevirme** sekmesinde tüzel kişiliği, hesabı ve döviz kuru türü ile oranı tanımlayın. **Şuradan döviz kurunu uygula** alanında üç seçenek kullanılabilir:

- **Konsolidasyon tarihi**: Döviz kurunu almak için konsolidasyon tarihi kullanılır. Bu oran, nokta veya ay sonu oranına eşdeğerdir. Oranın önizlemesini görebilir ancak düzenleyemezsiniz.
- **Hareket tarihi**: Döviz kurunu seçmek için her hareketin tarihi kullanılır. Bu seçenek çoğunlukla sabit kıymetler için kullanılır ve çoğunlukla geçmiş oran olarak adlandırılır. Hesap sayfasında çeşitli hareketler için birçok oran bulunduğundan oranın önizlemesini göremezsiniz.
- **Kullanıcı tanımlı oran**: Bu seçeneği belirledikten sonra istediğiniz döviz kurunu girebilirsiniz. Bu seçenek, ortalama döviz kurları için veya sabit döviz kuruna göre konsolidasyon işlemi yapıyorsanız yararlı olabilir.

![Para birimi çevirme sekmesi](./media/currency-translation-cons-online.png "Para birimi çevirme sekmesi")

## <a name="additional-resources"></a>Ek kaynaklar

Konsolidasyon ve para birimi dönüştürmeleri hakkında daha fazla bilgi için bu konunun ana konusuna bakın: [Mali konsolidasyonlar ve para birimi dönüştürmeye genel bakış](./financial-consolidations-currency-translation.md).

Konsolide mali tabloları oluşturabileceğiniz senaryolar hakkında bilgi için bkz. [Konsolide mali tabloları oluşturma](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]