---
title: Kira deftere nakil hesaplarını ayarlama
description: Bu konu, Varlık kiralama hareketleri için gerekli olan deftere nakil hesaplarını listeler ve Kira deftere nakil parametreleri sayfasında deftere nakil hesaplarının nasıl tanımlanacağını açıklar.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 26e046b627d71721f4a4d7b6a60171a482e3e357
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992801"
---
# <a name="set-up-lease-posting-accounts"></a>Kira deftere nakil hesaplarını ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, Varlık kiralama hareketleri için gerekli olan deftere nakil hesaplarını listeler ve **Kira deftere nakil parametreleri** sayfasında deftere nakil hesaplarının nasıl tanımlanacağını açıklar.

Muhasabe Standartları Kodlaması Konu 842 (ASC 842) ve Uluslararası Mali Raporlama Standardı 16 (IFRS 16) gerekliliklerine uymak için hesap planınızda hesap oluşturmanız gerekebilir. Ancak, ASC ve IFRS standartlarına uymak için oluşturduğunuz hesaplar sabit varlık hesapları değildir. ASC 842 kapsamında, kullanım hakkı (ROU) valrığı hem finansal kiralamalar hem de işletme kiralamalarına kaydedilir. Bu kiralamalar sabit varlıklardan ayrıdır. (Yine de bir ROU varlığını Sabit varlıkları kullanarak koruyabilirsiniz.)

Hesap yapıları oluşturma hakkında bilgi için bkz. [Hesap yapıları oluşturma](../general-ledger/tasks/create-account-structures.md). Ana hesap oluşturma hakkında bilgi için bkz. [Ana hesap oluşturma](../general-ledger/tasks/create-main-account.md).

Aşağıdaki tabloda, kiralanan varlık hareketleri için daha önce oluşturulmadıysanız oluşturmanız gereken hesap örnekleri gösterilmiştir. IFRS 16 kapsamında, işletme kiralaması ilişkileri düşük değerli ve kısa süreli kiralamalar için kullanılmaya devam eder.

| Genel muhasebe hesap numarası | Hesap türü  | Hesap adı                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Varlık         | Araç ROU varlığı                                     |
| 180160                | Varlık         | Bina ROU varlığı                                    |
| 180250                | Varlık         | Birikmiş amortisman - araçlar                   |
| 180260                | Varlık         | Birikmiş amortisman - binalar                  |
| 222300                | Pasif     | Kısa süreli yükümlülük - finansal kiralamalar                |
| 222310                | Bilanço | Kısa süreli yükümlülük - İşletme kiralamaları              |
| 250200                | Pasif     | Senet borçları                                         |
| 250601                | Bilanço | Uzun süreli yükümlülük - finansal kiralamalar                 |
| 250602                | Bilanço | Uzun süreli yükümlülük - işletme kiralamaları               |
| 250606                | Bilanço | Ertelenmiş kira                                         |
| 300160                | Bilanço | Yedek akçe                                     |
| 604500                | Gider       | Kiralama Gideri                                         |
| 604501                | Gider       | Araç işletme kiralaması gideri - faiz taahhuku  |
| 604502                | Gider       | Araç işletme kiralaması gideri - amortisman        |
| 605200                | Gider       | Bina işletme kiralaması gideri - faiz taahhuku |
| 605201                | Gider       | Bina işletme kiralaması gideri - amortisman       |
| 607101                | Gider       | Araç kiralama amortisman gideri                    |
| 607102                | Gider       | Bina kiralama amortisman gideri                   |
| 607103                | Gider       | Değer düşüşü gideri - finansal kiralamalar                   |
| 607104                | Gider       | Değer düşüşü gideri - İşletme kiralamaları                 |
| 618910                | Gider       | Kiralama gideri - finansal kiralamalar                        |
| 618920                | Gider       | Değişken ödemeler - finansal kiralamalar                    |
| 618930                | Gider       | Değişken ödemeler - işletme kiralamaları                  |
| 800600                | Gider       | Araç kiralama faiz gideri                        |
| 800601                | Gider       | Bina kiralama faiz gideri                       |
| 801201                | Bilanço | Kazanç ve kayıp - kiralama değişikliği                      |

## <a name="configure-posting-accounts"></a>Deftere nakil hesaplarını yapılandırma

Hesapları oluşturulan kiralama defterlerine ve gruplarına atamak için Varlık kiralama parametrelerini yapılandırmanız gerekir.

1. **Varlık kiralama \> Kurulum \> Kira deftere nakil parametreleri**'ne gidin.
2. **Hesaplar** sekmesinde **Kiralama hesapları** hızlı sekmesini açın. İlgili **Deftere nakil türüne** göre finansal kiralamaları ve işletme kiralamalarının ana hesaplarını belirleyin. Önceki tabloda, işletme kiralamalarına ve finans kiralamalara ilişkin hesaplar gösterilmektedir.

    > [!NOTE]
    > Bu adımda, **Kiralama gideri mahsup** ve **Kira artışı/azalışı** hariç her deftere nakil türü için hem işletme kiralamalarına hem de finansal kiralamalara yönelik olarak ayrı hesaplar ayarlamanız gerekir. IFRS 16 muhasebe çerçevesine bağlı olan şirketler, işletme kiralaması için bir ana hesap eklemelidir. IFRS 16 kapsamında tüm kiralamalar finansal kiralama kabul edildiğinden, bu alan gerekli bir alan olsa da sistem bu hesabı kullanmayacaktır.
    >[!NOTE]
    > **Kira artışı/azalışı**; **Başlangıçtaki doğrudan maliyet, Kiralama teşvikleri, Kiralama ön ödemeleri ve Parçalara ayırma** maliyetleri dahil ek varlık hususları için deftere nakil türü olarak kullanılacak ancak varsayılan ayarı **Kiralama varlığı** olan Kullanım hakkı ana hesabına nakledilecektir.        
    
3. Ana hesaba karşılık gelen belirli bir kiralama grubunu seçmek için **Hesap Kodu** alanında **Grup**'u seçin. Ardından, **Hesap/Grup numarası** alanında, ana hesaba atanacak kiralama grubunu seçin.
4. Sistemde ayarlanmış idari maliyetlere hesap kodları atamak için **İcra maliyetleri** hızlı sekmesindeki **Gider türü** alanında bir gider seçin. Ardından her bir defterle kullanmak üzere finansal hesaplar ve işletme hesapları atayın.

    > [!NOTE]
    > Planlanan gider faturası deftere nakledildiğinde, seçilen finansal hesap veya işletme hesabı borçlandırılır.
    > **Kira gideri mahsup** işlemi, icra maliyeti hareketleri için deftere nakil türü olarak kullanılacak ancak kiralama ayrıntılarında veya kiralama defteri formunda **İcra maliyeti ödeme planı satırları**'nda tanımlı **Mahsup hesap**'a nakledilecektir.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]