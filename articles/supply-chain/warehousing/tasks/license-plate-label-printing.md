---
title: Plaka etiketi yazdırmayı etkinleştirme
description: Bu konu, satış malzeme çekme işinde stoktan son madde çekildikten sonra Seri sevkiyat konteyner kodu (SSCC) etiketini otomatik olarak yazdırma konusunda açıklama sağlar.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a608e9a2356f9dd49bbec1bcbe5489af5931d44
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830894"
---
# <a name="enable-license-plate-label-printing"></a>Plaka etiketi yazdırmayı etkinleştirme

[!include [banner](../../includes/banner.md)]

Bu konu, satış malzeme çekme işinde stoktan son madde çekildikten sonra Seri sevkiyat konteyner kodu (SSCC) etiketini otomatik olarak yazdırma konusunda açıklama sağlar. Bu yordamı USMF demo veri şirketinde çalıştırabilirsiniz. Kendi verilerinizi kullanarak çalıştırırsanız, lisans plakaları için ayarlanmış bir numara seriniz olması gerekir. Bu göreve başlamadan önce bir etiket yazdırıcı kurulumu yapmanız gerekir. Organizasyon yönetimi > Kurulum > Ağ yazıcıları öğesine gidin. Eylem Bölmesi'nde, Seçenekler'e ve ardından Belge rota aracısı yükleyicisini indir düğmesine tıklayın. Yükleyiciyi çalıştırın ve yordama devam etmeden önce Etkin olarak ayarlanmış çalışır durumda bir ağ yazıcınız olduğundan emin olun.


## <a name="set-up-the-gs1-company-prefix"></a>GS1 şirket önekini ayarlayın
1. **Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Ambar > Yönetim parametreleri**'ne gidin.
2. **GS1 şirket öneki** alanına, GS1 şirket numaranız için 7 sayı girin.
3. **Kaydet**'i seçin.
4. Sayfayı kapatın.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>SSCC lisans plaka numarası serisini ayarlayın
1. **Gezinti bölmesi > Modüller > Kuruluş yönetimi > Numara serileri > Numara serileri**'ne gidin.
2. **Alan** alanında bir seçenek seçin.
3. **Referans** alanında bir seçenek seçin.
4. **Şirket** alanına bir değer yazın.
5. **Segmentler** bölümünü genişletin.
6. **Düzenle** öğesini seçin.
7. **Segment** tablosunda ilk satırı seçin.
8. **Kaldır**'ı seçin.
9. **Kaldır**'ı seçin.
10. **Kaydet**'i seçin.
11. Sayfayı kapatın.

## <a name="create-the-document-route-layout"></a>Belge yönlendirme düzenini oluşturun
1. **Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Belge rotası > Belge rotası düzenleri** öğesine gidin. SSCC düzenini etkinleştirin.  
2. **Yeni**'yi seçin.
3. **Düzen kodu** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.
5. **Metnin sonuna ekle**'yi seçin.
6. **Kaydet**'i seçin.
7. Sayfayı kapatın.

## <a name="set-up-the-document-routing"></a>Belge yönlendirmeyi ayarlayın
1. **Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Belge rotası > Belge rotası** öğesine gidin.
2. **İş emri türü** alanında bir seçenek seçin.
3. **Yeni**'yi seçin.
4. **Ambar** alanına bir değer yazın.
5. **Ad** alanına bir değer yazın.
6. **Yeni**'yi seçin.
7. **Düzen kodu** alanına bir değer girin veya buradan bir değer seçin.
8. **Ad** alanında kullanmak istediğiniz yazıcı adını girin.
9. **Kaydet**'i seçin.
10. Sayfayı kapatın.

## <a name="create-mobile-device-menu"></a>Mobil cihaz menüsü oluşturun
1. **Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menü öğeleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Menü öğesi adı** alanına bir değer girin.
4. **Başlık** alanına bir değer yazın.
5. **Mod** alanında bir seçenek seçin.
6. **Mevcut işi kullan** alanında **Evet**'i seçin.
7. **Lisans plakası oluştur** alanında **Evet**'i seçin.
8. **İş sınıfları** bölümünü genişletin.
9. **Yeni**'yi seçin.
10. **İş sınıfı kodu** alanında bir değer girin.
11. **Kaydet**'i seçin.
12. Sayfayı kapatın.
13. **Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menü**'ye gidin.
14. Ağaçta, daha önce oluşturduğunuz menü öğesini seçin.
15. **Düzenle** öğesini seçin.
16. Menüye menü öğesi eklemek için oku seçin.
17. **Kaydet**'i seçin.
18. Sayfayı kapatın.

## <a name="update-a-work-template"></a>İş şablonu güncelleştirme
1. **Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > İş > İş şablonları**'na gidin.
2. **Düzenle** öğesini seçin.
3. **Yeni**'yi seçin.
4. **İş türü** alanında **Yazdır**'ı seçin.
5. **İş sınıfı kodu** alanına bir değer girin veya buradan bir değer seçin.
6. **Yukarı taşı**'yı seçin.
7. **Kaydet**'i seçin.
8. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]