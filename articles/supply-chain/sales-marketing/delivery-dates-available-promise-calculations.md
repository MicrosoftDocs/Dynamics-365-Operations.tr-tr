---
title: Sipariş taahhüdü
description: Bu konuda sipariş taahhütleri hakkında bilgiler verilmiştir. Sipariş Taahhüdü müşterileriniz için güvenilir teslimat tarihleri taahhüt etmenize yardımcı olur ve böylece bu tarihleri karşılayabilmeniz için esneklik sağlar.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f7535ba28358fef21784956da38cd334a4aebe7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572613"
---
# <a name="order-promising"></a>Sipariş taahhüdü

[!include [banner](../includes/banner.md)]

Bu konuda sipariş taahhütleri hakkında bilgiler verilmiştir. Sipariş Taahhüdü müşterileriniz için güvenilir teslimat tarihleri taahhüt etmenize yardımcı olur ve böylece bu tarihleri karşılayabilmeniz için esneklik sağlar.

Sipariş taahhüdü erken sevk ve giriş tarihlerini hesaplar ve teslim tarihi kontrol yöntemi ve taşıma günlerini temel alır. Dört teslim tarihi kontrol yöntemi arasından seçim yapabilirsiniz:

-   **Satış sağlama süresi** – Satış sağlama süresi, satış siparişinin oluşturulmasından maddelerin sevk edilmesi arasındaki zaman anlamına gelir. Teslim tarihi hesaplaması, bir varsayılan gün sayısına dayanır ve stok kullanılabilirliğini, bilinen talebi veya planlanan tedariki dikkate almaz.
-   **KM (kullanılabilir taahhüt)** – KM mevcut bulunan ve müşteriye belirli bir tarihte taahhüt edilebilecek bir madde miktarıdır. KM hesaplaması kaydedilmemiş stok, sağlama süreleri, planlanan girişler ve sorunları içerir.
-   **KM + Çıkış marjı** sevkiyat tarihi karşılanabilir miktar KM tarihi ile maddenin çıkış marjının toplamına eşittir. Çıkış marjı, maddelerin sevkiyata hazırlanması için gereken süredir.
-   **CTP (Teslim edilebilir miktar)**– Kullanılabilirlik açılım ile hesaplanır.

> [!NOTE]
> Bir satış siparişi güncelleştirildiğinde sipariş taahhüdü bilgileri yalnızca, var olan sipariş taahhüdü tarihi yerine getirilmezse, aşağıdaki örneklerde görüldüğü gibi güncelleştirilir:
> 
> - **Örnek 1**: Geçerli sipariş taahhüdü tarihi 20 Temmuz'dur ancak artan miktar nedeniyle 25 Temmuz'dan önce teslim edilemiyor. Geçerli tarihe artık uyulmadığı için sipariş taahhüdü tetiklenir.
> -  **Örnek 2**: Geçerli sipariş taahhüdü tarihi 20 Temmuz'dur ancak azalan miktar nedeniyle 15 Temmuz'da teslim edilebilmektedir. Ancak, geçerli tarihin yerine getirilmesi gerektiğinden, sipariş taahhüdü tetiklenmez ve 20 Temmuz, sipariş taahhüdü tarihi olarak kalır.

## <a name="atp-calculations"></a>ATP hesaplamaları
Karşılanabilir miktar (ATP) “ileriye dönük toplam ATP” yöntemini kullanarak hesaplanır. Bu ATP hesaplama yönteminin temel avantajı, girişler arasındaki çıkışların toplamı son girişten fazla olduğunda, /(örneğin bir gereksinimi karşılamak için önceki bir girişten bir miktar kullanılması zorunlu olduğunda) örnekleri yönetebilmesidir. "İleriyi görebilmeli kümülatif ATP" hesaplama yöntemi, alınacak kümülatif miktar, verilecek kümülatif miktarı aşana kadarki tüm sorunları içerir. Bu nedenle, KM hesaplama yöntemi, bir önceki dönemden bazı miktarların sonraki dönemde kullanılıp kullanılamayacağını değerlendirir.  

ATP miktarı, ilk dönemdeki kaydedilmemiş stok bakiyesinin miktarıdır. Genellikle, bir giriş planlanan her dönem için hesaplanır. Program ATP dönemini gün olarak hesaplar ve geçerli tarihi ATP miktarının ilk tarihi olarak hesaplar. İlk dönemde ATP, vadesi gelmiş ve geçmiş müşteri siparişlerinin çıkarıldığı eldeki stoku dahil eder.  

ATP aşağıdaki formülü kullanarak hesaplanır:  

