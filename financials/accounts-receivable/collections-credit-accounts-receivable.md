---
title: "Alacak hesaplarında alacak ve tahsilatlar"
description: "Alacak hesapları tahsilat bilgileri, Microsoft Dynamics 365 for Operations Collections sayfası kullanılarak bir merkezi görünümde yönetilir. Kredi ve tahsilat yöneticileri bu merkezi görünümü kullanarak tahsilatları yönetebilir. Tahsilat temsilcileri, tahsilat işlemine önceden tanımlanmış tahsilat kriterlerini kullanarak oluşturulmuş müşteri listelerinden veya Müşteriler sayfasından başlayabilir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 050c9f3ba539906bdbfbc5b4e4ee4af336236b73
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="credit-and-collections-in-accounts-receivable"></a>Alacak hesaplarında alacak ve tahsilatlar

[!include[banner](../includes/banner.md)]


Alacak hesapları tahsilat bilgileri, Microsoft Dynamics 365 for Operations Collections sayfası kullanılarak bir merkezi görünümde yönetilir. Kredi ve tahsilat yöneticileri bu merkezi görünümü kullanarak tahsilatları yönetebilir. Tahsilat temsilcileri, tahsilat işlemine önceden tanımlanmış tahsilat kriterlerini kullanarak oluşturulmuş müşteri listelerinden veya Müşteriler sayfasından başlayabilir.

Tahsilatları ayarlamaya veya bunlar üzerinde çalışmaya başlamadan önce, aşağıdaki kavramları anlamanız gerekir:
-   Müşteri yaşlandırma anlık görüntüsü belirli bir zamandaki yaşlandırılmış bakiye bilgilerini içerir
-   Tahsilat müşteri havuzları işinizi organize etmenize yardımcı olur
-   Tahsilat temsilcilerinin kendi müşteri havuzları olabilir
-   Liste sayfaları tahsilat müşterilerini, etkinlikleri ve servis taleplerini düzenler
-   Bir müşteriyle ilgili tüm tahsilat bilgileri tek bir sayfada bulunur ve bu sayfadan eylem gerçekleştirebilirsiniz
-   Fazi ve ücretlerden feragat etme, bunları eski durumuna getirme veya tersine çevirme işlemi tek bir adımda yapılabilir
-   Silme hareketleri oluşturma tek bir adımda gerçekleştirilebilir
-   Yetersiz fon (NSF) ödemeleri işlemleri bir adımda yapılabilir

Aşağıdaki bölümlerde her bir kavram tanımlanmıştır.

## <a name="customer-aging-snapshots"></a>Müşteri yaşlandırma anlık görüntüsü 
Bir yaşlandırma anlık görüntüsü, bir müşterinin belirli bir zamandaki hesaplanan yaşlandırılmış bakiyesini içerir. Bu bilgi, Yaşlandırılmış bakiyeler listesi sayfası ve Tahsilatlar sayfasında görüntülenir. Tahsilatlar listesi sayfalarında bilgileri görebilmeniz için yaşlandırma anlık görüntüsünün oluşturulmuş olması gerekir. 

Her müşteri için, yaşlandırma anlık görüntüsü bir yaşlandırma anlık görüntüsü başlığı ve yaşlandırma dönemi tanımındaki her yaşlandırma dönemine karşılık gelen ayrıntılı kayıtları içerir. 

Yaşlandırma anlık görüntüsü başlığı vadesi gelen toplam tutarı, alacak limitini, sevk irsaliyesi tutarını, satış siparişi tutarını, müşteri hesabındaki ihtilaflı hareketlerin toplam tutarını içerir. Müşteriye ilişkin tüm hareketler bu tutarlar hesaplanırken dahil edilir. Vadesi gelen toplam tutar, alacak limiti, sevk irsaliyesi tutar ve satış siparişi tutarı Tahsilatlar sayfasındaki Alacak bilgisi Bilgi Kutusunda gösterilir. 

Yaşlandırma dönemi tanımındaki her yaşlandırma dönemi için bir yaşlandırma anlık görüntüsü ayrıntı kaydı oluşturulur. Her yaşlandırma anlık görüntüsü ayrıntı kaydı yaşlandırma dönemi kodunu ve yaşlandırma dönemindeki tarihlerle birlikte hareketlerin toplam tutarını içerir. Hareketler bir yaşlandırma dönemine atanabilir (vadesi 30 gün geçmiş gibi). Tarih, yaşlandırm anlık görüntüsünü oluştururken belirttiğiniz Yaşlandırma tarihiyle ilişkilidir. Bu bilgi, Yaşlandırılmış bakiyeler liste sayfasında ve Tahsilatlar sayfasındaki Yaşlandırılmış bakiyeler Bilgi Kutusunda görüntülenir.

