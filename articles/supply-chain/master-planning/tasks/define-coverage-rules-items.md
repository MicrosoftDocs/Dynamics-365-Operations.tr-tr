---
title: Maddeler için kapsam kurallarını tanımlama
description: Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d92185bdbcf7aa1a668b6d2aa311805e42293c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439315"
---
# <a name="define-coverage-rules-for-items"></a>Maddeler için kapsam kurallarını tanımlama

[!include [banner](../../includes/banner.md)]

Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam, kapsam kurallarını oluşturmayı ve belirli bir madde için kapsama ayarlarını geçersiz kılmayı gösterir. Ayrıca varsayılan stok ayarlarının nasıl belirleneceğini de açıklar.


## <a name="create-a-coverage-group"></a>Bir kapsam grubu oluşturma
1. **Gezinti bölmesi > Modüller > Master planlama > Kurulum > Kapsam grupları**'na gidin.
2. **Yeni**'ye tıklayın.
3. **Kapsam grubu** alanına bir değer yazın.
4. **Ad** alanına bir değer yazın.
5. **Takvim** alanına bir değer yazın. Nazım planlamanın bu gruptaki maddelerin stok yenilemesi önerilerini oluşturmak için kullandığı takvimi seçin.  
6. **Kapsam kodu** alanında bir seçenek seçin. Bu yordam için 'Gereksinim'i seçin.  
7. **Kapsam zaman dilimi (gün) alanı**'na '90' girin. Bu gruptaki maddeler için, master planlama gelecek en fazla 90 gün için stok yenileme önerileri oluşturur.  
8. **Negatif günler** alanına '1' girin.
9. **Pozitif günler** alanına '1' girin.
10. **Diğer** bölümünü genişletin veya daraltın.
11. **Gün sayısı olarak emniyet marjları** bölümünde, **Gereksinim tarihine eklenen giriş marjı** alanına '1' girin. Örneğin giriş marjı bir gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir giriş için bir satın alma siparişi satırı planlanırsa, nazım planlama ayarlanan giriş tarihini 16 mayıs olarak hesaplar.  
12. **Gereksinim tarihinden kesilen çıkış marjı** alanına '1' girin. Örneğin emniyet marjı 1 gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir teslimat için bir satış siparişi satırı planlanırsa, nazım planlama ayarlanan teslim tarihini 14 mayıs olarak hesaplar.  
13. **Madde sağlama süresine eklenen sipariş yenileme sınırı** alanına '1' girin.
14. **Kaydet**'e tıklayın.

## <a name="create-a-new-product"></a>Yeni ürün oluşturma
1. **Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.
2. **Yeni**'ye tıklayın.
3. **Ürün numarası** alanında bir değer girin.
4. **Ürün adı** alanına bir değer yazın.
5. **Madde modeli grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. **Madde modeli** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, istenen kaydı bulun ve seçin.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. **Depolama boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
12. Listede, istenen kaydı bulun ve seçin.
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. **İzleme boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
15. Listede, istenen kaydı bulun ve seçin.
16. Listede, seçili satırdaki bağlantıya tıklayın.
17. **Tamam**'a tıklayın.

## <a name="setup-default-order-settings"></a>Varsayılan sipariş ayarlarını yapma
1. **Eylem Bölmesi**'nde **Plan**'a tıklayın.
2. **Sipariş ayarları**'nın altında, **Varsayılan sipariş ayarları**'na tıklayın.
3. **Satınalma siparişi**'nin altında, **Varsayılan site** alanında satınalma siparişleri oluşturulurken varsayılan olarak kullanılan tesisi yazın.
4. **Varsayılan ambar** alanına, maddenin depolandığı sahayı yazın.
5. **Stok** bölümünü genişletin veya daraltın.
6. **Çoklu** alanına '10' yazın.
7. **Minimum sipariş miktarı** alanına '10' yazın.
8. **Maksimum sipariş miktarı** alanına '100' yazın.
9. **Standart sipariş miktarı** alanına '10' yazın.
10. **Satınalma sağlama süresi** alanına bir sayı girin.
11. **Çalışma günleri** onay kutusunu seçin veya temizleyin.
12. **Kaydet**'e tıklayın.
13. **Varsayılan sipariş türü** alanında 'Satınalma siparişi'ni seçin.
14. **Kaydet**'e tıklayın.
15. Sayfayı kapatın. Varsayılan sipariş ayarları sayfasını kapatın.  

## <a name="add-an-item-to-a-coverage-group"></a>Kapsama grubuna bir madde ekleme
1. **Plan** bölümünü genişletin veya daraltın.
2. **Kapsam grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
3. Listede, oluşturduğunuz **Kapsam grubu**'nu bulun.
4. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="create-item-coverage-rules"></a>Madde kapsama kuralları oluşturma
1. **Eylem Bölmesi**'nde **Plan**'a tıklayın.
2. **Kapsam** altında, **Madde karşılama**'ya tıklayın.
3. **Yeni**'ye tıklayın.
4. **Genel** sekmesine tıklayın.
5. **Karşılama grubu** ayarlarını geçersiz kılma başlığı kutusunu işaretleyin.
6. **Kapsam zaman dilimi (gün)** alanına '60' girin. Gereklilik grubu kapsamındaki maddeler 90 gün önceden planlanmasına rağmen, bu madde 60 gün önceden planlanacaktır.  
7. **Negatif günler** alanına '2' girin.
8. **Pozitif günler** alanına '2' girin.
9. **Sağlama süresi** sekmesine tıklayın.
10. **Satınalma** başlığındaki onay kutusunu seçin.
11. **Satınalma zamanı** alanına '5' girin.
12. **Kaydet**'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]