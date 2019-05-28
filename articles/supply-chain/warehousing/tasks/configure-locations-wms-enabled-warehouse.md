---
title: WMS özellikli bir ambarda yerleşimleri yapılandırma
description: Bu kılavuz, yeni bir WMS etkin ambarın (gelişmiş ambar yönetimi süreçleri kullanan bir ambarın) konum kurulumunun nasıl yapılandırılacağını gösterir.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2be3c7cb33225041872e8b747ba28063f897dae9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563494"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>WMS özellikli bir ambarda yerleşimleri yapılandırma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu kılavuz, yeni bir WMS etkin ambarın (gelişmiş ambar yönetimi süreçleri kullanan bir ambarın) konum kurulumunun nasıl yapılandırılacağını gösterir. Bu işlem genellikle ambar yöneticisi tarafından yapılır. Bu kılavuzu, demo verileri şirketi USMF'yi veya kendi verilerinizi kullanarak yerine getirebilirsiniz. Bir önkoşul, yapılandırılmış en az bir tesis olmasıdır.


## <a name="create-a-new-warehouse"></a>Yeni bir ambar oluşturun
1. Ambarlara git.
2. Yeni'ye tıklayın.
3. Ambar alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Tesis alanına bir değer yazın.
6. Ambar bölümünü genişletin veya daraltın.
7. Ambar yönetimi süreçleri kullanımını Evet olarak ayarlayın.
    * Bu ayar, ambar çalışma ve mobil aygıtları kullanarak gelişmiş ambar işlemleri çalıştırmanızı sağlar.  
8. Sayfayı kapatın.

## <a name="define-a-location-format"></a>Konum biçimi tanımlayın.
1. Konum biçimlerine git.
    * Konum biçimleri, bir ambar içinde kullanılan farklı konum bölme pozisyonları için tutarlı ve benzersiz adlar oluşturmak için kullanılan isim sistemi biçimlerdir. Ayırıcıları, yerleşimin koridor numarası gibi bileşenlerini tanımlamayı kolaylaştırmak için bir konum biçimi parçası olarak kullanmak için yararlı olabilir. Bu örnekte, dört bileşenli bir isim oluşturacağız. Örneğin, bu koridor, dolap, raf ve bölme olabilir.  
2. Yeni'ye tıklayın.
3. Konum biçimi alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Segment tanımı alanına bir değer yazın.
    * Bu konum adının ilk bölmesinin neyi temsil ettiğini açıklar. Örneğin bu, koridor olabilir.  
6. Uzunluk alanına bir sayı girin.
    * Bu, bu yerleşim adı bölümünün kaç karakter olması gerektiğini belirler. Unutmayın, ayırıcılar da dahil olmak üzere, adın tüm bileşenlerinin toplam 10 karakterden uzun olamaz.  
7. Ayırıcı alanına bir değer yazın.
    * Bu, adın birinci ve ikinci bileşeni arasında hangi karakter veya simgenin kullanıldığını belirler.  
8. Yeni'ye tıklayın.
9. Segment tanımı alanına bir değer yazın.
10. Uzunluk alanına bir sayı girin.
11. Ayırıcı alanına bir değer yazın.
12. Yeni'yi tıklatın.
13. Segment tanımı alanına bir değer yazın.
14. Uzunluk alanına bir sayı girin.
15. Ayırıcı alanına bir değer yazın.
16. Yeni'yi tıklatın.
17. Segment tanımı alanına bir değer yazın.
18. Uzunluk alanına bir sayı girin.
19. Kaydet'e tıklayın.
20. Sayfayı kapatın.

## <a name="define-location-types"></a>Konum türlerini tanımlayın
1. Konum türlerine git.
    * Yerleşim tipleri farklı ambar yönetimi işlemlerini denetlemek için filtreleme seçenekleri olarak kullanılabilir. En düşük gereksinim olarak giden ambar yönetimi işlemi tanımlamak için hazırlama ve son sevkiyat yerleşim tiplerini oluşturmanız gerekir.  
