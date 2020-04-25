---
title: Saat ve işe devam kaydına genel bakış
description: Zaman kayıt çalışanları, örneğin giriş saati, çıkış saati, dolaylı faaliyetlerin kaydı ve devamsızlık kaydı gibi farklı türlerde zaman kayıtları girebilirler. Bu konuda kayıtlar, bunların hesaplanması, onaylanması ve zaman çizelgelerinin onaylanması sürecine yapı ve otomatik onay eklenmesi için iş akışının kullanımı hakkında bilgiler verilmiştir.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 02d2baebfb7309156400a178591605619fe59053
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210300"
---
# <a name="time-and-attendance-registration-overview"></a>Saat ve işe devam kaydına genel bakış

[!include [banner](../includes/banner.md)]

Zaman kayıt çalışanları, örneğin giriş saati, çıkış saati, dolaylı faaliyetlerin kaydı ve devamsızlık kaydı gibi farklı türlerde zaman kayıtları girebilirler. Bu konuda kayıtlar, bunların hesaplanması, onaylanması ve zaman çizelgelerinin onaylanması sürecine yapı ve otomatik onay eklenmesi için iş akışının kullanımı hakkında bilgiler verilmiştir. 

<a name="registrations"></a>Kayıtlar
-------------

Saat ve işe devam ayarını kullanan şirketlerde, çalışanların işe devam ettikleri sürenin yanı sıra işte harcadıkları süreleri de kaydetmeleri gerekir. Bazı şirketlerde çalışanların giriş ve çıkış saatlerini kaydettirmeleri gerekir. Diğer şirketlerde, çalışanların aldıkları molaların yanı sıra gerçekleştirdikleri fiili aktivitelerde harcadıkları zamanı da kaydettirmeleri gerekebilir. Saat ve işe devam ayarı için beklenen kullanıcılar şöyledir:
-   Örneğin günlük, haftalık veya iki haftada bir olacak şekilde düzenli aralıklarla saat ve işe devam kaydı yaptırması gereken çalışanlar.
-   Başka işlemler için çalışan kayıtlarını hesaplayan, onaylayan ve transferini gerçekleştiren denetçiler, yöneticileri ve bordro görevlileri.

| **Not**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saat ve işe devam ayarı ile birlikte İmalat yürütme'yi çalıştırıyorsanız projedeki tüm kayıtlar, proje faaliyetleri, dolaylı faaliyetler, devamsızlık kodları ve fazla mesai ile esnek çalışma saatleri kaydedilir ve bu kayıtlar her iki modülde de bordro hesaplanırken kullanılır. |

## <a name="time-registrations-workers"></a> Zaman kayıt çalışanları
Saat ve devamsızlık kaydı yapabilmeleri için çalışanların istihdam edildikleri şirkette zaman kayıt çalışanı olarak ayarlanması gerekir.

Ayarlamanın ardından çalışanlar farklı türde kayıtlar girebilir.

-   İşe gelirken veya çıkarken giriş-çıkış saati.
-   İmalat işlerinde zaman ve malzeme tüketimi.
-   Makine bir kaynak olarak tanımlanmışsa atölyede makine başında geçirilen süre.

| **Not**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Çalışan üretim işine başladığında bir asistan olarak çalışmayı seçerse, atölyede belirli bir makinede yapılan zaman kayıtlarına otomatik olarak atanabilir. |

-   Projelerde ve proje faaliyetlerinde zaman kayıtları.
-   Proje ücretlerini ve malzeme tüketimini ilgili proje ücret günlükleri ve proje ürün günlükleri üzerinde kaydetme.
-   Planlı devamsızlık.
-   İşe geç kalma veya planlanandan daha erken bırakma durumundaki devamsızlık.
-   El ile kaydedilen ya da sistem tarafından otomatik hesaplanan molalar.
-   Bir çalışanın iş günü boyunca uğraşacağı üretim dışı faaliyetler olan dolaylı faaliyetler. Bu faaliyetlere örnekler arasında toplantılar veya çalışma alanının temizlenmesi bulunur.
-   Ek çalışma saatleri, esnek saatler veya fazla mesai olarak kaydedilebilen fazla mesai.

## <a name="adding-clock-out-registrations"></a>Çıkış saati kayıtları ekleme
İş gününün sonunda çalışan çıkış saati kaydını yapmayı unutursa, eksik kayıtlar toplu bir işlem çalıştırılarak eklenebilir. Sistem, çalışanın ilişkili profiline göre giriş ve çıkış saatlerini karşılaştırır ve profilin iş bitiş zamanına uyacak şekilde eksik çıkış saati kaydını otomatik olarak ekler. Hem giriş hem de çıkış saati kayıtları, kayıtların bir sonraki hesaplanması ve bordroya aktarılmadan önce onaylanması için çok önemlidir.

## <a name="calculating-registrations"></a>Kayıtları hesaplama
Bir kayıt çalışanı, genellikle belirli bir ekip vardiya veya çalışma grubuyla ilişkili bir hesaplama grubuna atanır. Ekip yöneticisi ya da denetmen genellikle çalışanların yaptığı kayıtları doğrular ve bu nedenle hesaplamanın günlük bazda ilgili hesaplama grupları için çalıştırılmasından da sorumlu kişidir. Hesaplama işleminin bir parçası olarak ekip yöneticisinin veya gözetmenin yetkileri şöyledir:
-   Hatalı kayıtların düzeltilmesi. Örneğin, geçiş kodlarını değiştirmek ve üretim işleri hakkında geribildirim ayarlamak.
-   Eksik kayıtları ekleme. Örneğin, çıkış saati kayıtları oluşturmak ve devamsızlık hareketleri oluşturmak.
-   Hatalı kayıtları silme.

