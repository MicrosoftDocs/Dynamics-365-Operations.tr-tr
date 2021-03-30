---
title: Konsolidasyon için bağlı şirket tüzel kişiliği ayarlama
description: Bu konu, konsolidasyon şirketleri için hesap grafikleriyle nasıl çalışılacağını açıklamaktadır.
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
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 44bd184514b24a816cc83f6b0070a5e08163921b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204821"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Konsolidasyon için bağlı şirket tüzel kişiliği ayarlama

[!include [banner](../includes/banner.md)]

Konsolidasyon için yan kuruluş oluşturmak amacıyla kullandığınız yöntem, bağlı olan tüzel kişiliğinden hesap plan yapısının, konsolide tüzel kişilikteki hesap planını yansıtma düzeyine kısmen bağlıdır.

Bir dönem kapanışı kapsamında bir konsolidasyon başlatmadan önce, dönem sonu kapanışı için hazırlık faaliyetlerini tamamlayın ancak konsolidasyon tamamlanana kadar yan kuruluş hesaplarını kapatmayın. Dönem sonu kapanışı hakkında daha fazla bilgi için bkz. [Genel muhasebe defterini dönem sonunda kapatma](close-general-ledger-at-period-end.md) ve [Mali yılı kapatma](tasks/close-fiscal-year.md).

> [!NOTE]
>  Microsoft Dynamics 365 Finance için Management Reporter'ı kullanarak birden çok tüzel kişilik için mali sonuçları konsolide bir biçimde birleştirmeniz önerilir. Management Reporter, tüzel kişiliklerde konsolide mali raporlar oluşturmanıza, diğer kaynaklardan konsolidasyon verilerini içeri aktarmak için Excel'i kullanmanıza ve Dynamics 365 Finance'te konsolidasyon sürecini çalıştırmak zorunda kalmadan tutarları istediğiniz sayıda raporlama para birimlerine çevirmenize olanak sağlar.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Yan kuruluş ana hesaplarını konsolide ana hesaplarla eşleştirme

Yan kuruluş tüzel kişiliğindeki hesap planı, konsolide tüzel kişilikteki hesap planını izlemiyorsa bağlı kuruluştaki ana hesapları konsolide tüzel kişilikteki ana hesaplarla eşleyebilirsiniz.

1. *Yan kuruluş tüzel kişiliği*'nde, **Genel muhasebe \> Kurulum** \> **Hesap planı \> Hesap planı**'na gidin.
2. Hesap planı seçin. **Ana hesaplar** hızlı sekmesinde, bir ana hesap seçin ve **Düzenle**'yi seçin.
3. Konsolide bir ana şirketle eşlenmesi gereken her bir yan kuruluş hesabını seçin. **Genel** hızlı sekmesinde, **Konsolidasyon hesabı** alanına, seçili yan kuruluş ana hesabına ait bakiyenin veya hareketlerin transfer edileceği konsolide tüzel kişilikteki hesabı girin. Birden fazla yan kuruluş hesabı için aynı konsolide ana hesabı girebilirsiniz.

    > [!NOTE]
    > Eşlenen yan kuruluş hesaplarının ana hesap türleri konsolide tüzel kişilikteki hesapların ana hesap türlerinden farklıysa, konsolidasyon sırasında, **Toplam** ana hesap türüne sahip olan hesapların değerlerinin üzerine yazılır.

4. Mali boyutları esas alan konsolide tüzel kişilikle ilgili raporları ve mali tabloları hazırlayın. Bir alt firmada kullanılan mali boyutları konsolide tüzel kişilikteki mali boyutlarla eşleştirmek için aşağıdaki adımları izleyin:

    1. *Yan kuruluş tüzel kişiliği*'nde, **Genel muhasebe \> Kurulum \> Mali boyutlar \> Mali boyutlar**'a gidin, bir mali boyut seçin ve **Mali boyut değerleri**'ni seçin.
    2. Konsolide tüzel kişilikte farklı bir mali boyut değeriyle eşleştirilecek mali boyut değerini seçin.
    3. **Genel** hızlı sekmesinde, **Grup boyutu** alanına konsolide tüzel kişilikteki mali boyutu girin. Konsolidasyon sırasında, bu mali boyut yan kuruluş tüzel kişiliğinde seçilen mali boyutu kullanan hareketlere ve bakiyelere atanır. Buraya girdiğiniz mali boyutlar konsolide tüzel kişilikte kullanılmalıdır. Grup mali boyutu olarak kullanılan mali boyutu birkaç yan kuruluş mali boyutuna atayabilirsiniz.

