---
title: Siparişleri doğrudan teslim olarak sevk etme
description: Bu konu, satış siparişi için bir doğrudan teslimat oluşturmayı göstermektedir.
author: omulvad
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eacd80f8f8b9b4a4c2a1e5e5b0da7f0c46e82166d1d02d15ce26dd641f7127f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781381"
---
# <a name="ship-orders-as-direct-deliveries"></a>Siparişleri doğrudan teslim olarak sevk etme

[!include [banner](../../includes/banner.md)]

Bu konu, satış siparişi için bir doğrudan teslimat oluşturmayı göstermektedir. Malları ilk önce ambarınız yerine doğrudan satıcınızdan müşteriye sevk etmek istediğinizde doğrudan teslimat seçeneğini kullanırsınız. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. "Doğrudan teslimatları çalışma alanından oluştur" ikincil alt görevini başarıyla tamamlamak için, satış siparişinde seçtiğiniz ürün için Serbest bırakılan ana ürünlerin Satınalma FastTab'inde belirtilmiş varsayılan bir Satıcı olduğundan emin olun.

## <a name="set-an-individual-order-for-direct-delivery"></a>Doğrudan teslimat için tek bir sipariş ayarlama
1. **Gezinti bölmesi > Modüller > Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Müşteri hesabı** alanında bir değer girin veya seçin, ardından **Tamam**'ı seçin.
4. **Madde numarası** ve **Tesis** alanlarına değerleri girin veya seçin ve sonra **Kaydet**'i seçin.
5. Eylem Panosunda **Satış siparişi**'ni, ardından **Doğrudan teslimat**'ı seçin. Teslimat oluştur sayfası, tüm açık satış siparişi satırlarını satış siparişinden kopyalayarak listeler. Sipariş ayrıntılarını gözden geçirebilir ve gerekiyorsa doğrudan teslimat oluşturmadan önce satınalma miktarı ve fiyatlandırma koşulları gibi ayrıntıları değiştirebilirsiniz.  
6. **Tümünü dahil et** alanında **Evet** seçeneğini seçin.
    - Satış siparişi satırlarının yalnızca bir alt kümesi için bir doğrudan teslimat oluşturmak istiyorsanız, bunları tek tek seçin.  
    - **Satıcı hesabı** alanı bir satıcı numarası ile önceden doldurulmuş veya halihazırda doldurulmamış olabilir. Varsayılan satıcı ürün için (ilişkili ürün kapsamında) ayarlanmışsa, bu satıcı satıra kopyalanır. Aksi takdirde, manüel olarak bir satıcı girmeniz gerekir. Bu örnekte, bir tanesi önceden doldurulmuş olsa bile, sonraki adımda yeni bir satıcı seçilmektedir.   
7. **Satıcı hesabı** alanında bir değer girin veya seçin, ardından **Tamam**'ı seçin. İleti, satınalma siparişinin oluşturulduğunu bildirir.   
8. **Satır ayrıntıları** bölümünü genişletin.
9. **Teslimat** sekmesini seçin ve **Doğrudan teslim** alanının **Evet** olarak ayarlandığını doğrulayın.
10. Eylem Bölmesinde, **Genel**'i seçin.
11. **İlgili siparişleri** seçin.
12. **Satınalma siparişi** alanındaki bağlantıyı izlemek için tıklayın.
13. **Satır ayrıntıları** bölümünü genişletin ve **Adres** sekmesini seçin.
    - Bu satınalma siparişi satırındaki teslimat adresi şirketinizin adresi değil, müşterinin teslimat adresidir.  
    - Satınalma siparişi satırında ya da kaynak satış siparişi satırında teslimat adresini değiştirirseniz, ilgili sipariş satırı otomatik olarak güncelleştirilir.  
