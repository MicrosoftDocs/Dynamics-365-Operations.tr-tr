---
title: Banka hesabı için mutabakat sağlama
description: Bu konu, bir banka hesabının nasıl mutabakatı yapılacağını açıklar.
author: panolte
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9d6b5b07cac8910f7706af718a7dd6d524c67075
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835064"
---
# <a name="reconcile-a-bank-account"></a>Banka hesabı için mutabakat sağlama

[!include[banner](../includes/banner.md)]

Bir banka ekstresi aldığınızda, yasal varlık banka hareketlerinin banka ekstresi üzerindeki hareketlerle düzenli aralıklarla mutabakatını sağlamanız gerekir.

Ekstrede listelenen herhangi bir çek veya havale makbuzu ödemesi **Bekleyen iptal** durumundaysa, banka hesabı ekstresi mutabakatını yapamazsınız. Gözden geçiren bir kişi çekin ters işlemini veya havale makbuzu ödemesi iptalini deftere nakleder veya reddederse, durum artık **Bekleyen iptal** olmaz ve banka hesabı mutabakatını sağlayabilirsiniz.

1.  **Nakit ve banka yönetimi** \> **Banka hesapları** \> **Banka hesapları** öğesine gidin. Banka ekstresi ile mutabakat için banka hesabını ve **Mutbakat** > **Hesap mutabakatı** seçin.

2.  **Banka ekstresi tarihi** ve **Banka ekstresi** alanlarına bilgi girin. **Kapanış bakiyesi** alanında, banka hesabının bakiyesini banka hesap ekstresinde görüntülendiği şekilde girin.

3.  **Hesap mutabakat** sayfasını açmak için **Hareketleri** seçin.

4.  Banka hesabı ekstresindeki her hareket için Dynamics 365 Finance'daki tutar banka hesabı ekstresindeki tutara karşılık geliyorsa **Temizlenmiş** onay kutusunu seçin. Ayrıca, **Banka hareket türü** alanına değeri girebilir veya değiştirebilirsiniz. Bu alan değeri, banka hesabı istatistikleri ve bazı raporlar için önemlidir.
    

    > [!NOTE]
    > <P>Banka ekstresinde olmayan hareketlerde <STRONG>Temizlenmiş</STRONG> onay kutusunu seçmeyin. Bu hareketler, sonraki bir banka hesabı ekstresiyle mutabakatları sağlanıncaya kadar bu sayfada görünmeye devam eder.</P>
    > <P>Hareket <STRONG>Bekleyen iptal</STRONG> durumundaysa, <STRONG>Temizlenmiş</STRONG> onay kutusu kullanılamaz. Finance ters işlemlerin ve iptal işlemlerinin deftere nakledilmeden önce gözden geçirilmesini gerektirecek şekilde ayarlanırsa, hareketler bu durumda olabilir. Gözden geçiren bir kişi çekin ters işlemini veya iptalini deftere nakleder veya reddederse, durum artık <STRONG>Bekleyen iptal</STRONG> olmaz ve banka ekstresi ile banka hesabı mutabakatını sağlayabilirsiniz.</P>

    
    Hepsi banka ekstresi üzerinde görüntülenen denetim aralığı için **Temizlenmiş** onay kutusunu seçmek için onay aralığı **Çek aralığını işaretle**'yi seçin ve sonra aralığı belirtin.

5.  Banka hesabı hareketinin tutarı banka ekstresi üzerindeki hareketin tutarına karşılık gelmiyorsa, düzeltme tutarını **Düzeltme tutarı** alanına girin.
    

    > [!NOTE]
    > <P>Düzeltilecek hareketin mali dönemi kapatıldıysa, <STRONG>Düzeltme tutarı</STRONG> alanı kullanılamaz. Bunun yerine, düzeltme için açık mali dönemde bulunan bir hareket tarihiyle bir satır oluşturun. Bu durumda, özgün işlemde kullanılan mali boyutları ve ayrıca mahsup ana hesabı eklemeniz gerekir.</P>



6.  Banka ekstresinde bulunan ancak Finance'te kayıtlı olmayan girişler (masraflar veya faiz vb.) için hareketler oluşturun. **Banka hareket türünü** ve uygun mali boyutlarını girin.

7.  Banka hesabı ekstresindeki hareketler **Temizlenmiş** olarak işaretlenirse, **Mutabakat sağlanmadı** alanındaki tutar (siz değişiklik yaptıkça sürekli olarak yeniden hesaplanır) sıfıra ulaşır. Sıfıra ulaştığında, mutabakatı ve oluşturduğunuz hareketleri ve düzeltmeleri deftere nakletmek için **Hesap mutabakatı sağla**'yı seçin.
    
    Mutabakat deftere nakledildikten sonra, eklenmiş olan hareketler bir daha değiştirilemez veya düzeltilemez ve daha sonraki hesap mutabakatında görünmez.

8.  Henüz mutabakatlı olmayan banka hareketlerini görüntülemek için **Mutabakat sağlanmamış banka hareketleri** raporunu kullanın. Banka hesabının banka ekstresini görüntülemek için **Banka ekstresi** raporunu kullanın.

## <a name="cancel-bank-statement-reconciliation"></a>Banka ekstresi mutabakatını iptal et 

Banka ekstresi mutabakat işlevselliğini iptal etmek, banka ekstresi mutabakatını iptal etmenizi sağlar. Bu özelliği kullanmak için,**Özellik Yönetimi** çalışma alanında **Banka ekstresi mutabakatı iptali** özelliğini etkinleştirin. Ayrıca **Banka ekstresi düzenlemeye izin ver** parametresini etkinleştirmeniz gerekir. Bunu yapmak için **Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri > Banka mutabakatı**'na gidin.
 
Banka ekstresi mutabakatları yalnızca girildikleri kronolojik sırada iptal edilebilir. Bir banka ekstresi mutabakatı iptal edildiğinde, yeni hareketler ve düzeltmeler tersine çevrilir ve diğer tüm işlemler mutabakat sağlanacak şekilde işaretlenir.
 
Banka ekstresi mutabakatını iptal etmek için banka ekstresini seçin ve **Banka ekstresi > Banka mutabakatını iptal et**'i seçin. **Banka mutabakatını iptal et** sayfasında **Neden kodu**, **Neden yorumu** ve **İptal tarihini** sağlayın. İptal başlangıcı için **Tamam**'ı seçin. Unutmayın, banka ekstresi iptal tarihi banka ekstresi tarihinde veya sonra olmalıdır. Banka ekstresi mutabakatı iptal edildikten sonra banka ekstresi için **İptal tarihi** alanı sağlanan **İptal tarihi** ile güncelleştirilir. Mutabakatı iptal edilen hareketleri görüntülemek için **Hareketler** düğmesini seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]