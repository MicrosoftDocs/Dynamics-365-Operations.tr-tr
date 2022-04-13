---
title: Maddeler için kapsama kurallarını tanımlama
description: Bu yordam, kapsam kurallarını oluşturmayı ve belirli bir madde için kapsama ayarlarını geçersiz kılmayı gösterir. Ayrıca varsayılan stok ayarlarının nasıl belirleneceğini de açıklar.
author: t-benebo
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bca0e1786adb08a7cd4795b49c974ab95183b1dd
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469336"
---
# <a name="define-coverage-rules-for-items"></a>Maddeler için kapsama kurallarını tanımlama

[!include [banner](../../includes/banner.md)]

Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam, kapsam kurallarını oluşturmayı ve belirli bir madde için kapsama ayarlarını geçersiz kılmayı gösterir. Ayrıca varsayılan stok ayarlarının nasıl belirleneceğini de açıklar.

## <a name="create-a-coverage-group"></a>Bir kapsam grubu oluşturma

Aşağıdakileri gerçekleştirerek bir kapsama grubu oluşturun:

1. **Gezinti bölmesi > Modüller > Master planlama > Kurulum > Kapsam grupları**'na gidin.
1. **Yeni**'yi seçin.
1. **Kapsam grubu** alanına bir değer yazın.
1. **Ad** alanına bir değer yazın.
1. **Takvim** alanına bir değer yazın. Nazım planlamanın bu gruptaki maddelerin stok yenilemesi önerilerini oluşturmak için kullandığı takvimi seçin.  
1. **Kapsam kodu** alanında bir seçenek seçin. Bu yordam için 'Gereksinim'i seçin.  
1. **Kapsam zaman dilimi (gün) alanı**'na '90' girin. Bu gruptaki maddeler için, master planlama gelecek en fazla 90 gün için stok yenileme önerileri oluşturur.  
1. **Negatif günler** alanına '1' girin.
1. **Pozitif günler** alanına '1' girin.
1. **Diğer** bölümünü genişletin veya daraltın.
1. **Gün sayısı olarak emniyet marjları** bölümünde, **Gereksinim tarihine eklenen giriş marjı** alanına '1' girin. Örneğin giriş marjı bir gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir giriş için bir satın alma siparişi satırı planlanırsa, nazım planlama ayarlanan giriş tarihini 16 mayıs olarak hesaplar.
1. **Gereksinim tarihinden kesilen çıkış marjı** alanına '1' girin. Örneğin emniyet marjı 1 gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir teslimat için bir satış siparişi satırı planlanırsa, nazım planlama ayarlanan teslim tarihini 14 mayıs olarak hesaplar.  
1. **Madde sağlama süresine eklenen sipariş yenileme sınırı** alanına '1' girin.
1. **Kaydet**'i seçin.

## <a name="create-a-new-product"></a>Yeni bir ürün oluştur

Aşağıdakileri gerçekleştirerek yeni bir ürün oluşturun:

1. **Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.
1. **Yeni**'yi seçin.
1. **Ürün numarası** alanında bir değer girin.
1. **Ürün adı** alanına bir değer yazın.
1. **Madde modeli grubu** alanında, aramayı açmak için açılır menü düğmesini seçin.
1. Listede, istenen kaydı bulun ve seçin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **Madde grubu** alanında, aramayı açmak için açılır menü düğmesini seçin.
1. Listede, istenen kaydı bulun ve seçin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **Depolama boyutu grubu**'nda, aramayı açmak için açılır menü düğmesini seçin.
1. Listede, istenen kaydı bulun ve seçin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **İzleme boyutu grubu** alanında, aramayı açmak için açılır menü düğmesini seçin.
1. Listede, istenen kaydı bulun ve seçin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **Tamam**'ı seçin.

## <a name="set-up-default-order-settings"></a>Varsayılan sipariş ayarlarını yapma

Aşağıdakileri gerçekleştirerek varsayılan sipariş ayarlarını yapın:

1. **Eylem Bölmesi**'nde, **Plan**'ı seçin.
1. **Sipariş ayarları**'nın altında, **Varsayılan sipariş ayarları**'nı seçin.
1. **Satınalma siparişi**'nin altında, **Varsayılan site** alanında satınalma siparişleri oluşturulurken varsayılan olarak kullanılan tesisi yazın.
1. **Varsayılan ambar** alanına, maddenin depolandığı sahayı yazın.
1. **Stok** bölümünü genişletin veya daraltın.
1. **Çoklu** alanına '10' yazın.
1. **Minimum sipariş miktarı** alanına '10' yazın.
1. **Maksimum sipariş miktarı** alanına '100' yazın.
1. **Standart sipariş miktarı** alanına '10' yazın.
1. **Satınalma sağlama süresi** alanına bir sayı girin.
1. **Çalışma günleri** onay kutusunu seçin veya temizleyin.
1. **Kaydet**'i seçin.
1. **Varsayılan sipariş türü** alanında 'Satınalma siparişi'ni seçin.
1. **Kaydet**'i seçin.
1. Sayfayı kapatın. Varsayılan sipariş ayarları sayfasını kapatın.  

## <a name="add-an-item-to-a-coverage-group"></a>Kapsama grubuna bir madde ekleme

Aşağıdakileri yaparak bir kapsama grubuna bir madde ekleyin:

1. **Plan** bölümünü genişletin veya daraltın.
1. **Kapsama grubu** alanında, aramayı açmak için açılır menü düğmesini seçin.
1. Listede, oluşturduğunuz **Kapsam grubu**'nu bulun.
1. Listeden, seçilen satırdaki bağlantıyı seçin.

## <a name="create-item-coverage-rules"></a>Madde kapsama kuralları oluşturma

Aşağıdakileri gerçekleştirerek madde kapsama kuralları oluşturun:

1. **Eylem Bölmesi**'nde, **Plan**'ı seçin.
1. **Kapsam** altında, **Madde kapsamı**'nı seçin.
1. **Yeni**'yi seçin.
1. **Genel** sekmesini seçin.
1. **Karşılama grubu** ayarlarını geçersiz kılma başlığı kutusunu işaretleyin.
1. **Kapsam zaman dilimi (gün)** alanına '60' girin. Gereklilik grubu kapsamındaki maddeler 90 gün önceden planlanmasına rağmen, bu madde 60 gün önceden planlanacaktır.  
1. **Negatif günler** alanına '2' girin.
1. **Pozitif günler** alanına '2' girin.
1. **Sağlama süresi** sekmesini seçin.
1. **Satınalma** başlığındaki onay kutusunu seçin.
1. **Satınalma zamanı** alanına '5' girin.
1. **Kaydet**'i seçin.

> [!NOTE]
> Üretilen maddeler için, madde için rota yoksa, **Üretim sağlama süresi** kullanılır. Maddeyle ilgili etkin bir rota ilişkilendirilmişse, master planlama siparişin rota sürelerine ve kapasitesine (varsa) göre siparişi çizelge, ve tarihleri hesaplayacaktır.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