## <a name="collections-customer-pools"></a> Tahsilat müşteri havuzları 
Müşteri havuzları, tahsilatlar veya yaşlandırma işlemleri için görüntülenebilen veya yönetilebilen müşteri kayıtları grubunu tanımlayan sorgulardır. Yaşlandırılmış bakiyeler, Tahsilat etkinlikleri ve Tahsilat servis talepleri liste sayfalarındaki bilgileri filtrelemek için kullanıcı havuzlarını kullanın. Yaşlandırma anlık görüntüleri oluşturulduğunda eklenecek müşteri hesaplarını filtrelemek için de müşteri havuzlarını kullanabilirsiniz.

## <a name="collections-agents"></a>Tahsilat temsilcisi
Varsayılan olarak, Microsoft Dynamics 365 for Operations kullanıcıları tahsilat listesi sayfalarındaki tüm müşteri bilgilerini görebilirler. Tahsilat listesi sayfalarındaki ve Tahsilatlar sayfasındaki bilgileri filtrelemek için kullanılabilecek müşteri havuzlarını belirlemek için tahsilat temsilcisi kayıtlarını kullanabilirsiniz. 

Tahsilat temsilcisi, ödemelerin zamanında tahsil edildiğinden emin olmak için müşterilerle birlikte çalışan kişidir. Microsoft Dynamics 365 for Operations'ta tahsilat temsilcileri, Kullanıcı ayarı sayfasında kullanıcılara atanan çalışanlardır.

## <a name="collections-list-pages"></a> Tahsilatlar listesi sayfaları 
Aşağıdaki liste sayfaları tahsilat bilgilerini düzenlemenize yardımcı olur.
-   Yaşlandırılmış bakiyeler – Liste sayfasındaki sütunlar yaşlandırma dönemi için müşteri bakiyelerini ve yaşlandırılan tutarları gösterir. Bu bilgiler bir yaşlandırma anlık görüntüsünde depolanır. Yaşlandırma dönemleri, kullanılan yaşlandırma dönemi tanımı tarafından belirlenir. Yaşlandırma dönemi tanımı, havuz sorgusu için belirtildiyse, müşteri havuzundan alınır. Müşteri havuzunda bir yaşlandırma dönemi tanımı yoksa, Alacak hesapları parametreleri sayfasında belirtilmiş varsayılan yaşlandırma dönemi tanımı kullanılır. Hiçbir varsayılan yaşlandırma dönemi tanımı belirtilmemişse, Yaşlandırma dönemi tanımları sayfasındaki ilk yaşlandırma dönemi tanımı kullanılır.
-   Tahsilat etkinlikleri - Liste sayfasındaki sütunlar tahsilat etkinlikleri olarak tanımlanan etkinlikleri görüntüler. Bu etkinlikler Tahsilatlar sayfası kullanılarak oluşturulur. Tahsilatlarla ilgili olarak yaptığınız işleri izlemek için bu etkinlikleri kullanın.
-   Tahsilat servis talepleri – Liste sayfasındaki sütunlar, Tahsilatlar için servis talebi türü bulunan bir servis talebi kategorisine sahip durumlarla ilgili bilgileri görüntüler.

> [!NOTE]
> Bu liste sayfalarında bilgileri görebilmeniz için yaşlandırma anlık görüntüsünün oluşturulmuş olması gerekir. Bilgiler, yalnızca yaşlandırma anlık görüntüsü oluşturulan müşteriler için görüntülenebilir. Liste sayfasında gösterilen kayıtlar aşağıdaki şekilde de filtrelenebilir:
<li>Varsayılan olarak, Microsoft Dynamics 365 for Operations kullanıcısı bir yaşlandırma anlık görüntüsü bulunan tüm müşterilere erişebilir.</li>
<li>Müşteri havuzları varsa, tahsilat liste sayfalarındaki bilgilerin filtreleneceği havuzları kullanmak için kullanıcının tahsilat temsilcisi olarak ayarlanması gerekir. Bilgiler, seçili müşteri havuzuna dahil olan müşterilerle sınırlıdır.</li>
<li>Bir kullanıcı tahsilat temsilcisi olarak ayarlanırsa, yalnızca bu tahsilat temsilcisi için seçilen havuzlar liste sayfasında kullanılabilir. Tahsilat temsilcisi için Tahsilatlar sayfasında Temsilcinin tüm müşteri havuzlarını görmesine izin ver seçeneği seçilirse, söz konusu temsilci tüm havuzları görebilir.</li>


