---
title: Genel muhasebe hesabı kapatmaları
description: Bu konu, Genel muhasebe kapatmaları sayfasını genel muhasebe hareketlerini kapatmak ve kapatmaları geri almak için nasıl kullanılacağını açıklar.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: e98b012210338e7f18cb874eefbc8a023aa4428b
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075336"
---
# <a name="ledger-settlements"></a>Genel muhasebe hesabı kapatmaları

[!include [banner](../includes/banner.md)]

Genel muhasebe kapatması, genel muhasebedeki borç ve alacak hareketlerini eşleştirme işlemidir. Borç ve alacak tutarlarının mutabakatı, genel muhasebe hesabının bakiyesinin bu bakiyeyi oluşturan ayrıntılı hareketlerle mutabakatını yapmak için kullanılır.

Kapatılan hareketler sorguların ve raporların dışında tutulabilir. Bu şekilde, genel muhasebe hesabının bakiyesini oluşturan açık genel muhasebe hareketlerini analiz etmek daha kolaydır.

> [!IMPORTANT] 
> Borç Hesapları (AP) ve Alacak Hesapları (AR) modüllerinde fatura ve ödemelerin de kapatması vardır. AR ve AP alt defterlerinde kapatma gerçekleştiğinde, karşılık gelen defter girişleri otomatik olarak kapatılmaz.

## <a name="ledger-settlement-features"></a>Genel muhasebe kapatma özellikleri
Microsoft Dynamics 365 Finance sürüm 10.0.21'de, **Gelişmiş genel muhasebe kapatmayı etkinleştir** seçeneği **Genel muhasebe parametreleri** sayfasından kaldırıldı. Gelişmiş genel muhasebe kapatması artık her zaman etkindir.
Finance sürüm 10.0.25'te, **Genel muhasebe kapatması ile yıl sonu kapanışı arasındaki farklılıklar** özelliği tanıtıldı. Bu özellik, hem genel muhasebe kapatma hem de Genel muhasebe yıl sonu kapanışında temel işlevselliği değiştirir. **Özellik yönetimi** çalışma alanında bu özelliği etkinleştirmeden önce, [Genel muhasebe kapatması ile yıl sonu kapanışı arasındaki fark](awareness-between-ledger-settlement-year-end-close.md) bölümüne bakın.

## <a name="set-up-ledger-settlement"></a>Genel muhasebe kapatmasını ayarlama
Genel muhasebe kapatmasını yapmak istediğiniz ana hesapları seçmelisiniz. Bu ana hesapları seçmenin iki yolu vardır.

1. **Genel muhasebe** > **Genel muhasebe ayarı** > **Genel muhasebe parametreleri**'ne gidin.
2. **Genel muhasebe kapatmaları** sekmesinde, ana hesapları seçmek istediğiniz hesap grafiklerini seçin.
3. Genel muhasebe kapatması yapılacak ana hesapları seçin. Hesap grafikleri genel olduğundan, seçili hesap grafiklerinin atandığı tüm şirketler, genel muhasebe kapatma için seçilen ana hesaplara sahip olur.

  -veya-

1. **Genel muhasebe** > **Periyodik görevler** > **Genel muhasebe hesabı kapatmaları**'na gidin.
2. **Genel muhasebe kapatma hesapları**'nı seçin.
3. İletişim kutusunda, genel muhasebe kapatmasının yapılması gereken hesap ve ana hesap grafiklerini seçin. Bu iletişim kutusu bir kısayoldur. Buraya eklediğiniz tüm ana hesaplar da **Genel muhasebe parametreleri** sayfasına yansıtılır.

Ana hesapları genel muhasebe kapatmasından istediğiniz zaman kaldırmak için aynı temel yordamları kullanabilirsiniz. Ana hesabın kaldırılmasının, önceki genel muhasebe kapatmaları üzerinde hiçbir etkisi yoktur. Ancak ana hesap ve hareketler artık **Genel muhasebe kapatması** sayfasında görünmez.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Hareketleri kapat
Genel muhasebe hareketlerini kapatmak için bu adımları izleyin.

