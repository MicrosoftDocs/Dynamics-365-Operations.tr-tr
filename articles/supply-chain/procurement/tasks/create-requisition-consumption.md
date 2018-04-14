--- 
title: "Tüketim talebi oluşturma"
description: "Bu yordam, bir talep oluşturma işleminde size yol gösterir."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7d8ca4e7eedea140f32e264c205b243027a06d03
ms.openlocfilehash: d1ea95d0bc283297fcedaee730e1829850f07998
ms.contentlocale: tr-tr
ms.lasthandoff: 11/20/2017

---
# <a name="create-a-requisition-for-consumption"></a>Tüketim talebi oluşturma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir talep oluşturma işleminde size yol gösterir. Ürün tedarik kataloğunuzda bulunan ürünleri arama ve kataloğunuzda bulunmayanları nasıl ekleyeceğiniz hakkında farklı yolları gösterir. Bu yordama başlamadan önce Tüketim'in varsayılan talep türü olarak ayarlanmış olduğu bir satın alma ilkeniz olmalıdır. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz. Yordam, yalnızca çalışan olarak ayarlanmış bir kullanıcı profili tarafından kullanılabilir.  Bu görev normalde bir personel tarafından yerine getirilir. Personel işe alma güvenlik rolü, görevleri gerçekleştirmenize izin verir veya USMF kullanıyorsanız, Sibel olarak oturum açabilirsiniz.


## <a name="create-a-new-requisition"></a>Yeni bir talep oluştur
1. Tedarik ve kaynak Hizmeti'nden > Satınalma talepleri > Satınalma talepleri benim tarafından hazırlandı'ya git.
2. Yeni'ye tıklayın.
3. İsim alanında, talebe bir ad verin.
4. Talep edilen tarih alanında, bir tarih girin.
    * Varsayılan olarak, istenen tarih ve hesap oluşturma tarihi satınalma talebi satırlarına kopyalanır. Satır düzeyinde değiştirilebilirler. Talep tarihi, talep edilen teslimat tarihidir.  
5. Muhasebe tarihi alanında bir tarih girin.
    * Muhasebe tarihi, muhasebe girişini genel deftere kaydetmek için ve bütçe fonlarının mevcut olup olmadığını doğrulamak için kullanılan tarihtir.  
6. Tamam'a tıklayın.
7. Sebep alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Varsayılan olarak, seçtiğiniz işletme gerekçesi sebebi, satınalma talebi satırında belirecektir fakat bunu satır seviyesinde değiştirebilirsiniz.    
8. Listede, istenen kaydı bulun ve seçin.
9. Sebebi seçin
10. Detaylar alanında talep için daha açıklayıcı bir gerekçe girin.

## <a name="add-a-line-to-the-requisition"></a>Talebe bir satır ekle
1. Satır ekle'ye tıklayın.
    * Satınalma talebine satırlar eklemenin iki yolu vardır. Ürün numarasını zaten biliyorsanız ya da ürün kataloğunda olmayan bir ürün talep edeceğinizi zaten biliyorsanız, "Satır Ekle" ile doğrudan satırı ekleyebilirsiniz. Diğer bir yol ürün kataloğunda maddeleri bulmak için arama ve filtreleme kullanabileceğiniz "Ürün Ekle" seçeneğini kullanmaktır.    
2. Yeni oluşturduğunuz satıra tıklatın.
    * Talepte bulunan, talebi isteyen çalışandır.   
    * Talebi hazırlayan kişi varsayılan olarak talep eden kişidir. Başka bir çalışan adına bir talep satırı hazırlamanız için izin verilmiş olması gerekir. Bu tür izinleriniz varsa diğer çalışanlar bu aramada gösterilecektir.  
3. Madde numarası alanına bir değer girin.
    * Seçmeniz için kullanılabilir olan öğeler, kategori erişim ilkesi ve tüzel kişilik için satın alma tedarik katalog ile sınırlıdır.   
4. Miktar alanına bir sayı girin.

## <a name="add-more-products-to-the-requisition"></a>Talebe daha fazla ürün ekle
1. Ürünler ekle'ye tıklayın.
    * Bu, ürün kataloğu içinde ürünler arayabileceğiniz bir seçenektir.    
2. Tedarik kataloğu düğümü bul alanında, aradığınız kategorinin adının ilk bölümünü yazın ve Enter tuşuna basın.
    * Örneğin, comput yazın.  
3. InvokeDefaultButton kısayolunu kullanın.
4. Seçilen kategorideki ürünler listesine filtre uygulamak için Filtre'yi kullanın.
5. Talebe eklemek istediğiniz ürün kartını seçin.
6. Satırlara ekle'yi tıklatın.
7. Miktar alanına bir sayı girin.
8. Tedarik kataloğu düğümü bul alanında, aradığınız kategorinin adının ilk bölümünü yazın ve Enter tuşuna basın.
    * Örneğin, yüksek (vurgulayıcılar) yazın.  
9. InvokeDefaultButton kısayolunu kullanın.
10. Tedarik Kataloğu'nda listelenmemiş bir ürün eklemek Listelenmemiş ürünü satırlara ekle'yi tıklatın.
11. Ürün adı alanına bir değer girin.
12. Birim alanına bir değer yazın.
13. Tamam'ı tıklatın.
14. Madde açıklaması alanına madde için bir açıklama yazın.
15. Miktar alanına bir sayı girin.
16. Birim fiyatı alanına bir sayı girin.
    * (Seçtiğiniz satıcı hesabı alanına) belirli bir satıcı için fiyatı biliyorsanız, bu fiyatı girebilirsiniz   
17. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Bu alanda seçilebilecek satıcılar, satınalma ilkelerine ve satıcının geçerli tedarik kategorisinin durumuna bağlıdır. Burada bir satıcı seçmeye alternatif olarak, Satıcı Öner düğmesini tıklatabilirsiniz.    
18. Listede kullanmak istediğiniz satıcıyı seçin.
19. Harici madde numarası alanına bir değer girin.
    * Bu, satıcı tarafından bilinen bir ürün için referans numarasıdır. Örneğin, bu satıcının kendi kataloğundaki ürünün madde numarası olabilir.  
20. Tamam'a tıklayın.

## <a name="distribute-amounts"></a>Tutarları dağıt
1. Finansal öğeler'e tıklayın.
2. Dağıtım tutarlarını'nı tıklatın.
    * Bu işlem ilk satır maliyetini 2 hesapları arasında dağıtmayı gösterir. Bu daha sonra, talep incelemede olduğunda da yapılabilir.  
3. Yeni bir dağıtım satırı oluşturmak için Böl'e tıklatın.
4. Genel muhasebe hesabı alanında maliyetin bir kısmını üstlenecek ilk maliyet merkezini seçin.
5. Diğer dağıtım satırını seç.
6. Genel muhasebe hesabı alanında diğer maliyet merkezi belirtin.
7. Eşit olarak dağıt'ı tıkaltın.
8. Sayfayı kapatın.

## <a name="view-line-details"></a>Satır ayrıntılarını görüntüle
1. Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.

## <a name="submit-the-requisition"></a>Talebi gönder
1. İletişim kutusu formunu açmak için İş akışı'na tıklayın.
2. Gönder'i tıklatın.
3. Sayfayı kapatın.
4. Yorum alanına, talebin onaylayıcısı için bir not yazın.
5. Gönder'i tıklatın.
6. Sayfayı kapatın.
7. Sayfayı yenileyin.


