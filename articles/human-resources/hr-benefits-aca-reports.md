---
title: Uygun Bakım Yasası (ACA) raporları oluşturma
description: Ekonomik Bakım Yasası (ACA) raporlaması, Ekonomik Bakım Yasası'nın **İşveren İçin Zorunlu** kısmını desteklemek için 1095-B ve 1095-C formlarını oluşturur.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053213"
---
# <a name="generate-aca-reports"></a>ACA raporları oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ekonomik Bakım Yasası (ACA) raporlaması, Ekonomik Bakım Yasası'nın **İşveren İçin Zorunlu** kısmını desteklemek için 1095-B ve 1095-C formlarını oluşturur.

> [!NOTE]
> ACA raporlaması yalnızca ABD'deki tüzel kişiler için etkinleştirilir.

## <a name="getting-started"></a>Başlarken

1095-B ve 1095-C formlarının bilgilerini izlemek için önce bir veya daha fazla Ekonomik bakım kapsamı grubu oluşturmanız gerekir. Ekonomik Bakım kapsamı grupları şunları gösterir:

- Bir çalışan için kapsam teklifi
- Maliyet federal yoksulluk sınırının üzerindeyse, çalışanın en düşük maliyetli aylık prim payı
- Varsa işveren tarafından kullanılan Safe Harbor

Ekonomik Bakım kapsamı grupları, koşulların aynı olduğu her çalışan kaydını değiştirmeden bu alanların bilgilerini yönetmenize olanak tanır. Sayfadaki **Toplu atama** seçeneğini kullanarak bir veya daha fazla çalışana Ekonomik Bakım karşılama gruplarını kolayca atayabilirsiniz.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Bir kapsama grubunun birden fazla sürümünü tutmak

Bir kapsama grubunun birden fazla sürümünü tutabilirsiniz. Bu işlevsellik, yeni bir grup oluşturmanıza ve çalışanları yeniden atamanıza gerek kalmadan değişiklik yapmanıza olanak tanır. 

ACA kapsama grupları oluşturduktan sonra, **Toplu atama** seçeneğiyle grupları çalışanlara toplu olarak atayabilirsiniz. Ayrıca, ACA bilgilerinin izlenip izlenmeyeceğini ve raporlanıp raporlanmayacağını, bir çalışanın Ekonomik Bakım kapsamı grubuna atanıp atanmayacağını ayrı ayrı belirtebilirsiniz.

Yarı zamanlı çalışanlar gibi bazı ACA kapsam bilgilerini izlemeniz gerekmez. Bu durumda, **Rapor kapsamı** alanını **Hayır** olarak ayarlayın. İzlenebilir ACA bilgilerine sahip her çalışanı Ekonomik Bakım kapsama grubuna atamanız gerekse de aşağıdaki seçenekleri aylar için farklı değerlerle değiştirebilirsiniz:

- **Kapsam teklifi**
- **Personel maliyet payı**
- **Güvenli Liman**

Ekonomik Bakım kapsamı grubu değerleri için özel durumlar girmek üzere, **İstihdam sekmesindeki** **Ek bilgiler** bölümünün altındaki **Çalışan ayrıntısı** sayfasında **Ekonomik Bakım Kapsamı** bağlantısını seçin.

## <a name="reporting-health-care-coverage"></a>Sağlık bakımı kapsamasını raporlama

Tam zamanlı çalışanlara sunulan sağlık sigortası kapsamını izlemenin yanı sıra işveren, çalışanın kayıtlı olduğu işveren destekli kendi kaynaklarından teminat ayırmayla sigortalı sağlık kapsamı sunuyorsa (istihdam durumlarının tam zamanlı veya yarı zamanlı olmasına bakılmaksızın), 1095-C hakkında ek bilgilerin bildirilmesi gerekir. İşveren tarafından desteklenen kazanç planları tarafından kapsanan her personelin (bakmakla yükümlü olduğu kişi dahil), kapsanmış oldukları aylar için rapora dahil edilmeleri gerekir. 

