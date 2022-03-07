---
title: Sevkiyat otomatik güncelleştirmeleri
description: Bu konu, sevkiyatlar için otomatik güncelleştirme sağlayan işleve genel bir bakış sağlar.
author: Mirzaab
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3402a4c90299cf52e489e85ed55aff9762796545
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580108"
---
# <a name="shipment-auto-updates"></a>Sevkiyat otomatik güncelleştirmeleri

[!include [banner](../includes/banner.md)]

Sevkiyat otomatik güncelleştirme işlevi, yük bir ambara serbest bırakıldıktan sonra, bir sevkiyatla ilişkilendirilmiş yükleme satırındaki miktarları (artış ve azalmalar) otomatik olarak güncelleştirir. Bu işlev, sevkiyattaki yük satırı veya yük dalgada işlenene kadar etkin kalır. Kullanıldığında, sipariş güncelleştirmeleri ambar işi oluşturuluncaya kadar el ile müdahale gerektirmeden ambara otomatik olarak akabilir.

Sevkiyatı otomatik güncelleştirme işlevi kullanılmazsa, ambar işi oluşturuluncaya kadar yalnızca miktardaki azalma ambara otomatik olarak akabilir. Kullanıcılar satırları el ile güncelleştirmeli veya silmeli ve sipariş miktarları artarsa veya yeni sipariş satırları eklenirse satırları yeniden serbest bırakmalıdır. Sevkiyatı otomatik güncelleştirme işlevini kullanarak, işletmeler ilgili sevkiyatların ve yüklerin sipariş satırı güncelleştirmelerini yansıtmayacağı endişesi taşımadan ambara güncelleştirmeleri sorunsuz şekilde sağlayabilir.

Sevkiyatı otomatik güncelleştirme işlevi hem satış siparişi satırları, hem de transfer emri satırları için geçerlidir ve belirli bir ambar için açıktır. Bu nedenle, şirketler gerektiğinde ambarlarda farklı sevkiyatı otomatik güncelleştirme ilkeleri uygulayabilir. Varsayılan olarak, miktar azalmaları için sevkiyatı otomatik güncelleştirme ilkesi ambar yönetimi işlemlerini kullanan tüm ambarlar için uygulanır. Bu varsayılan ilke ayarı kullanıldığında, ambar işi oluşturuluncaya kadar yalnızca miktar azalmaları otomatik olarak bir sevkiyat ve yükleme arasında akar. Bu davranış, sevkiyatı otomatik güncelleştirme işlevi sunulmadan önce kullanılan davranışa benzer.

## <a name="main-elements-of-the-functionality"></a>İşlevlerin ana öğeleri

Sevkiyatı otomatik güncelleştirme işlevi öncelikle sevkiyat durumuna bağlıdır ve bir satış siparişi satırında veya transfer emri satırında değişiklik yapıldığında bir yükleme satırındaki miktarın değiştirilip değiştirilemeyeceğini belirler. Ayrıca, var olan bir yükleme satırına otomatik olarak yeni bir yükleme satırı eklenmesi gerekip gerekmediğini belirlemek için sevkiyat durumunu temel alır. Sevkiyat durumu **Dalga oluşturuldu** veya daha yüksek bir durum olduğunda, otomatik güncelleştirme gerçekleşmez.

Dalga durumu da otomatik güncelleştirmeler için dikkate alınır. Yükleme satırıyla ilişkili olan dalga durumu **Tutuldu**, **Yürütülüyor**, **Serbest bırakıldı**, **Çekildi** veya **Sevkedildi** olarak ayarlandığında (satış siparişi satırında veya transfer emri satırında miktar azalmasına göre), bir kullanıcı yükleme satırındaki miktarı azaltmaya çalışırsa, aşağıdaki hata iletisi görüntülenir: "Rezervasyonlar, rezervasyonlara dayanan oluşturulmuş bir iş bulunduğundan kaldırılamadı." Ek olarak, dalga daha önce sözü edilen dalga durumlarının birine sahip olduğunda, bir kullanıcı satış siparişi satırı veya transfer emri satırındaki miktarı artırarak yükleme satırı miktarını dolaylı olarak artırmayı denerse, yükleme satırındaki miktar otomatik olarak artırılmaz. Bu durumda, yük satırının el ile güncelleştirilmesi gerekir.

## <a name="scenarios"></a>Senaryolar

Sevkiyatı otomatik güncelleştirme işlevi dört senaryoyu destekler: yeni sipariş satırı ekleme, sipariş satırındaki miktarı artırma, sipariş satırındaki miktarı azaltma ve sipariş satırını kaldırma.

