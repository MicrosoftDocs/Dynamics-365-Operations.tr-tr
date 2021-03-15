---
title: Konsolidasyon işleminde tüzel kişilik hazırlama
description: Konsolidasyon sırasında, birkaç tüzel kişilik hesabı kümesinden hareketleri tek bir tüzel kişilik hesabı kümesinde birleştirebilirsiniz. Bu konuda, bir konsolidasyon için tüzel kişiliğin nasıl hazırlanacağı açıklanmaktadır.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990323"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Konsolidasyon işleminde tüzel kişilik hazırlama

[!include [banner](../includes/banner.md)]

Konsolidasyon sırasında, birkaç tüzel kişilik hesabı kümesinden hareketleri tek bir tüzel kişilik hesabı kümesinde birleştirebilirsiniz. Bu konuda, bir konsolidasyon için tüzel kişiliğin nasıl hazırlanacağı açıklanmaktadır.

> [!NOTE]
> Microsoft Dynamics 365 Finance için Management Reporter'ı kullanarak birden çok tüzel kişilik için mali sonuçları konsolide bir biçimde birleştirmeniz önerilir. Management Reporter, tüzel kişiliklerde konsolide mali raporlar oluşturmanıza, diğer kaynaklardan konsolidasyon verilerini içeri aktarmak için Excel'i kullanmanıza ve Dynamics 365 Finance'te konsolidasyon sürecini çalıştırmak zorunda kalmadan tutarları istediğiniz sayıda raporlama para birimlerine çevirmenize olanak sağlar.

Konsolide tüzel kişilikten mali tablolar gibi raporları yazdırabilirsiniz. Ancak, konsolide tüzel kişiliği günlük hareketler için kullanamazsınız.

Konsolide tüzel kişilikten farklı veritabanları kullanan tüzel kişiliklerden gelen verileri konsolide edebilirsiniz. Bu konsolidasyon işlemine *içeri aktarma konsolidasyonu* denir. Alternatif olarak, tüzel kişilikler konsolide tüzel kişilikle aynı veritabanını kullanabilir. Bu konsolidasyon işlemine *çevrimiçi konsolidasyon* denir.

Konsolide tüzel kişilik, yan kuruluşların sonuçlarını ve bakiyelerini toplar. Konsolidasyon için konsolide tüzel kişilik hazırlamak için bu adımları izleyin.

1. **Genel muhasebe \> Kurulum \> Kuruluş \> Tüzel kişilikler**'e gidin.
2. Konsolide tüzel kişilik olacak tüzel kişiliği oluşturmak için **Yeni**'yi seçin.
3. **Finansal konsolidasyon işlemi için kullan** onay kutusunu seçin ve konsolide tüzel kişilik hakkında bilgi girin. Bu bilgileri tam olarak konsolide tüzel kişilik için mali tablolarda görünmesini istediğiniz şekilde girdiğinize emin olun.
4. Sayfayı kapatın.
5. Sayfanın sağ üst köşesindeki alanda konsolide tüzel kişiliği seçin ve sonra **Tamam**'ı seçin.
6. **Genel muhasebe \> Kurulum \> Kayıt defteri**'ne gidin.
7. Konsolide tüzel kişilik için hesap planını, mali takvimi, muhasebe para birimini, isteğe bağlı raporlama para birimini ve varsayılan döviz kuru türünü seçin. 
8. **Genel muhasebe \> Kurulum \> Döviz \> Döviz kurları**'na gidin.
9. Yan kuruluş tüzel kişiliklerin para birimleri için ilgili dönemlerde döviz kurları ayarlayın.
10. Sayfayı kapatın.
11. Konsolide tüzel kişiliğin yabancı para birimleri kullanan yan kuruluşları varsa şu adımları izleyin:

    1. **Genel muhasebe \> Kurulum \> Deftere nakil \> Otomatik hareketler için hesaplar**'a gidin.
    2. **Deftere nakil türü** alanında uygun bir hesap seçin.

        - Tüzel kişiliğin ana tüzel kişilikle finansal veya operasyonel olarak birbirine bağımlı yabancı yan kuruluşları varsa **Konsolidasyon farkları için kar/zarar hesabı** deftere nakil türü için uygun bir hesap seçin.
        - Ana tüzel kişilikten finansal ve operasyonel olarak bağımsız bir yan kuruluşu veya ana tüzel kişilikten finansal ve operasyonel olarak bağımsız olan birkaç yan kuruluşun sonuçlarını içeren bir tüzel kişiliği konsolide ediyorsanız ve verileri konsolide etmek için çeviri yöntemleri kullanıyorsanız **Konsolidasyon farkları için bakiye hesabı** deftere nakil türü için uygun bir hesap seçin.

    3. **Ana hesap** alanında, yabancı para birimi yeniden değerleme ayarlamaları için kullanılacak ana hesapları seçin.
    4. Sayfayı kapatın.

    Konsolide tüzel kişiliği bir dönemin başlarında oluşturursanız konsolidasyon döneminde döviz kurları değiştikçe döviz tutarlarını yeniden değerleyebilirsiniz.

Konsolide tüzel kişilik artık **Konsolide et** periyodik işi için ayarlanmıştır. Bir içeri aktarma konsolidasyonu veya çevrimiçi konsolidasyon yapabilirsiniz.

- İçeri aktarma konsolidasyonu yapmak için **Genel muhasebe \> Periyodik \> Konsolide et \> Konsolide et \[İçeri aktarma kaynağı\]**'na gidin.
- Çevrimiçi konsolidasyon yapmak için **Genel muhasebe \> Periyodik \> Konsolide et \> Konsolidasyon \[\]Çevrimiçi**'ye gidin.

> [!NOTE]
> Konsolidasyonu işlemeden önce, yan tüzel kişilikleri konsolidasyon için hazırlamanız gerekir. Daha fazla bilgi için bkz. [Konsolidasyon için bir bağlı tüzel kişilik ayarlama](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]