1. **Genel muhasebe** > **Periyodik görevler** > **Genel muhasebe hesabı kapatmaları**'na gidin.
2. Sayfanın üst kısmına filtreleri ayarlayın:

    - Tarih aralığı seçin. Alternatif olarak, tarih aralığını otomatik olarak doldurmak için bir tarih aralığı kodu seçin. Mali yılları arasındaki hareketler için genel muhasebe kapatması yapmanız önerilmez.
    - Deftere nakil katmanını gerekli şekilde değiştirin. Farklı deftere nakil katmanlarındaki hareketleri kapatamazsınız.
    - Ana hesabı ve boyutları ayrı ayrı göstermek için bir finansal boyut seçin.

3. **Hareketleri görüntüle**'yi seçerek, önceki bölümdeki hesap planı listesini ayarladığınızda belirttiğiniz hesap listesini ve ayarladığınız filtrelerle eşleşen tüm hareketleri gösterin.

    - Filtreleri veya boyut kümelerini değiştirirseniz, yneiden **Hareketleri görüntüle**'yi seçmelisiniz.
    - Tek bir ana hesaba yönelik hareketleri filtrelemek için **Genel muhasebe hesabı** alanında filtre kullanın. Farklı ana hesaplara nakledilen hareketler için genel muhasebe kapatması yapmanız önerilmez.

4. Kapatma için satırları seçin. Sayfanın üstündeki **Seçilen tutar** alanının değeri, seçilen satırlardaki toplam tutara göre artar veya azalır.
5. Hareketleri seçmeyi tamamladıktan sonra **Seçilen olarak işaretle**'yi seçin. Seçili her hareket için **İşaretli** sütununda bir onay işareti görünür. Ayrıca, kılavuzun üstündeki **İşaretli tutar** alanının değeri, işaretli satırlardaki toplam tutara göre artar veya azalır.
6. **İşaretli tutar** alanındaki değer **0** (sıfır) iken **İşaretlenmiş hareketleri kapat**'ı seçin. İşaretli hareketlerin durumu **Kapatıldı** olarak değiştirilir.

    > [!IMPORTANT]
    > Etkin tüzel kişilik için kapatma için işaretlediğiniz tüm hareketler, filtre uyguladığınız için genel muhasebe kapatma sayfasında gösterilmese bile kapatılacaktır.

## <a name="make-transactions-easier-to-find"></a>Hareketleri bulmayı kolaylaştırın
**Genel muhasebe hesabı kapatmaları** sayfası, kapatmak için gereken hareketleri görüntülemenizi kolaylaştıran özellikler içerir.

- **İşaretli** onay kutusunun seçili olup olmadığına bağlı olarak hareketleri filtrelemek için **İşaretli** filtresini kullanın.
- Hareketleri durumlarına göre filtrelemek için **Durum** filtresini kullanın.
- Tutarları mutlak değere göre sıralamak için **Mutlak tutara göre sırala**'yı seçin. Bu şekilde, aynı tutara sahip borç ve alacakları gruplayabilirsiniz.

## <a name="reverse-a-settlement"></a>Kapatmayı ters çevirin
Yanlışlıkla yapılan bir kapatmayı tersine çevirin.

1. [Hareketleri kapatma](#settle-transactions) bölümündeki 1 ila 3 adımlarını izleyerek ilgilendiğiniz hareketleri gösterin.
2. **Durum** filtresinde, **Kapatılmış**'ı seçin.
3. Ters çevrilmesi için satırları seçin.
4. **İşaretli hareketleri ters çevir**'i seçin. Aynı kapatma kimliğine sahip tüm hareketlerin durumu **Kapatılmadı** olarak güncelleştirilir.

    > [!IMPORTANT]
    > Aynı kapatma kimliğine sahip tüm hareketler işaretli olmasalar bile tersine çevrilir. Örneğin, dört satır işaretliydi ve kapatıldı. Dört satırın da kapatma kimliği aynıdır. Bu dört satırdan birini işaretler ve **işaretli hareketleri ters çevir**'i seçerseniz dört satır da ters çevrilir.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