- **Yeni sipariş satırı ekle**: **Ambar** sayfasındaki (**Ambar yönetimi \> Kurulum \> Ambar \> Ambarlar**) **Ambar** hızlı sekmesinde bulunan **Sevkiyatı otomatik güncelleştir** alanı **Her zaman** olarak ayarlandığında, sipariş için bir sevkiyat varsa ve satış siparişi oluşturulduktan sonra satış siparişi veya transfer emrine yeni bir sipariş satırı eklenirse, var olan yük güncelleştirilmez. Var olan yüke referans içermeyen yeni bir yük satırı oluşturulur ve var olan sevkiyatla ilişkilendirilir. Yeni satır yüke eklenir ve serbest bırakılır.
- **Bir sipariş satırındaki miktarı artır**: **Sevkiyatı otomatik güncelleştir** alanı **Her zaman** olarak ayarlandığında, sipariş için bir sevkiyat varsa ve var olan satış siparişi satırı veya transfer emri satırındaki miktar, satış siparişi için bir yük oluşturulduktan sonra artırılırsa, yük satırı sipariş satırı ile aynı miktar kadar artar. Yük serbest bırakılmışsa ancak bir iş oluşturulmamışsa, yük satırı sipariş satırı ile aynı miktar kadar artar.
- **Bir sipariş satırıda miktarı azalt**: **Sevkiyatı otomatik güncelleştir** alanı **Her zaman** veya **Miktar azaltıldığında** olarak ayarlandığında sipariş için bir sevkiyat varsa ve var olan satış siparişi satırında veya transfer emri satırındaki miktar satış siparişi için bir yük oluşturulduktan sonra azaltılmışsa, bu yük satırındaki miktar zaten sipariş satırındaki miktara eşit veya bu miktardan daha az olmadığı sürece, ilişkili yük satırındaki miktar eşleşecek şekilde güncelleştirilir. Bu durumda, yük satırı etkilenmez. Yük serbest bırakılmışsa ancak bir iş oluşturulmamışsa, yük satırındaki miktar sipariş satırındaki yeni miktara eşit veya bundan az olmadıkça, ilişkili yükleme satırındaki miktar eşleşecek şekilde güncelleştirilir. Bu durumda, yük satırı etkilenir.
- **Bir sipariş satırını kaldır**: **Sevkiyatı otomatik güncelleştir** alanı **Her zaman** veya **Miktar azaltıldığında** olarak ayarlandığında, kullanıcı bir yük satırının mevcut olduğu bir sipariş satırını kaldırmaya çalışırsa bir hata iletisi gösterilir.

## <a name="example-scenario"></a>Örnek senaryo

Bu senaryo için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Sevkiyatı otomatik güncelleştir işlevini açma

Sevkiyatı otomatik güncelleştir işlevini açmak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar**'a gidin.
2. Ambar **24**'ü seçin.
3. **Ambar** hızlı sekmesinde, **Sevkiyatı otomatik güncelleştir** alanında, değeri **Miktar azaldığında** yerine **Her zaman** olarak değiştirin.

Değeri **Her zaman** olarak değiştirdikten sonra, satış siparişi satırları ve transfer emri satırlarındaki miktarlardaki herhangi bir artış veya düşüş ve yeni satır eklemeleri, daha önce açıklanan güncelleştirme kısıtlamalarına uygun şekilde seçilen ambara ait tüm sevkiyatlara ve yüklere yansıtılır.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Dalga şablonunu, yük satırlarının otomatik olarak işlenmemesi için değiştirme

Dalga şablonunu otomatik olarak yükleme satırlarını işlemeyecek şekilde yapılandırmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
2. **24 Sevkiyat varsayılanı** dalga şablonunu seçin.
3. **Düzenle** öğesini seçin.
4. **Genel** hızlı sekmesinde **Dalga oluşturmayı otomatikleştir** seçeneğini **Evet** olarak ayarlayın ve diğer tüm seçeneklerin **Hayır** olarak ayarlandığından emin olun.

Dalga oluşturma işleminin bir parçası olarak hiçbir işin otomatik olarak oluşturulup serbest bırakılmaması önemlidir. Satış siparişi satırı için oluşturulan yükleme satırıyla ilişkili iş oluşturulduktan sonra, satış siparişi satırındaki miktar değiştirilirse yük satırı artık otomatik olarak güncelleştirilmez.

### <a name="create-a-sales-order"></a>Satış siparişi oluştur