5. Çevrimiçi konsolidasyon yapıyorsanız, aktarımların istediğiniz gibi gerçekleştiğine emin olmak için şu adımları izleyin:

    1. *Konsolide tüzel kişilikte*, **\[Çevrimiçi\] Konsolide Et** sayfasını açmak için **Genel muhasebe \> Periyodik \> Konsolide Et \> Konsolide Et \[Dışarı aktarma hedefi\]**'ne gidin.
    2. **Ölçüt** sekmesinde, **Konsolidasyon hesabını kullan** onay kutusunu seçin.
    3. **Mali boyutlar** sekmesinde, uygun mali boyutları seçin.
    4. Seçtiğiniz her mali boyut için, boyutların görünmesi gereken sırayı belirtmek üzere **Segment sırası** alanına bir sayı girin.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Bağlı kuruluşta ve konsolide tüzel kişiliklerde aynı hesap planını tutma

Yan tüzel kişilikteki ana hesaplar, konsolide tüzel kişilikteki ana hesaplarla aynı hesap numaralarına ve hesap planı için aynı yapıya sahip olabilir. Bu durumda, bağlı kuruluştaki ana hesapları konsolide tüzel kişilikteki ana hesaplara el ile eşlemeniz gerekmez.

Konsolidasyona başlamadan önce şu adımları izleyin.

1. *Konsolide tüzel kişilikte*, **\[Çevrimiçi\] Konsolide Et** sayfasını açmak için **Genel muhasebe \> Periyodik \> Konsolide Et \> Konsolide Et \[Dışarı aktarma hedefi\]**'ne gidin.
2. **Konsolidasyon hesabını kullan** onay kutusunu seçin. Konsolidasyon sırasında, hareketler ve bakiyeler otomatik olarak doğru hesaba aktarılır.

> [!NOTE]
> Hesaplar eşleşmezse konsolidasyon durur ve bir ileti alırsınız.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Var olan bir hesap planını temel alan konsolide tüzel kişilik için hesap planı oluşturma

Konsolide tüzel kişilikte henüz bir hesap planı oluşturulmamış olsa bile konsolidasyon yapabilirsiniz.

- Konsolide tüzel kişilikte kullanmak istediğiniz hesap yapısını planladıysanız, yan kuruluş hesaplarını bu yapıyla eşleyebilirsiniz.
- Herhangi bir bağlı kuruluş hesabı eşlemezseniz, bağlı kuruluş verileri konsolide tüzel kişiliğe aktarıldığında konsolide tüzel kişilikteki hesaplar otomatik olarak oluşturulur. Bu hesaplar ana hesaba dayanır. Sonraki veriler, bağlı kuruluş hesaplarıyla aynı hesap numarasına sahip konsolide tüzel kişilikteki hesaplarda birikir.

Hesapları eşlemiş olup olmadığınıza bakılmaksızın, bu tür bir konsolidasyonu çalıştırmadan önce konsolide tüzel kişilikteki **Konsolide Et** sayfasında **Konsolidasyon hesabını kullan** onay kutusunu temizleyin.

> [!NOTE]
> Bu yöntemi, bağlı kuruluş tüzel kişiliklerinden birine ait hesap planından konsolide tüzel kişilikte bir hesap planı oluşturmak için kullanabilirsiniz. Daha fazla bilgi için bkz. [Konsolidasyon hesabı grupları ve ek konsolidasyon hesapları](../budgeting/consolidation-account-groups-consolidation-accounts.md). Ardından, konsolide edilen her ana hesaba uygun bir konsolidasyon dönüştürme ilkesi atayın ve tüm bağlı kuruluş tüzel kişilikleri için konsolidasyonu çalıştırın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]