**ACA raporlanabilir** onay kutusunu seçerek her yan hak planının raporlanıp raporlanmayacağını belirtebilirsiniz.

Ayrıca, çalışanlar bakmakla yükümlü olduğu kişilerden herhangi birinin bir sosyal hak kapsamında olmasını seçtiyse, yükümlü oldukları her çalışan için kapsadığı tarihleri **Sosyal hakları koru** sayfasında belirtebilirsiniz. Bakmakla yükümlü olunan kişinin sosyal hak altında olduğunu belirtmek için **Bakılmakla Yükümlü Olunan Kişiler** hızlı sekmesinin eylem bölmesinde **Düzenle** düğmesini seçin.

**Bakılmakla yükümlü kapsama veri yöneticisi** sayfası üzerinde, bakılmakla yükümlü kişinin kazanç tarafından kapsandığı tarihi belirtebilirsiniz. Bu sayfaya tarihler girmek, **Kazançları koru** sayfası üzerindeki **Kapsanan** onay kutusunu otomatik seçer.

## <a name="generate-1095-b-and-1095-c-forms"></a>1095-B ve 1095-C formları oluşturma

Ayrıca ürünün içinden 1095-B ve 1095-C formları oluşturabilir ve bunları çalışanlarınızın her birine dağıtabilirsiniz. Sistem ayrıca elektronik olarak 1095-C formları ve 1094-C IRS iletim dosyaları üretebilir.  

1095-C formunu oluştururken, uygun vergi yılını girin ve sosyal güvenlik numaralarının maskelenip maskelenmemesi gerektiğini belirtin. 500'den fazla çalışan için 1095-C formları yazdırıyorsanız birden fazla PDF dosyası alırsınız. **Belge yönetimi parametreleri** penceresindeki **Maksimum dosya boyutu**'nu 150 MB'a artırmanız önerilir.

## <a name="viewing-information"></a>Görüntüleme bilgisi

**Çalışan Ekonomik Bakım kapsamı** sayfasını, hangi personellerin her bir kapsama grubuna atandığını, hangi personellerin bir rapora dahil edilmesi gerekmediğini ve hangi personellerin atanmamış olduğunu görmek için kullanabilirsiniz.

Ekonomik Bakım kapsama grubundaki varsayılan değerlerden herhangi biri geçersiz kılınmışsa değiştirilen değerin yanında bir yıldız işareti görünür. 12 ayın tamamı için değerler aynı ise ve geçersiz kılınmamışsa, değer **Tüm 12 ay** sütununda yazdırılır.

Ayrıca, hangi çalışanların ACA raporuna dahil edilemeyecek olarak işaretlendiğini anlamak için sorgulama penceresini de kullanabilirsiniz. Kapsamın kendilerine sunulup sunulmadığını izlemenize gerek yoktur ve yıl sonunda onlara 1095-C yayınlamanıza gerek yoktur. 1095-C almayan tüm çalışanların listesini oluşturmak için **Filtreleme ölçütü** alanında **Raporlanabilir Değil**'i seçin.

Ayrıca, atanmamış (**ACA Raporu kapsamı** alanı boş) veya **Yıl** alanında seçilen yıl için süresi dolmuş bir Ekonomik Bakım kapsama grubuna atanmış çalışanları görüntüleyebilirsiniz.

Filtreleme seçeneklerinden herhangi birini kullanarak oluşturulan personel listelerini Excel'e aktarabilirsiniz.

Kendi kaynaklarından teminat ayırmayla sigorta kapsamı sağladığınız için kapsanan kişileri bildirmeniz gerekiyorsa **ACA raporlanabilir** olarak işaretlenmiş sosyal hak planları kapsamındaki bakılmakla yükümlü olunan kişileri görüntüleyebilirsiniz. Eylem bölmesinde **Bakılmakla yükümlü olunan kişi kapsamını görüntüle**'yi seçin.

> [!NOTE]
> Sorgulama penceresinde yalnızca **ACA raporlanabilir** olarak işaretlenmiş sosyal hak planları görüntülenir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]