## <a name="collections-page"></a> Tahsilatlar sayfası
Bir müşteriye ilişkin tahsilat bilgileri, etkinlikleri ve servis taleplerini görüntülemek, yönetmek ve işlem yapmak için Tahsilatlar sayfasını kullanın. 

Üstteki bölme seçili müşteriyle ilgili vakaları görüntüler. Orta pano, müşteri için hareketleri görüntüler. Alt bölmede müşteriyle ilgili etkinlikleri görüntüler. Bir veya daha fazla hareket ve etkinlikle ilgili tahsilat bilgilerini izlemek için tahsilat servis talepleri oluşturabilirsiniz. Üst ve alt bölmedeki bilgiler servis talebine göre filtrelenebilir. 

Bilgi kutuları seçili müşteriyle ilgili yaşlandırılmış bakiyeleri ve alacak limiti bilgilerini görüntüler. Bu bilgiler yaşlandırma anlık görüntüsünde depolanır. Gerekirse, yaşlandırma anlık görüntüsünü geçerli bilgilerle güncelleştirebilirsiniz. 

Eylem Bölmesi seçili müşteri, servis talebi, hareket veya etkinlik için ilgili bilgileri görüntüleyen düğmeler içerir. Ayrıca, bir hareketin tahsilat durumunu değiştirme, e-posta sağlayıcınızla tümleştirme yaparak e-posta iletişimleri gönderme, müşterilere para iadesi yapma, NFS ödemelerini işleme koyma ve tahsil edilemeyen bakiyeleri silme gibi ortak işlemleri de gerçekleştirebilirsiniz.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Faiz ve ücretlerden feragat etme, bunları eski durumuna getirme veya tersine çevirme 
Vade farkı dekontlarından veya vade farkı notlarının bir parçası olan ücretler ve hareket faizinden feragat edebilir, bunları eski durumuna getirebilir veya tersine çevirebilirsiniz. Bu işlemleri Tüm müşteriler liste sayfasındaki Eylem Bölmesinin Tahsilat sekmesinden Vade farkı dekontu, Hareket faizi veya Ücret'e tıklayarak yapabilirsiniz. 

Bu ayarlamalar yalnızca vade farkı dekontlarını ve bunların içerdiği faiz ile ücretleri etkiler. Bir müşterinin borçlu olduğu tüm giderleri silmek için "Bir adımda silme hareketleri oluştur" bölümünde bulunan adımları izleyin.

## <a name="create-writeoff-transactions"></a>Silme hareketi oluşturma
Ödenmemiş borçları Tahsilatlar formundaki ve Yaşlandırılmış bakiyeler, Müşteriler ve Açık müşteri faturaları liste sayfalarındaki Silme seçeneğine tıklayarak silebilirsiniz. 

Bir müşteri için hareketleri sildiğinizde, müşteriye ilişkin tüm hareketler otomatik olarak kapatma için işaretlenir. Silinen tutar, işaretlenen hareketlerin net tutarına bağlıdır. Silme hareketi genel günlükte oluşturulur ve en fazla üç türde günlük satırı içerebilir.

-   İlk günlük satırı türü müşteri silme girişini içerir. İşaretli hareketler birden fazla para birimi kodu, boyut ve nakil profili birleşimi içeriyorsa, her birleşim için ayrı bir günlük satırı oluşturulur.
-   İkinci günlük satırı türü genel muhasebe silme girişini içerir. İşaretli hareketler birden fazla para birimi kodu, boyut ve nakil profili birleşimi içeriyorsa, her birleşim için ayrı bir günlük satırı oluşturulur.
-   Üçüncü günlük satırı türü satış vergileri için genel muhasebe silme bilgileri içerir. Bu günlük satırı, yalnızca Alacak hesapları parametreleri sayfasında Ayrı satış vergisi seçimi işaretlendiğinde oluşturulur. İşaretlenen hareketler birden fazla satış vergisi borç hesabı, boyut ve satış vergisi kodu birleşimi içeriyorsa, her birleşim için ayrı bir günlük satırı oluşturulur.

Silme hareketi hareket para birimi cinsinden oluşturulur.
Yetersiz fon (NSF) ödemelerini işleme  
--------------------------------------------

Tahsilatlar sayfasındaki NSF ödemesine tıklayarak NSF ödemelerini işleyebilirsiniz. Bu düğmeye tıkladığınızda, ödeme iptal edilir. Müşteriye NSF ücreti uygulanırsa, ödeme günlüğünde gider hareketi oluşturulur. Ücret tutarı, otomatik giderler ayarlarını temel alır. NSF ödemeleri için uygulanan otomatik giderler, etkilenen banka hesabı için Banka hesapları sayfasında seçilen gider grubu tarafından belirlenir.





