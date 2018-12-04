--- 
title: "Plaka etiketi yazdırmayı etkinleştirme"
description: "Bu yordam, satış malzeme çekme işinde stoktan son madde çekildikten sonra Seri sevkiyat konteyner kodu (SSCC) etiketini otomatik olarak yazdırma konusunda açıklama sağlar."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="enable-license-plate-label-printing"></a>Plaka etiketi yazdırmayı etkinleştirme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, satış malzeme çekme işinde stoktan son madde çekildikten sonra Seri sevkiyat konteyner kodu (SSCC) etiketini otomatik olarak yazdırma konusunda açıklama sağlar. Bu yordamı USMF demo veri şirketinde çalıştırabilirsiniz. Kendi verilerinizi kullanarak çalıştırırsanız, lisans plakaları için ayarlanmış bir numara seriniz olması gerekir. Bu göreve başlamadan önce bir etiket yazdırıcı kurulumu yapmanız gerekir. Organizasyon yönetimi > Kurulum > Ağ yazıcıları öğesine gidin. Eylem bölmesinde, Seçenekler'e ve ardından Belge rota aracısı yükleyicisini indir düğmesine tıklayın. Yükleyiciyi çalıştırın ve yordama devam etmeden önce Etkin olarak ayarlanmış çalışır durumda bir ağ yazıcınız olduğundan emin olun.


## <a name="set-up-the-gs1-company-prefix"></a>GS1 şirket önekini ayarlayın
1. Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.
2. GS1 şirket öneki alanına, GS1 şirket numaranız için 7 sayı girin.
3. Kaydet'e tıklayın.
4. Sayfayı kapatın.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>SSCC lisans plaka numarası serisini ayarlayın
1. (Kuruluş yönetim > Numara serileri > Numara serileri'ne tıklayın.
2. Alan alanında bir seçenek seçin.
3. Referans alanında bir seçenek seçin.
4. Şirket alanına bir değer yazın.
5. Listede, seçili satırı işaretleyin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Segmentler bölümünü genişletin.
8. Düzenle öğesine tıklayın.
9. Segment tablosunda ilk satırı seçin.
10. Kaldır'a tıklayın.
11. Kaldır'a tıklayın.
12. Kaydet'e tıklayın.
13. Sayfayı kapatın.

## <a name="create-the-document-route-layout"></a>Belge yönlendirme düzenini oluşturun
1. Ambar yönetimi > Kurulum > Belge rotası > Belge rotası düzenleri öğesine gidin.
    * SSCC düzenini etkinleştirin.  
2. Yeni'ye tıklayın.
3. Düzen kodu alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Listede, istenen kaydı bulun ve seçin.
6. Metnin sonuna ekle'ye tıklayın.
7. Kaydet'e tıklayın.
8. Sayfayı kapatın.

## <a name="set-up-the-document-routing"></a>Belge yönlendirmeyi ayarlayın
1. Ambar yönetimi > Kurulum > Belge rotası > Belge rotası öğesine gidin.
2. İş siparişi türü alanında bir seçenek seçin.
3. Yeni'yi tıklatın.
4. Ambar alanına bir değer yazın.
5. İsim alanına bir değer yazın.
6. Yeni'yi tıklatın.
7. Düzen kodu alanına bir değer girin veya buradan bir değer seçin.
8. Ad alanında kullanmak istediğiniz yazıcı adını girin.
9. Kaydet'e tıklayın.
10. Sayfayı kapatın.

## <a name="create-mobile-device-menu"></a>Mobil cihaz menüsü oluşturun
1. Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğeleri seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Menü öğesi adı alanına bir değer girin.
4. Başlık alanına bir değer yazın.
5. Mod alanında bir seçenek seçin.
6. Mevcut işi kullan alanında Evet'i seçin.
7. Lisans plakası oluştur alanında Evet'i seçin.
8. İş sınıfları bölümünü genişletin.
9. Yeni'ye tıklayın.
10. İş sınıfı kodu alanında bir değer girin.
11. Kaydet'e tıklayın.
12. Sayfayı kapatın.
13. Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğesine gidin.
14. Listede, istenen kaydı bulun ve seçin.
15. Ağaçta, 'Ağaçta, daha önce oluşturduğunuz menü öğesini seçin' seçeneğini seçin.
16. Düzenle'yi tıklatın.
17. Menüye menü öğesi eklemek için oka tıklayın.
18. Kaydet'e tıklayın.
19. Sayfayı kapatın.

## <a name="update-a-work-template"></a>İş şablonu güncelleştirme
1. Ambar yönetimi > Kurulum > İş > İş şablonları öğesine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Düzenle öğesine tıklayın.
4. Yeni'yi tıklatın.
5. Listede, seçili satırı işaretleyin.
6. İş türü alanında 'Yazdır'ı seçin.
7. İş sınıfı kodu alanına bir değer girin veya buradan bir değer seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Yukarı taşı'ya tıklayın.
10. Kaydet'e tıklayın.
11. Sayfayı kapatın.