2. Yeni'ye tıklayın.
3. Konum türü alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Sayfayı kapatın.

## <a name="define-location-profile"></a>Konum profilleri tanımlayın
1. Konum profillerine gidin.
    * Konum profillerinin tanımı çok önemlidir. Gruplandırılmış konum kapasitelerinin yanı sıra, hangi stokun depolanacağı ve nasıl depolandığına dair ilgili ilkeler buradan kontrol edilebilir. Yerleşim profilleri farklı ambar yönetimi işlemlerini denetlemek için filtreleme seçenekleri olarak kullanılabilir. En düşük gereksinim olarak ambar yönetimi işlemlerini etkinleştirmek için bir kullanıcı konumu profili oluşturmanız gerekir.  
2. Yeni'ye tıklayın.
3. Konum profili numarası alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Konum formatı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Konum türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, istenen kaydı bulun ve seçin.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. Karışık stok durumlarına izin ver onay kutusunu işaretleyin veya bu onay kutusunun işaretini kaldırın.
    * Bu konum profiline göre gruplandırılacak konumlarda karışık stok durum değerlerine izin vermek istiyorsanız bu seçeneği etkinleştirin.  
12. Toplu günler için atlatma kuralları onay kutusunu işaretleyin veya onay kutusundaki işareti kaldırın.
    * Bu kurala uymayan stok toplu işlerinin karıştırılmasına izin vermek istiyorsanız, stok toplu sona erme tarihlerinin kaç gün farklılık gösterebileceğine dair kuralı geçersiz kılmak için bu seçeneği etkinleştirin.  
13. Döngü sayımına izin ver onay kutusunu işaretleyin veya onay kutusundaki işareti kaldırın.
    * Bu konum profiline göre gruplandırılacak tüm konumlarda döngü sayımı işlemesine izin vermek istiyorsanız bu seçeneği etkinleştirin.  
14. Boyutlar bölümünü genişletin veya daraltın.
    * Boyutlar sekmesi, konumlardan her birinin içindeki yük kapasitesini hassas şekilde hesaplamak için parametreler ve yöntemler tanımlamanıza olanak sağlar.  
15. Sayfayı kapatın.

## <a name="enable-warehouse-management-parameters"></a>Ambar yönetim parametrelerini etkinleştirin
1. Ambar yönetim parametrelerine gidin.
    * Ambar işlerini işlemeye hazırlayabilmek için, kullanıcı konum profili, hazırlama konum türü ve son sevkiyat konum türü için parametreler ayarlamanız gerekir. Giden işlemler, tanımladığınız son sevkiyat konum türünde biter bitmez, ilgili giden hareketleri 'Çekildi' olarak güncelleştirilir.  
2. Konum profilleri bölümünü genişletin veya daraltın.
3. Kullanıcı konumu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Konum türleri bölümünü genişletin veya daraltın.
6. Depolama konum türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Son yükleme konumu türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. Sayfayı kapatın.

## <a name="define-warehouse-zone-groups"></a>Ambar bölge gruplarını tanımlayın.
1. Ambar bölge gruplarına gidin.
    * Ambar bölgeleri, farklı ambar yönetimi işlemlerini denetleme seçenekleri için filtre olarak kullanılabilir. Bir bölge tanımlamadan önce bölge grubu oluşturmanız gerekir.  
2. Yeni'ye tıklayın.
3. Bölge grubu numarası alanına bir değer yazın.
4. Bölge grubu adı alanına bir değer yazın.
5. Sayfayı kapatın.

## <a name="define-warehouse-zones"></a>Ambar bölgelerini tanımlayın
1. Gidilecek bölgeler.
2. Yeni'ye tıklayın.
3. Bölge numarası alanında bir değer girin.
4. Bölge adı alanına bir değer girin.
5. Bölge grubu numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Sayfayı kapatın.

