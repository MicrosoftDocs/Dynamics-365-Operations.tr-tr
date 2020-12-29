---
title: Genel muhasebe hesabı kapatmaları
description: Bu konu, Genel muhasebe kapatmaları sayfasını genel muhasebe hareketlerini kapatmak ve kapatmaları geri almak için nasıl kullanılacağını açıklar.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448726"
---
# <a name="ledger-settlements"></a>Genel muhasebe hesabı kapatmaları

[!include [banner](../includes/banner.md)]

Genel muhasebe kapatmaları, genel muhasebede borç ve alacak hareketlerini eşleştirmenizi ve onları kapatılmış olarak işaretlemenize olanak tanır. Bu şekilde, ilgili hareketlerin temizlenmiş olduğundan emin olabilirsiniz. Yanlışlıkla yapıldıysa kapatmaları geri alabilirsiniz.

## <a name="enable-advanced-ledger-settlements"></a>Gelişmiş genel muhasebe kapatmalarını etkinleştirin

Gelişmiş genel muhasebe kapatmaları sayfası, hareketleri filtrelemek ve seçmek için ek yetenekler sağlar. Gelişmiş genel muhasebe kapatmaları sayfasını etkinleştirmek için şu adımları izleyin.

1. **Genel muhasebe** \> **Genel muhasebe ayarı** \> **Genel muhasebe parametreleri**'ne gidin. 
2. **Genel muhasebe hesabı kapatmaları** sekmesinde, **Gelişmiş genel muhasebe kapatması** seçeneğini **Evet** olarak ayarlayıp gelişmiş genel muhasebe işlevini açın. Gelişmiş **Genel muhasebe hesabı kapatmaları** sayfası, **Periyodik görevler**'deki **Genel muhasebe kapatmaları**'nı seçtiğinizde kullanılır. 
3. Her hesap planı için genel muhasebe hesabı kapatmalarına kullanmak hesaplar listesine girmeniz gerekir. Bu liste, **Genel muhasebe hesabı kapatmaları** sayfasında görünen hareketler listesini filtrelemek için kullanılır. **Hesap planı** listesinde, bir hesap planı seçin ve sonra listeye yeni hesaplar eklemek için **Yeni**'yi seçin.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Gelişmiş genel muhasebe kapatmaları sayfasını kullanarak hareketleri kapatın

Genel muhasebe hareketlerini kapatmak için bu adımları izleyin.

1. **Genel muhasebe** \> **Periyodik görevler** \> **Genel muhasebe hesabı kapatmaları**'na gidin.
2. Sayfanın üst kısmına filtreleri ayarlayın:

    - Bir tarih aralığı seçin veya tarih aralığını otomatik olarak doldurmak için **Tarih aralığı kodu**'nu seçin.
    - Deftere nakil katmanını gerekli şekilde değiştirin.
    - Genel muhasebe hesabı ve boyutları ayrı ayrı göstermek için bir finansal boyut seçin.

3. **Hareketleri görüntüle**'yi seçerek, önceki bölümdeki hesap planı listesini ayarladığınızda belirttiğiniz hesap listesini ve ayarladığınız filtrelerle eşleşen tüm hareketleri gösterin. Filtreleri veya boyut kümelerini değiştirirseniz, yneiden **Hareketleri görüntüle**'yi seçmelisiniz.
4. Kapatma için dikkate alacak en az bir satır seçin. Sayfanın üstündeki **Seçilen tutar** alanının değeri, seçtiğiniz satırlardaki toplam tutara göre artar veya azalır.
5. Hareketleri seçmeyi tamamladıktan sonra **Seçilen olarak işaretle**'yi seçin. Seçtiğiniz her hareket için **İşaretli** sütununda bir onay işareti görüntülenir. Ayrıca, kılavuzun üstündeki **İşaretli tutar** alanının değeri, işaretlediğiniz satırlardaki toplam tutara göre artar veya azalır.
6. **İşaretli tutar** değeri **0** (sıfır) iken **İşaretlenmiş hareketleri kapat**'ı seçin. İşaretli hareketlerin durumu **Kapatıldı** olarak değiştirilir.

## <a name="make-transactions-easier-to-find"></a>Hareketleri bulmayı kolaylaştırın

**Genel muhasebe hesabı kapatmaları** sayfası, kapatmak için gereken hareketleri görmenizi kolaylaştıran özellikler içerir.

- **Seçileni kaldır** düğmesi, seçili tüm satırlar için **İşaretli** alanını temizler.
- **İşaretli** filtre, **İşaretli** alanlarının seçili veya temiz olmasına bağlı olarak hareketleri filtrelemenizi sağlar.
- **Durum** filtresi, durumlarının **Kapatılmış** veya **Kapatılmamış** olduğuna bağlı olarak hareketleri filtrelemenizi sağlar.
- **Mutlak tutara göre sırala** düğmesi, mutlak değere göre tutarları sıralamanızı sağlar, böylece aynı tutara sahip olan borçlar ve alacakları birlikte gruplayabilirsiniz.

## <a name="reverse-a-settlement"></a>Kapatmayı ters çevirin

Yanlışlıkla yapılan bir kapatmayı tersine çevirin.

1. "Gelişmiş genel muhasebe kapatmaları sayfasını kullanarak hareketleri kapatın" sayfasındaki 1 ila 3 adımlarını izleyerek aradığınız hareketleri gösterin.
2. **Durum** filtresinde, **Kapatılmış**'ı seçin.
3. Geriye alma için dikkate alacak en az bir satır seçin. Sayfanın üstündeki **Seçilen tutar** alanının değeri, seçtiğiniz satırlardaki toplam tutara göre artar veya azalır.
4. Hareketleri seçmeyi tamamladıktan sonra **Seçilen olarak işaretle**'yi seçin. Seçtiğiniz her hareket için **İşaretli** sütununda bir onay işareti görüntülenir. Ayrıca, sayfanın üstündeki **İşaretli tutar** alanının değeri, işaretlediğiniz satırlardaki toplam tutara göre artar veya azalır.
5. **İşaretli tutar** değeri **0** (sıfır) iken **İşaretlenmiş hareketleri geri al**'ı seçin. İşaretli hareketlerin durumu **Kapatılmadı** olarak değiştirilir.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Hareketler listesinde bulunan hesapların listesini güncelleştirin

Hareketler listesinde bulunan hesapları düzenleyebileceğiniz iletişim kutusunu açmak için **Genel muhasebe kapatma hesapları**'nı seçin. Listeye yeni hesaplar eklemek için **Yeni**'yi seçin. Bu liste, **Genel muhasebe hesabı kapatmaları** sayfasında görünen hareketler listesini filtrelemek için kullanılır.
