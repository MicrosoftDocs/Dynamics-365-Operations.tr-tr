---
title: "Sipariş taahhüdü"
description: "Bu makalede sipariş taahhütleri hakkında bilgiler verilmiştir. Sipariş Taahhüdü müşterileriniz için güvenilir teslimat tarihleri taahhüt etmenize yardımcı olur ve böylece bu tarihleri karşılayabilmeniz için esneklik sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8aa0a58b03ee18e42ca7770ea3e22311c1ddba67
ms.lasthandoff: 03/31/2017


---

# <a name="order-promising"></a>Sipariş taahhüdü

Bu makalede sipariş taahhütleri hakkında bilgiler verilmiştir. Sipariş Taahhüdü müşterileriniz için güvenilir teslimat tarihleri taahhüt etmenize yardımcı olur ve böylece bu tarihleri karşılayabilmeniz için esneklik sağlar.

Sipariş taahhüdü erken sevk ve giriş tarihlerini hesaplar ve teslim tarihi kontrol yöntemi ve taşıma günlerini temel alır. Dört teslim tarihi kontrol yöntemi arasından seçim yapabilirsiniz:

-   **Satış sağlama süresi** – satış sağlama süresi satış siparişinin oluşturulmasından maddelerin sevk irsaliyesini arasındaki zamanı demektir. Teslim tarihi hesaplamasını bir varsayılan gün sayısına göre ve stok kullanılabilirliği, bilinen talep veya planlanan tedarik dikkate almaz.
-   **ATP (kullanılabilir taahhüt)** – KM olan bulunan ve müşteriye belirli bir tarihte taahhüt bir madde miktarı. KM hesaplaması kaydedilmemiş stok, sağlama süreleri, planlanan girişler ve sorunları içerir.
-   **KM + Çıkış marjı** sevkiyat tarihi karşılanabilir miktar KM tarihi ile maddenin çıkış marjının toplamına eşittir. Çıkış marjı, maddelerin sevkiyata hazırlanması için gereken süredir.
-   **CTP (Teslim edilebilir miktar) **– Kullanılabilirlik açılım ile hesaplanır.

## <a name="atp-calculations"></a>ATP hesaplamaları
ATP miktarı "toplu ATP ile bakma" yöntemi kullanılarak hesaplanır. Girişler arasında sorunlar toplamı en geç giriş (örneğin, bir önceki alış irsaliyesinden gelen ve bir miktar bir gereksinimi karşılamak üzere kullanılmalıdır) birden fazla olduğu durumlarda işleyebilir bu KM hesaplama yöntemi başlıca yararı olur. Verilecek kümülatif miktar almak için toplu miktarı aşıyor kadar tüm sorunları "toplu ATP ile bakma" hesaplama yöntemini içerir. Bu nedenle, KM hesaplama yöntemi, bir önceki dönemden bazı miktarların sonraki dönemde kullanılıp kullanılamayacağını değerlendirir.  

ATP miktarı, ilk dönemdeki kaydedilmemiş stok bakiyesinin miktarıdır. Genellikle, bir giriş planlanan her dönem için hesaplanır. Program ATP dönemini gün olarak hesaplar ve geçerli tarihi ATP miktarının ilk tarihi olarak hesaplar. İlk dönemde ATP, vadesi gelmiş ve geçmiş müşteri siparişlerinin çıkarıldığı eldeki stoku dahil eder.  

ATP aşağıdaki formülü kullanarak hesaplanır:  

KM KM önceki dönem + girişler için geçerli dönem – geçerli dönem için sorunlar – Net bir sorun için ne zaman alış irsaliyeleri ve Gelecek dönem, gelecekteki tüm dönemler için toplam aşan sorunlar toplamı kadar dönemine kadar ileride her dönem için = miktar ve Gelecek dönem dahil olmak üzere.  