14. **Teslimat** sekmesini seçin.
    - Tıpkı satış siparişi satırı gibi ilgili satınalma siparişi satırı türü de Doğrudan teslimat olarak ayarlanır.  
    - Satınalma siparişi satırının Teslimat tarihi ve Onaylı teslimat tarihi, sırasıyla satış siparişi satırındaki Talep edilen giriş tarihi ve Onaylı giriş tarihi şeklinde ayarlanır.   
    - Satınalma satırında ya da satış satırında bu tarihlerin birini güncelleştirirseniz, ilgili siparişin tarihleri otomatik olarak güncelleştirilir.     
    - Malların doğrudan müşteriye teslimatı şeklinde ayarlanan satınalma siparişi özel bir ilişki üzerinden kaynak satış siparişine bağlanır. Bu ilişkilendirme, satış siparişinin sevk irsaliyesi güncelleştirmesinin kendiliğinden satış siparişinden yapılamayacağı ve satınalma siparişi kullanılarak yapılması gerektiği kuralını zorunlu kılar. Ancak, müşteri faturalandırması satış siparişinden gerçekleştirilmelidir.  
15. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
16. **Onay**'ı seçin.
17. **Tamam**'ı seçin.
18. Eylem Bölmesinde, **Teslim alma**'yı seçin.
19. **Ürün girişi**'ni seçin.
20. **Ürün girişi** alanına bir değer girin.
21. **Tamam**'ı seçin.
22. Eylem Bölmesinde, **Genel**'i seçin.
23. **İlgili siparişler**'i seçin ve istenen kaydı vurgulayın.
    - Satınalma siparişi 'alındı' olarak güncelleştirildikten veya başka bir deyişle satıcı malları müşterinin adresine sevk ettikten sonra, kaynak satış siparişinin durumu otomatik olarak Teslim edildi olarak güncelleştirilir.  
    - Satış siparişi artık faturalandırılabilir.    
24. **Tamam**'ı seçin.
25. Sayfayı kapatın.
26. **Tamam**'ı seçin. Sayfaları kapatın ve ana sayfaya dönün.

## <a name="create-direct-deliveries-from-the-workbench"></a>Çalışma alanından doğrudan teslimatlar oluşturma
1. **Gezinti > Modüller > Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Müşteri hesabı** alanında bir değer girin veya seçin, ardından **Tamam**'ı seçin.
4. **Madde numarası** ve **Site** alanlarına bir değer girin veya bu alanda bir değer seçin.
5. **Satır ayrıntıları** bölümünü genişletin, ardından **Teslimat** sekmesini seçin. Önceki yordamda olduğu gibi bir doğrudan teslimatı satış siparişi işleminin parçası olarak oluşturmak yerine, bu görevi bir satınalma uzmanına bırakmayı seçebilirsiniz. Satış siparişi satırını doğrudan teslimat işleme işlemine dahil etmek için doğrudan teslimatın satırını işaretlemeniz gerekir.  
6. **Doğrudan teslimat** alanında **Evet** seçeneğini seçin.
    - Ürün zaten varsayılan olarak doğrudan teslimat için ayarlanmışsa, alan sipariş satırı girişinde otomatik olarak Evet olarak ayarlanacaktır. Doğrudan teslimat seçeneğini Evet olarak ayarlayarak ve varsayılan bir Doğrudan teslimat ambarı seçerek Serbest bırakılan ana üründe doğrudan teslimat için bir ürün ayarlayabilirsiniz.  
    - Satınalma siparişi henüz oluşturulmadığından, Doğrudan teslimat durumu "Doğrudan teslim edilecek" şekilde ayarlanır.   
7. **Kaydet**'i seçin.
8. Ana sayfaya dönünceye kadar sayfaları kapatın.
9. Arama çubuğuna `Direct delivery` girin.
    - Doğrudan teslimat sayfası, satınalma aracısına doğrudan teslim edilecek tüm satış siparişi satırlarına yönelik genel bakış sağlayan bir çalışma ekranı olarak iş görür ve bunlara ilgili satınalma siparişlerini oluşturulma imkanı sağlar. Ayrıca, bunlar Onay ve Teslimat sekmelerinde açık doğrudan teslimat siparişlerini ve doğrulanan siparişleri görüntüleyebilir.  
    - Bir doğrudan teslimat siparişi oluşturduktan sonra, bu otomatik olarak Onay sekmesine gönderilir. Doğrudan bu sayfadan siparişi onaylamayı seçebilirsiniz. Satınalma onaylandığında, girişini kaydettirdiğiniz Teslimat sekmesine otomatik olarak taşınır.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]