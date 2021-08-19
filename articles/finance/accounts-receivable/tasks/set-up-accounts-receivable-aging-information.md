---
title: Alacak hesapları yaşlandırma bilgilerini ayarlama ve oluşturma
description: Bu kılavuz, yaşlandırma dönemi tanımı yapmanıza, müşteri bakiyelerini yaşlandırmanıza, Yaşlandırılmış bakiye listesinde ve Tahsilatlar sayfasında bakiyeleri görüntülemenize yardımcı olur.
author: mikefalkner
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2468beea898de6367c655b54d89c1faab1e4435506bd21019c970af32d215729
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713294"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Alacak hesapları yaşlandırma bilgilerini ayarlama ve oluşturma

[!include [banner](../../includes/banner.md)]

Bu kılavuz, yaşlandırma dönemi tanımı yapmanıza, müşteri bakiyelerini yaşlandırmanıza, Yaşlandırılmış bakiye listesinde ve Tahsilatlar sayfasında bakiyeleri görüntülemenize yardımcı olur. Bu kayıtta USMF demo şirketi kullanılmaktadır.


## <a name="create-an-aging-period-definition"></a>Yaşlandırma dönemi tanımı oluşturun
1. **Gezinti bölmesinde Modüller > Alacak ve tahsilatlar > Kurulum > Yaşlandırma dönemi tanımları**'na gidin.
2. **Yeni**'ye tıklayın.
3. **Yaşlandırma dönemi tanımı** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.
5. Yeni yaşlandırma dönemi eklemek için **Alta ekle**'ye tıklayın.
6. **Dönem** alanına, yaşlandırma raporlarını göstermek için açıklamayı girin.
7. **Birim** alanına bir sayı girin.
8. **Aralık** alanında bir seçenek belirtin. Genel muhasebe dönemi, genel muhasebe takviminize denk gelir. Gün, hafta, ay, üç aylık dönem ve yıl, tarih türüne aralığın boyutunu tanımlar. Sınırsız seçeneği, dönemin ilk veya son dönem olmasına bağlı olarak, önceki veya sonraki hareketlerin tümünü seçer.  
9. **Yaşlandırma göstergesi** alanında bir seçenek belirtin.
10. Kılavuzun en üstündeki dönemi seçin. Yaşlandırma dönemi tanımındaki en eski dönemi belirtmek için açıklamayı güncelleştirin
11. **Dönem** alanına, yaşlandırma döneminin yeni açıklamasını girin.
12. Sayfayı kapatın.

## <a name="age-the-balances"></a>Bakiyeleri yaşlandırın
1. **Alacak ve tahsilatlar > Dönemsel görevler > Müşteri bakiyelerini yaşlandır**'a gidin.
2. **Yaşlandırma dönemi tanımı** alanında, oluşturduğunuz yaşlandırma dönemi tanımını seçin.
    + Her yaşlandırma dönemi için birer etkin anlık görüntü alabilirsiniz.  
    + Tüm müşteriler varsayılan olarak işlenir. Tek bir müşteri tahsilatları havuzu hesaplamak için bu seçimi kullanabilirsiniz.  
    + Yaşlandırma için kullanacağınız hareketten tarihi seçin.  
    + Yaşlandırma için bir "başlangıç" tarihi seçin. Varsayılan değer bugündür, ancak bu alanı Seçili tarih olarak değiştirirseniz, istediğiniz tarihi seçebilirsiniz. Toplu işlem için, Bugünün tarihi'ni kullanın.  
3. **Şirket** aralığını genişletin. Anlık görüntüye dahil edilecek şirketleri seçebilirsiniz. Geçerli şirket varsayılan olarak seçilidir.
4. Anlık görüntüyü işlemek için **Tamam**'ı tıklatın. Bu işlem biraz zaman alır, bu nedenle sürgünün kaybolmasını bekleyin ve mesaj merkezinde mesaj görüntülenip görüntülenmediğini kontrol edin.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Tahsilat sayfasında Yaşlandırılmış bakiyeler listesini görüntüleyin
1. **Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler**'e gidin. Liste sayfası müşteri bakiyelerini gösterir. Yaşlandırma simgesi, en eski hareketin yaşlandırma dönemini gösterir.  
2. Bakiyesi olan bir müşteri seçin.
3. Yaşlandırılmış bakiyeleri görüntülemek için **Yaşlandırma bilgi** kutusu alanını genişletin. Bilgi kutusu için yaşlandırma dönemi tanımı, parametrelerde belirtilmiş varsayılan yaşlandırma dönem tanımından alınır. Bunu, Toplama menüsünü kullanarak değiştirebilirsiniz.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]