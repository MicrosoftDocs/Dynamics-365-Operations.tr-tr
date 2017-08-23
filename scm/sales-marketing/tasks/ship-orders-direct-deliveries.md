--- 
title: "Siparişleri doğrudan teslim olarak sevk etme"
description: "Bu yordam, satış siparişi için bir doğrudan teslimat oluşturmayı göstermektedir."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d98e288a157183fbf4d7c032d86bb4a65166e297
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Siparişleri doğrudan teslim olarak sevk etme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, satış siparişi için bir doğrudan teslimat oluşturmayı göstermektedir. Malları ilk önce ambarınız yerine doğrudan satıcınızdan müşteriye sevk etmek istediğinizde doğrudan teslimat seçeneğini kullanırsınız. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. "Doğrudan teslimatları çalışma alanından oluştur" ikincil alt görevini başarıyla tamamlamak için, satış siparişinde seçtiğiniz ürün için Serbest bırakılan ana ürünlerin Satınalma FastTab'inde belirtilmiş varsayılan bir Satıcı olduğundan emin olun.


## <a name="set-an-individual-order-for-direct-delivery"></a>Doğrudan teslimat için tek bir sipariş ayarlama
1. Tüm satış siparişleri'ne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer girin veya seçin.
    * USMF kullanıyorsanız, hesap US-001'yi seçebilirsiniz.  
4. Tamam'a tıklayın.
5. Madde numarası alanında bir değer girin veya seçin.
    * USMF kullanıyorsanız, T0020 öğesini seçebilirsiniz.  
6. Kaydet'e tıklayın.
7. Eylem Bölmesinde, Satış siparişi öğesine tıklayın.
8. Doğrudan teslimat öğesine tıklayın.
    * Teslimat oluştur sayfası, tüm açık satış siparişi satırlarını satış siparişinden kopyalayarak listeler. Sipariş ayrıntılarını gözden geçirebilir ve gerekiyorsa doğrudan teslimat oluşturmadan önce satınalma miktarı ve fiyatlandırma koşulları gibi ayrıntıları değiştirebilirsiniz.  
9. Tümünü dahil et alanında Evet seçeneğini belirleyin.
    * Satış siparişi satırlarının yalnızca bir alt kümesi için bir doğrudan teslimat oluşturmak istiyorsanız, bunları tek tek seçin.  
    * Satıcı hesabı alanı bir satıcı numarası ile önceden doldurulmuş olabilir. Varsayılan satıcı ürün için (ilişkili ürün kapsamında) ayarlanmışsa, bu satıcı satıra kopyalanır. Aksi takdirde, manüel olarak bir satıcı girmeniz gerekir. Bu örnekte, bir tanesi önceden doldurulmuş olsa bile, sonraki adımda yeni bir satıcı seçilmektedir.   
10. Satıcı hesabı alanında bir değer girin veya bir değer seçin.
    * USMF kullanıyorsanız, hesap 1001'i seçebilirsiniz.  
11. Tamam'a tıklayın.
    * İleti, satınalma siparişinin oluşturulduğunu bildirir.   
12. Satır ayrıntıları bölümünü genişletin.
13. Teslimat sekmesine tıklayın.
    * Doğrudan teslimat alanı artık Evet olarak ayarlanır.  
    * Doğrudan teslimat durumu oluşturulan Satınalma siparişini gösterir.   
14. Eylem Bölmesinde, Genel öğesine tıklayın.
15. İlgili siparişleri tıklatın.
16. Satınalma siparişi alanındaki bağlantıyı izlemek için tıklayın.
17. Satır ayrıntıları bölümünü genişletin.
18. Adres sekmesini tıklatın.
    * Bu satınalma siparişi satırındaki teslimat adresinin şirketinizin adresi değil müşterinin teslimat adresi olduğunu unutmayın.  
    * Satınalma siparişi satırında ya da kaynak satış siparişi satırında teslimat adresini değiştirirseniz, ilgili sipariş satırı otomatik olarak güncelleştirilir.  