ATP = Önceki dönemin ATP'si + Geçerli dönemin girişleri – Geçerli dönemin çıkışları – Gelecek döneme kadar ve gelecek dönem dahil olmak üzere, tüm gelecek dönemlerdeki girişlerin toplamı, gelecek döneme kadar ve gelecek dönem dahil olmak üzere, çıkışların toplamını geçene kadar her gelecek dönem için net giriş miktarı.  

ATP hesaplamasının, herhangi bir miktar taahhüt edilebilir olduğunda sistemin bitiş tarihi ve ATP zaman diliminin ötesinde bilgiler içermediğine dikkat edin.

Değerlendirilmesi gereken başka çıkış veya giriş kalmadığında, aşağıdaki tarihlerin ATP miktarı hesaplanan son ATP miktarıyla aynı olur.  

Bir madde için kullanılan tüm boyutlar ATP kontrolü gerçekleştirildiğinde verilmezse, çıkış ve girişlerde belirtilmeye devam ediyor olurlar. Bu durumda, ATP hesaplamasında kullanılan giriş ve çıkış satırlarının sayısını düşürmek için ATP hesaplamasında giriş ve çıkışların varolan boyutlara eklenmesi gerekir.  

Gösterilen KM miktarı her zaman büyük veya eşit 0 (sıfır) olur. Eğer hesaplama negatif bir ATP miktarı sonucu verirse (örneğin, daha önce taahhüt edilen miktar, mevcut miktarı geçerse), miktar otomatik olarak 0 olarak ayarlanır.

### <a name="example"></a>Örnek

**KM geriye dönük talep zaman dilimi** alanı geri talep siparişleri veya gecikmeli stok çıkışlarını bakılması gereken geçmiş süresini denetler. **KM geriye dönük tedarik zaman dilimi** alanı geri tedarik siparişleri veya gecikmeli stok girişlerine bakılması gereken geçmiş süresini denetler. Örneğin, yalnızca yedi gün gecikmeli siparişler KM hesaplamasında dikkate alınacaksa, her iki alanın ayarlanması gerektiğini **7**.  

**KM Gecikmeli talep öteleme süresi** ve **KM Gecikmeli tedarik öteleme süresi** alanları, zaman gecikmeli talep veya tedarikin KM hesaplamasında ne zaman dikkate alınacağını belirler. Örneğin, gecikmeli talep ve tedarik bir sonraki gündeki KM hesaplamasında dikkate alınacaksa, her iki alan da **2** olarak ayarlanmalıdır. Değerin **2** olması, ATP hesaplamasında dikkate alınacak gecikmeli satınalma siparişindeki bir maddenin miktarının, bugünün tarihinden iki gün sonra mevcut olarak görüleceği anlamına gelir.  

Aşağıdaki örnek için **KM geriye tedarik zaman dilimi** ve **KM geriye dönük talep zaman dilimi** alanlarında **7** ve **KM Ertelenen talep öteleme süresinin** ve **KM Gecikmeli tedarik öteleme süresinin** alanlarında **1** girilir.  

Üç gün önce teslim alınması gereken 200 parça ürün için bir satınalma siparişi henüz alınmamıştır. Bu nedenle, dün gönderilmiş olması gereken bir satış siparişi satırı için aynı ürünün 75 parçası gönderilmemiştir.  

Bir müşteri arayıp aynı üründen 150 adet sipariş vermek istediğinde. Ürün kullanılabilirliğini doğruladığınızda, 10 gün sonra teslim edilecek 100 adet ürün için başka bir satınalma siparişi bulursunuz.  

Ürün için bir satış siparişi satırı oluşturun ve miktarı **150** olarak belirleyin.  

Teslimat tarihi kontrolü ATP yöntemi olduğu için, ATP verisi en erken olası sevk tarihini bulmak için hesaplanır. Ayarlara dayanarak, geciktirilmiş olan satınalma siparişi ve satış siparişi dikkate alınır ve sonucundaki ATP miktarı geçerli tarih için 0'dır. Yarın, gecikmiş satınalma siparişinin alınması beklendiğinde, ATP miktarı 0'dan fazla olarak hesaplanır (bu durumda, 125 olarak hesaplanır). Ancak, bundan 10 gün sonra, 100 parçalık ek satınalma siparişinin alınması beklendiğinde, ATP miktarı 150'den fazla olur.  

Bu nedenle, ATP hesaplamaya dayanarak, sevk tarihi şu andan itibaren 10 gün olarak ayarlanır. Bu nedenle, müşteri talep edilen miktarın şu andan itibaren 10 gün sonra teslim edilebileceğini söylersiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]