Değerlendirilmesi gereken başka çıkış veya giriş kalmadığında, aşağıdaki tarihlerin ATP miktarı hesaplanan son ATP miktarıyla aynı olur.  

Bir madde için kullanılan tüm boyutlar ATP kontrolü gerçekleştirildiğinde verilmezse, çıkış ve girişlerde belirtilmeye devam ediyor olurlar. Bu durumda, ATP hesaplamasında kullanılan giriş ve çıkış satırlarının sayısını düşürmek için ATP hesaplamasında giriş ve çıkışların varolan boyutlara eklenmesi gerekir.  

Gösterilen KM miktarı her zaman büyük veya eşit 0 (sıfır) olur. Eğer hesaplama negatif bir ATP miktarı sonucu verirse (örneğin, daha önce taahhüt edilen miktar, mevcut miktarı geçerse), program otomatik olarak miktarı **0** olarak ayarlar.

### <a name="example"></a>Örnek

**KM geriye dönük talep zaman dilimi** alanı geri talep siparişleri veya gecikmeli stok çıkışlarını bakılması gereken geçmiş süresini denetler. **KM geriye dönük tedarik zaman dilimi** alanı geri tedarik siparişleri veya gecikmeli stok girişlerine bakılması gereken geçmiş süresini denetler. Örneğin, yalnızca yedi gün gecikmeli siparişler KM hesaplamasında dikkate alınacaksa, her iki alanın ayarlanması gerektiğini **7**.  

**KM Gecikmeli talep öteleme süresi** ve **KM Gecikmeli tedarik öteleme süresi** alanları, zaman gecikmeli talep veya tedarikin KM hesaplamasında ne zaman dikkate alınacağını belirler. Örneğin, gecikmeli talep ve tedarik bir sonraki gündeki KM hesaplamasında dikkate alınacaksa, her iki alan da **2** olarak ayarlanmalıdır. Değerin **2** olması, ATP hesaplamasında dikkate alınacak gecikmeli satınalma siparişindeki bir maddenin miktarının, bugünün tarihinden iki gün sonra mevcut olarak görüleceği anlamına gelir.  

Aşağıdaki örnek için **KM geriye tedarik zaman dilimi** ve **KM geriye dönük talep zaman dilimi** alanlarında **7** ve **KM Ertelenen talep öteleme süresinin** ve **KM Gecikmeli tedarik öteleme süresinin** alanlarında **1** girilir.  

Üç gün önce teslim alınması gereken 200 parça ürün için bir satınalma siparişi henüz alınmamıştır. Bu nedenle, dün gönderilmiş olması gereken bir satış siparişi satırı için aynı ürünün 75 parçası gönderilmemiştir.  

Bir müşteri arayıp aynı üründen 150 adet sipariş vermek istediğinde. Ürün kullanılabilirliğini doğruladığınızda, 10 gün sonra teslim edilecek 100 adet ürün için başka bir satınalma siparişi bulursunuz.  

Ürün için bir satış siparişi satırı oluşturun ve miktarı **150** olarak belirleyin.  

Teslimat tarihi kontrolü ATP yöntemi olduğu için, ATP verisi en erken olası sevk tarihini bulmak için hesaplanır. Ayarlarına bağlı olarak, geciken satınalma siparişi ve satış siparişi olarak kabul edilir ve geçerli tarih için elde edilen ATP miktarı 0 olmasına. Gecikmiş Sipariş alınması gerekirken, yarın, ATP miktarı fazla 0 hesaplanır (Bu durumda, 125 hesaplanır). Ancak, şimdi, ne zaman 100 parça için ek bir satınalma siparişi alınabilmesi için beklenen gelen 10 gün ATP miktarı 150'den fazla olur.  

Bu nedenle, sevk tarihi şu andan itibaren 10 gün olarak ayarlamak, ATP hesaplamaya dayalı. Bu nedenle, müşteri talep edilen miktarın şu andan itibaren 10 gün sonra teslim edilebileceğini söylersiniz.