19. Teslimat sekmesine tıklayın.
    * Tıpkı satış siparişi satırı gibi ilgili satınalma siparişi satırı türü de Doğrudan teslimat olarak ayarlanır.  
    * Satınalma siparişi satırının Teslimat tarihi ve Onaylı teslimat tarihi, sırasıyla satış siparişi satırındaki Talep edilen giriş tarihi ve Onaylı giriş tarihi şeklinde ayarlanır.   
    * Satınalma satırında ya da satış satırında bu tarihlerin birini güncelleştirirseniz, ilgili siparişin tarihleri otomatik olarak güncelleştirilir.     
    * Malların doğrudan müşteriye teslimatı şeklinde ayarlanan satınalma siparişi özel bir ilişki üzerinden kaynak satış siparişine bağlanır. Bu ilişkilendirme, satış siparişinin sevk irsaliyesi güncelleştirmesinin kendiliğinden satış siparişinden yapılamayacağı ve satınalma siparişi kullanılarak yapılması gerektiği kuralını zorunlu kılar. Ancak, müşteri faturalandırması satış siparişinden gerçekleştirilmelidir.  
20. Eylem Bölmesinde, Satınalma öğesine tıklayın.
21. Onay'a tıklayın
22. Tamam'a tıklayın.
23. Eylem Bölmesinde, Al öğesine tıklayın.
24. Ürün girişi seçeneğine tıklayın.
25. Ürün girişi alanına bir değer girin.
26. Tamam'a tıklayın.
27. Eylem Bölmesinde, Genel öğesine tıklayın.
28. İlgili siparişleri tıklatın.
29. Listede, seçili satırı işaretleyin.
    * Satınalma siparişi 'alındı' olarak güncelleştirildikten veya başka bir deyişle satıcı malları müşterinin adresine sevk ettikten sonra, kaynak satış siparişinin durumu otomatik olarak Teslim edildi olarak güncelleştirilir.  
    * Satış siparişi artık faturalandırılabilir.    
30. Tamam'a tıklayın.
31. Sayfayı kapatın.
32. Tamam'a tıklayın.

## <a name="create-direct-deliveries-from-the-workbench"></a>Çalışma alanından doğrudan teslimatlar oluşturma
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Tüm satış siparişleri'ne gidin.
4. Yeni'ye tıklayın.
5. Müşteri hesabı alanında bir değer girin veya seçin.
6. Tamam'ı tıklatın.
7. Madde numarası alanında bir değer girin veya seçin.
8. Satır ayrıntıları bölümünü genişletin.
9. Teslimat sekmesine tıklayın.
    * Önceki yordamda olduğu gibi bir doğrudan teslimatı satış siparişi işleminin parçası olarak oluşturmak yerine, bu görevi bir satınalma uzmanına bırakmayı seçebilirsiniz. Satış siparişi satırını doğrudan teslimat işleme işlemine dahil etmek için doğrudan teslimatın satırını işaretlemeniz gerekir.  
10. Doğrudan teslimat alanında Evet'i seçin.
    *   Ürün zaten varsayılan olarak doğrudan teslimat için ayarlanmışsa, alan sipariş satırı girişinde otomatik olarak Evet olarak ayarlanacaktır. Doğrudan teslimat seçeneğini Evet olarak ayarlayarak ve varsayılan bir Doğrudan teslimat ambarı seçerek Serbest bırakılan ana üründe doğrudan teslimat için bir ürün ayarlayabilirsiniz.  
    * Satınalma siparişi henüz oluşturulmadığından, Doğrudan teslimat durumu Doğrudan teslim edilecek şekilde ayarlanır.   
11. Sayfayı kapatın.
12. Sayfayı kapatın.
13. Doğrudan teslimat'a gidin.
    * Doğrudan teslimat sayfası, satınalma aracısına doğrudan teslim edilecek tüm satış siparişi satırlarına yönelik genel bakış sağlayan bir çalışma ekranı olarak iş görür ve bunlara ilgili satınalma siparişlerini oluşturulma imkanı sağlar. Ayrıca, bunlar Onay ve Teslimat sekmelerinde açık doğrudan teslimat siparişlerini ve doğrulanan siparişleri görüntüleyebilir.   
14. Doğrudan teslimat oluştur'u tıklatın.
15. Onay sekmesini tıklatın.
    * Doğrudan teslimat siparişi oluşturduktan sonra bu sipariş otomatik olarak Onay sekmesine taşınır. Bu sayfada doğrudan siparişi onaylamayı seçebilirsiniz. Satınalma onaylandığında, girişini kaydettirdiğiniz Teslimat sekmesine otomatik olarak taşınır.  


