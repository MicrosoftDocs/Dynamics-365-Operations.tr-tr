--- 
title: "Maddeler için kapsam kurallarını tanımlama"
description: "Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3b34d2c35bc96cf75e9e699b835f7bcbbce1312b
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="define-coverage-rules-for-items"></a>Maddeler için kapsam kurallarını tanımlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam, kapsam kurallarını oluşturmayı ve belirli bir madde için kapsama ayarlarını geçersiz kılmayı gösterir. Ayrıca varsayılan stok ayarlarının nasıl belirleneceğini de açıklar.


## <a name="create-a-coverage-group"></a>Bir kapsam grubu oluşturma
1. Kapsam gruplarına gidin.
2. Yeni'ye tıklayın.
3. Kapsam grubu alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Takvim alanına bir değer yazın.
    * Nazım planlamanın bu gruptaki maddelerin stok yenilemesi önerilerini oluşturmak için kullandığı takvimi seçin.  
6. Kapsam kodu alanında bir seçenek seçin.
    * Bu yordam için gereksinimi seçin.  
7. Kapsam zaman dilimi (gün) alanına '90' girin.
    * Bu gruptaki maddeler için, master planlama gelecek en fazla 90 gün için stok yenileme önerileri oluşturur.  
8. Negatif günler alanına '1' girin.
9. Pozitif günler alanına '1' girin.
10. Diğer bölümünü genişletin veya daraltın.
11. Gereksinim tarihine eklenen giriş marjı alanına '1' girin.
    * Örneğin giriş marjı bir gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir giriş için bir satın alma siparişi satırı planlanırsa, nazım planlama ayarlanan giriş tarihini 16 mayıs olarak hesaplar.  
12. Gereksinim tarihinden kesilen çıkış marjı alanına '1' girin.
    * Örneğin emniyet marjı 1 gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir teslimat için bir satış siparişi satırı planlanırsa, nazım planlama ayarlanan teslim tarihini 14 mayıs olarak hesaplar.  
13. Madde sağlama süresine eklenen sipariş yenileme sınırı alanına '1' girin.
14. Kaydet'e tıklayın.

## <a name="create-a-new-product"></a>Yeni bir ürün oluştur
1. Serbest bırakılan ürünler öğesine gidin.
2. Yeni'ye tıklayın.
3. Ürün numarası alanında bir değer girin.
4. Ürün adı alanına bir değer girin.
5. Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, istenen kaydı bulun ve seçin.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. Depolama alanında, aramayı açmak için açılır menü düğmesine tıklayın.
12. Listede, istenen kaydı bulun ve seçin.
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. İzleme boyutu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
15. Listede, istenen kaydı bulun ve seçin.
16. Listede, seçili satırdaki bağlantıya tıklayın.
17. Tamam'a tıklayın.

## <a name="setup-default-order-settings"></a>Varsayılan sipariş ayarlarını yapma
1. Eylem Bölmesinde, Planla öğesine tıklayın.
2. Varsayılan sipariş ayarlarına tıklayın.
3. Satınalma tesisi alanına, satınalma siparişleri oluşturulurken varsayılan olarak kullanılan tesisi yazın.
4. Stok sahası alanına, maddenin depolandığı sahayı yazın.
5. Stok bölümünü genişletin veya daraltın.
6. Birden çok ayarını '10' olarak belirleyin.
7. Min. sipariş miktarını '10' olarak ayarlayın.
8. Maks. sipariş miktarını '100' olarak ayarlayın.
9. Standart sipariş miktarını '10' olarak ayarlayın.
10. Satınalma sağlama süresi alanına bir sayı girin.
11. Çalışma günleri onay kutusunu seçin veya temizleyin.
12. Kaydet'e tıklayın.
13. Varsayılan sipariş türü alanında 'Satınalma siparişi'ni seçin.
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.
    * Varsayılan sipariş ayarları sayfasını kapatın.  

## <a name="add-an-item-to-a-coverage-group"></a>Kapsama grubuna bir madde ekleme
1. Plan bölümünü genişletin veya daraltın.
2. Kapsam grup alanında, aramayı açmak için açılır menü düğmesine tıklayın.
3. Listede, oluşturduğunuz Kapsam grubunu bulun.
4. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="create-item-coverage-rules"></a>Madde kapsama kuralları oluşturma
1. Eylem Bölmesinde, Planla öğesine tıklayın.
2. Madde kapsamı'na tıklayın.
3. Yeni'ye tıklayın.
4. Genel sekmesine tıklayın.
5. Karşılama grubu ayarlarını geçersiz kılma başlığı kutusunu işaretleyin.
6. Kapsam zaman dilimi (gün) alanına '60' girin.
    * Gereklilik grubu kapsamındaki maddeler 90 gün önceden planlanmasına rağmen, bu madde 60 gün önceden planlanacaktır.  
7. Negatif günler alanına '2' girin.
8. Pozitif günler alanına '2' girin.
9. Sağlama süresi sekmesine tıklayın.
10. Satın alma başlığındaki onay kutusunu seçin.
11. Satınalma zamanı alanına '5' girin.
12. Kaydet'e tıklayın.