Kaydedilen sürenin çalışanın kayıtlarının hesaplanmasından önceki zaman profiliyle eşleşmesi gerektiğinden, standart zaman profili için istisnai durumu olan herhangi bir çalışanın çalışma zamanı profilini geçersiz kılmanız gerekir. Çalışan profilinin gündüz vardiyasında olduğu ve çalışanın fazla mesai ücreti olmadan gece vardiyasında çalışmayı kabul ettiği durumda, ekip yöneticisinin ya da bir denetmenin çalışma süresini fazla mesai olarak değil standart gece ücreti üzerinden hesaplayabilmek için varsayılan çalışan profilini geçersiz kılması gerekir. Bir devamsızlık kaydı eksikse, hesaplamada yine bir hata görünür. Hesaplamanın tamamlanması için eksik kaydın eklenmesi gerekir.

## <a name="approving-registrations"></a>Kayıtları onaylama
Bir hesaplama grubunu bir defa bir zaman kayıt çalışanına atadığınız için ona bir onay grubu da atamanız gerekir. Genellikle bir grup bir ekibe, vardiyaya veya çalışma grubuna özgüdür. Doğru hesaplanan zaman kayıtlarını, ödeme kalemlerinin oluşturulabilmesi ve ardından bir bordro sistemine transferinin gerçekleştirilebilmesi için onaylamanız gerekir; bunun anlamı hatasız bir hesaplama yapılmasıdır. Bordro yöneticisi genellikle kayıtların onayını yapar ve onay öncesindeki yetkileri şöyledir:
-   Tek tek çalışanlar için ödeme sözleşmelerini geçersiz kılma.
-   El ile prim ekleme.
-   Devamsızlık kaydıyla ilgili ek bilgiler girme.

| **Not**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Belirli çalışanlar için fazla mesai hesaplanmışsa, fazla mesai gün içindeki belirli işlere dağıtılabilir. Bu işlem, iş maliyeti çalışan ödemesine göre hesaplanıyorsa faydalıdır. |

## <a name="approving-registrations-using-workflow"></a> İş akışını kullanarak kayıtları onaylama
İş akışı kurallarıyla uyumlu kayıtları otomatik olarak onaylayan bir iş akışı onay işlemini yalnızca sapmaları el ile işlenecek şekilde bırakarak ayarlayabilirsiniz. İş akışı onayı etkinleştirilirse, ekip yöneticisi ya da denetmen onay için hesaplanmış kayıtları gönderir. İş akışı işlemi uygun onayları ve görevleri oluşturur ve sonra bunları için iş akışı içinde tanımlanan doğru kullanıcılara ve rollere atar. Saat ve işe devam için iki iş akışı onayı vardır.

| İş Akışı                                  | Amaç                                                                                                   | Kayıt türü                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saat ve işe devam durumu toplam gün sayısı            | İş akışı, örneğin gün için beklenen çalışma saati sayısına göre kayıtları doğrular. |                                                                                                                                                                                                                                                       |
| Saat ve işe devam durumu günlük kaydı. | İş akışı, kayıt tarihi için her bir kayıt türünü doğrular.                           | Saat ve işe devam • Giriş • Çıkış • Devamsızlık • Mola • Geçiş kodu • Proje • Proje faaliyeti • Dolaylı faaliyet Üretim işleri • Operasyon öncesi kuyruk • Ayarlar • İşlem • Çakışma • Taşıma • Operasyon sonrası kuyruk • Asistanı başlat • Asistanı durdur |



## <a name="transferring-approved-registrations"></a>Onaylanan kayıtları transfer etme
Kayıtların onaylanmasının ardından bunları periyodik bir bordro işine transfer edebilirsiniz. Transfer edilen bir kayıt bir faaliyet veya bir üretim emri veya proje gibi ilgili iş için deftere nakledilir. Bordro hareketleri kayıtlara dayalı her çalışan için oluşturulur.  

## <a name="reversing-transferred-registrations"></a>Transfer edilen bir kaydı ters kaydetme
Hareketleri ters kaydetme görevi (onları geri alma işlemi) bordro döneminin ödeme transferinin çalıştırılma zamanına kadar yapılabilir. Bu, bordro verilerinin harici bir dosyaya transfer edilmesi demektir. Ters kaydedildiğinde, tüm kayıtlar geri çekilir ve üretim emirleri veya projeler için deftere nakledilen hareketler dengelenir.

| **Not**                                                 |
|----------------------------------------------------------|
| Harici dosya bir bordro sistemine aktarılabilir. |

## <a name="registrations-in-electronic-timecards"></a>Elektronik zaman kartlarında kayıtlar
Anında geribildirim gerektirmeyen iş görevleri olan ancak proje faaliyetleri üzerinde çalışan çalışanlar, üretim işlerinde olduğu gibi elektronik zaman kartından yararlanabilir. Elektronik zaman kartları kayıtların istendiği zaman girilmesi için esneklik sunar ve günlük, haftalık ya da çalışan ofis dışına çıktıktan sonra tekrar geri döndüğünde iş zamanlaması oluşturmanın en iyi yoludur. Elektronik zaman kartlarını veya bu çalışanları kullanmak için çalışan ayrıntılarında Zaman kartı kullan seçeneğini belirlemeniz gerekir. Elektronik zaman kartları çalışanın şunları kaydettirmesini sağlar:

-   Tarih
-   Kayıt türü
-   Proje, dolaylı faaliyet veya üretim emri gibi iş referansı
-   İş tanımlayıcısı
-   Zaman tüketimi
-   Proje ücretleri
-   Proje kalemleri