Bir satış siparişi oluşturmak için şu adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
2. **US-003** müşterisini seçin.
3. **A0001** madde numarası için bir satır oluşturun.
4. Miktarı **10** olarak girin. (Ambar **24**'ü kullandığınızdan emin olun.)
5. **Kaydet**'i seçin.
6. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin. Bir sevkiyat ve bir dalga oluşturulur.

Önceki yordamda dalga şablonunu değiştirdiğiniz için, yük veya iş oluşturulmaz. Sevkiyat durumu **Açık**, dalga durumu **Oluşturuldu**'dur.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Satış siparişi satırındaki miktarı azaltma

Bir satış siparişi satırındaki miktarı azaltmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
2. Ambara henüz serbest bıraktığınız satış siparişini seçin.
3. Satış siparişi satırını seçin. **Miktar** alanında, değeri **10**'dan **8**'e değiştirin.
4. Satış siparişi satırında **Ambar \>Sevkiyat ayrıntıları**'nı seçin. **Sevkiyat ayrıntıları** sayfasında, **Yük satırları** hızlı sekmesindeki miktar satış siparişi satırındaki değişikliği yansıtır.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Satış siparişi satırındaki miktarı artırma

Bir satış siparişi satırındaki miktarı artırmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
2. Ambara daha önce serbest bıraktığınız satış siparişini seçin.
3. Satır miktarını **8** yerine **12** olarak değiştirin.
4. **Kaydet**'i seçin.
5. **Tüm satış siparişleri** sayfasına geri dönün ve satış siparişini yeniden seçin.
5. Eylem Bölmesinde **Ambar** sekmesindeki **İlgili bilgiler** grubunda **Sevkiyat ayrıntıları**'nı seçin. **Sevkiyat ayrıntıları** sayfasında, **Yük satırları** hızlı sekmesindeki miktar satış siparişi satırındaki değişikliği yansıtır.

Yük satırındaki miktar 8'den 12'ye yükseltilmiş olmasına karşın, otomatik rezervasyon açılmadıkça yalnızca sekiz öğe ayrılmış kalır. Var olan sevkiyata eklenen miktar rezerve edilmediği için, dalga rezervasyon olmadan bu noktada işlenirse, iş yalnızca önceden rezerve edilmiş olan miktar için oluşturulur.

> [!NOTE]
> Bir sipariş satırındaki miktar azaltıldığında, sipariş satırındaki yeni miktar zaten eşit veya bundan küçükse yükleme satırındaki miktar etkilenmez. Bir sipariş satırındaki miktar artırıldığında, yükleme satırı sipariş satırı ile aynı miktar kadar artar. Sipariş satırındaki miktar yük satırındaki miktardan farklıysa, farklılık kalır.

### <a name="add-a-sales-order-line"></a>Bir satış siparişi satırı ekleme

Bir satış siparişi satırı eklemek için şu adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
2. Ambara daha önce serbest bıraktığınız satış siparişini seçin.
3. **A0002** madde numarası için bir satır oluşturun.
4. **Miktar** alanına **10** yazın. (Ambar **24**'ü kullandığınızdan emin olun.) Yeni satır var olan sevkiyata otomatik olarak eklenir.
5. **Kaydet**'i seçin.
6. **Tüm satış siparişleri** sayfasına geri dönün ve satış siparişini yeniden seçin.
7. Eylem Bölmesinde **Ambar** sekmesindeki **İlgili bilgiler** grubunda **Sevkiyat ayrıntıları**'nı seçin. **Sevkiyat ayrıntıları** sayfasında, **Yük satırları** hızlı sekmesinde, ikinci yük satırına dikkat edin.

Var olan sevkiyata eklediğiniz satış siparişi satırı rezerve edilmediği için dalga bu noktada işlendiyse, iş yalnızca ilk satış siparişi satırı ve ilk yükleme satırındaki miktar için oluşturulur.

### <a name="process-a-wave"></a>Dalga işleme

Dalgayı işlemek için şu adımları izleyin.

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
2. Daha önce oluşturduğunuz dalgayı seçin.
3. Eylem Bölmesinde, **Dalga** sekmesindeki **Dalga** gurubunda **İşle**'yi seçin.

Dalga işlenir ve yük satırlarındaki rezerve edilen miktarlar için iş oluşturulur. Sevkiyat durumu **Açık** yerine **Dalga oluşturuldu** olarak güncelleştirilir. Sevkiyat durumu **Dalga oluşturuldu** olarak güncelleştirildiğinden, satır miktarlarındaki düşüşler veya artışlar gibi tüm değişiklikler veya satış siparişine yeni satırların eklenmesi, dalga oluşturulan siparişle ilişkili mevcut yük satırlarını etkilemez.

Bir sevkiyatın durumu **Dalga oluşturuldu** veya daha yüksek bir durum olduğunda, bir satış siparişi satırındaki miktara ilişkin güncelleştirmeler, sevkiyatla ilişkilendirilmiş bir yükleme satırına yansıtılmaz veya bu satıra göre doğrulanmaz. Bir yük satırındaki miktar üzerinde yapılan değişiklikler doğrudan yük satırında yapılmalıdır.

Doğrulama, yük satırı için iş oluşturulduktan ve rezervasyon yapıldıktan sonra gerçekleştirilir. Satış siparişi satırının miktarındaki azalma iş satırı rezervasyonuna göre doğrulanır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]