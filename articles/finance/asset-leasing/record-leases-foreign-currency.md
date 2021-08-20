---
title: Kiraları yabancı para birimlerinde kaydetme
description: Bu konu, kiraların muhasebe veya raporlama para birimi dışındaki para birimlerinde nasıl oluşturulacağını açıklamaktadır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 91bf3f91614f0dd4835c253456128c9ced046749c0e13383590e01dfd436c921
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766349"
---
# <a name="record-leases-in-foreign-currencies"></a>Kiraları yabancı para birimlerinde kaydetme

[!include [banner](../includes/banner.md)]

Muhasebe para birimi veya raporlama para birimi dışındaki para birimlerinde olan kiralamalar için varlık kiralama hesapları, **Genel muhasebe kurulumu** sayfasında oluşturulur. Tüm kiralamalar hareket para birimi cinsinden girilmelidir. Diğer bir ifadeyle, bunlar kiralama sözleşmesinde belirtilen para biriminde girilmelidir. Bu konu, kiraların muhasebe veya raporlama para birimi dışındaki para birimlerinde nasıl oluşturulacağını açıklamaktadır.

Kirayı yabancı bir para biriminde girerseniz kullanım hakkı (ROU) varlığına hem muhasebe para biriminde hem de raporlama para biriminde amortisman uygulanır. Bu para birimleri, **Genel muhasebe kurulumu** sayfasında yapılandırılabilir. Bu davranış Sabit varlıklarda da kullanılır. Yabancı bir para biriminde kiralama oluşturduğunuzda **Para birimi** alanında hareket para birimini seçin.

Muhasebe para biriminin döviz kuru, **Muhasebe para birimi döviz kuru** alanındaki varsayılan değerdir. Raporlama para biriminin döviz kuru, **Raporlama para birimi döviz kuru** alanındaki varsayılan değerdir. Bu döviz kurları kiralamanın başlangıç tarihinde geçerli olan kurlardır. **Muhasebe para birimi döviz kuru** ve **Raporlama para birimi döviz kuru** alanları, **Kiralama ayrıntıları** sayfasındaki **Mali ve raporlama kambiyo bilgileri** hızlı sekmesinde yer alır.

1. Otomatik olarak girilen döviz kurunu geçersiz kılmak için **Sabit kur** onay kutusunu işaretleyin ve sonra yeni kuru girin.
2. Diğer alanlara kiralama için gereken bilgileri girin ve **Planlama oluştur**'u seçin.
3. Yeni **Kiralama ayrıntıları** sayfasında **Defterler**'i seçin.
4. **Kiralama defteri**'ndeki **Mali ve raporlama kambiyo bilgileri** sekmesinde, **Muhasebe para birimi ilk kullanım hakkı varlığı** ve **Raporlama para birimi ilk kullanım hakkı varlığı** alanlarındaki değerleri doğrulayın. Bu alanların her biri ilgili para birimi cinsinden çevrilen ROU varlık bakiyesini gösterir. Bu alanlar, herhangi bir mali bilgiyi her değiştirdiğinizde güncelleştirilir. Ödeme planını onaylamadan önce **Planlama oluştur** seçeneğini belirleyin.

    İlk kabul günlük girişi, kiralamada listelenen döviz kurlarını kullanan ROU varlığını kaydeder. Günlük girişi aynı zamanda **Muhasebe para birimi ilk kullanım hakkı varlığı** ve **Raporlama para birimi ilk kullanım hakkı varlığı** alanlarının değerlerini içerir.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Yabancı para biriminde kiralamalar için sonraki ölçüm

Amortisman planı, beklenen amortisman gideri tutarlarını raporlama para birimi, muhasebe para birimi ve hareket para birimi cinsinden gösterir.

ROU varlığı bakiyelerini ve amortisman tutarlarını raporlama para birimi veya muhasebe para birimi cinsinden görüntülemek için, **Varlık amortisman planı** sayfasını açın ve **Muhasebe para birimi tutarlarını göster** veya **Raporlama para birimi tutarlarını göster** onay kutusunu seçin.

Yabancı bir para biriminde gösterilen bir kiralamayla ilgili amortisman gider günlüğü girişleri oluşturduğunuzda giriş, kiralamada listelenen döviz kurlarını kullanır. Aynı zamanda **Muhasebe para birimi ilk kullanım hakkı varlığı** ve **Raporlama para birimi ilk kullanım hakkı varlığı** alanlarının değerlerini içerir.

Nihai amortisman gider tutarı biraz farklı bir döviz kuru kullanılarak hesaplanabilir ve böylece ROU varlığı hem muhasebe para biriminde hem de raporlama para biriminde tümüyle amorti edilir.

Kiralama **Ertelenmiş kira** olarak yeniden sınıflandırıldığında sistem, muhasebe ve raporlama para birimlerinin döviz kurları zaten tanımlanmışsa, bunları otomatik olarak temizler.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