## <a name="create-locations-using-the-location-setup-wizard"></a>Konum Kurulum Sihirbazı'nı kullanarak konumlar oluşturun
1. Konum kurulum sihirbazına gidin.
2. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Bölge numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Konum profil numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, istenen kaydı bulun ve seçin.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. Listede, seçili satırı işaretleyin.
12. Gönderen numarası alanına bir tarih girin.
    * Gönderen numarası ve Alıcı numarası alanları kaç adet konum oluşturulacağını belirler. Örneğin, gönderen numarası olarak 1 ve Alıcı numarası olarak 3 girerseniz, konum biçiminde tüm dört satır için 81 konum (3x3x3x3) oluşturulur.  
13. Alıcı numarası alanına bir sayı girin.
14. Listede, istenen kaydı bulun ve seçin.
15. Gönderen numarası alanına bir tarih girin.
16. Alıcı numarası alanına bir sayı girin.
17. Listede, istenen kaydı bulun ve seçin.
18. Gönderen numarası alanına bir tarih girin.
19. Alıcı numarası alanına bir sayı girin.
20. Listede, istenen kaydı bulun ve seçin.
21. Gönderen numarası alanına bir tarih girin.
22. Alıcı numarası alanına bir sayı girin.
23. Oluştur'a tıklayın.

## <a name="create-locations-manually"></a>Konumları el ile oluştur
1. Konumlara gidin.
    * Ambar içinde konumların el ile oluşturulması kolaylıkla yapılabilir. Konum adı ve konum profil kimliği zorunlu değerlerdir.  
2. Yeni'ye tıklayın.
3. Ambar alanına bir değer yazın.
4. Yerleşim alanına bir değer girin.
    * Burada yeni bir konum yarattığınızı ve bu yüzden mevcut bir tanesini kullanmak yerine, yeni ve benzersiz bir isim yazmanız gerektiğini unutmayın.  
5. Konum profili numarası alanına bir değer yazın.
6. Sayfayı kapatın.

## <a name="define-pack-size-categories"></a>Ambalaj boyutu kategorilerini tanımla
1. Paket boyutu kategorilerine gidin.
    * Ambalaj boyutu kategorileri, fiziki olarak benzer ambalaj boyutlarına öğeleri gruplandırmak için kullanılabilir. Bu örnekte, ambalaj boyutu kategorisi, ambarın belirli bir bölümündeki çekme konumlarının kapasitesini denetlemekte kullanılacak. Lütfen ambalaj boyut kategori kimliğinin stoklamanın bir parçası olarak kullanılabilmesi için serbest bırakılan ürünün varlığının stoklama limitlerinin işlenmesi için atanması gerektiğini unutmayın.  
2. Yeni'ye tıklayın.
3. Paket boyutu kategori numarası alanına bir değer yazın.
4. Paket boyutu kategori ismi alanına bir değer yazın.
5. Sayfayı kapatın.

## <a name="define-location-stocking-limits"></a>Konum stoklama sınırlarını tanımla
1. Konum stoklama sınırlarına gidin.
    * Konum stoklama limitleri, stok miktarını taşıyacak fiziksel kapasitenin mevcut olmadığı konumlara yerleştirilmesini talep edecek işlerin oluşturulmasının önüne geçmeye yardımcı olmaktadır.  
2. Yeni'ye tıklayın.
3. Ambar alanına bir değer yazın.
4. Konum profili numarası alanına bir değer yazın.
5. Paket boyutu kategori numarası alanına bir değer yazın.
6. Miktar alanına bir sayı girin.
7. Kaydet'e tıklayın.
8. Sayfayı kapatın.

## <a name="define-fixed-picking-locations"></a>Sabit Malzeme çekme konumlarını tanımla
1. Sabit yerleşimlere gidin.
    * Ürün veya ürün varyantı başına kullanılacak konumlarını tanımlayabilirsiniz. Aynı ambar içinde aynı ürün için birden fazla sabit konum oluşturmak mümkündür.  
2. Yeni'ye tıklayın.
3. Madde numarası alanına bir değer girin.
4. Ambar alanına bir değer yazın.
5. Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Sayfayı kapatın.

