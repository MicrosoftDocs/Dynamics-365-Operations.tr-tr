---
title: Tüketim talebi oluşturma
description: Bu konuda bir talep oluşturma işlemi açıklanmaktadır.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acc2cdb9b74cccaefe565b0e2ae8ec4c5f2401c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439166"
---
# <a name="create-a-requisition-for-consumption"></a>Tüketim talebi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konuda bir talep oluşturma işlemi açıklanmaktadır. Ürün tedarik kataloğunuzda bulunan ürünleri arama ve kataloğunuzda bulunmayanları nasıl ekleyeceğiniz hakkında farklı yolları gösterir. Bu yordama başlamadan önce Tüketim'in varsayılan talep türü olarak ayarlanmış olduğu bir satın alma ilkeniz olmalıdır. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz. Yordam, yalnızca çalışan olarak ayarlanmış bir kullanıcı profili tarafından kullanılabilir. Bu görev normalde bir personel tarafından yerine getirilir. **Employee** işe alma güvenlik rolü, görevleri gerçekleştirmenize izin verir veya USMF kullanıyorsanız, **Sibel** olarak oturum açabilirsiniz.


## <a name="create-a-new-requisition"></a>Yeni bir talep oluştur
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma talepleri > Tarafımdan hazırlanan satınalma talepleri** öğesine gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanında, talebe bir ad verin.
4. **Talep edilen tarih** alanına, bir tarih girin. Varsayılan olarak, istenen tarih ve hesap oluşturma tarihi satınalma talebi satırlarına kopyalanır. Satır düzeyinde değiştirilebilirler. Talep tarihi, talep edilen teslimat tarihidir.  
5. **Muhasebe tarihi** alanına bir tarih girin. Muhasebe tarihi, muhasebe girişini genel deftere kaydetmek için ve bütçe fonlarının mevcut olup olmadığını doğrulamak için kullanılan tarihtir.  
6. **Tamam**'ı seçin.
7. **Neden** alanında, açılır menüden bir seçenek belirleyin. Varsayılan olarak, seçtiğiniz işletme gerekçesi sebebi, satınalma talebi satırında belirecektir fakat bunu satır seviyesinde değiştirebilirsiniz.  
8. Nedeni seçin.
9. **Ayrıntılar** alanına talep için daha açıklayıcı bir gerekçe girin.

## <a name="add-a-line-to-the-requisition"></a>Talebe bir satır ekle
1. **Satır ekle**'yi seçin. Satınalma talebine satırlar eklemenin iki yolu vardır. Ürün numarasını zaten biliyorsanız ya da ürün kataloğunda olmayan bir ürün talep edeceğinizi zaten biliyorsanız, **Satır ekle** ile doğrudan satırı ekleyebilirsiniz. Diğer bir yol ürün kataloğunda maddeleri bulmak için arama ve filtreleme kullanabileceğiniz **Ürün ekle** seçeneğini kullanmaktır.    
2. Yeni oluşturduğunuz satırı seçin.
    - Talepte bulunan, talebi isteyen çalışandır.   
    - Talebi hazırlayan kişi varsayılan olarak talep eden kişidir. Başka bir çalışan adına bir talep satırı hazırlamanız için izin verilmiş olması gerekir. Bu tür izinleriniz varsa diğer çalışanlar bu aramada gösterilecektir.  
3. **Madde numarası** alanına bir değer girin. Seçmeniz için kullanılabilir olan öğeler, kategori erişim ilkesi ve tüzel kişilik için satın alma tedarik katalog ile sınırlıdır.   
4. **Miktar** alanına bir sayı girin.

## <a name="add-more-products-to-the-requisition"></a>Talebe daha fazla ürün ekle
1. **Ürün ekle**'yi seçin. Bu, ürün kataloğu içinde ürünler arayabileceğiniz bir seçenektir.    
2. **Tedarik kataloğu düğümü bul** alanına, aradığınız kategorinin adının ilk bölümünü girin ve **Enter** tuşuna basın. Örneğin `comput` yazın.  
3. **InvokeDefaultButton** kısayolunu kullanın.
4. Seçilen kategorideki ürünler listesine filtre uygulamak için **Filtre**'yi kullanın.
5. Talebe eklemek istediğiniz ürün kartını seçin.
6. **Satırlara ekle**'yi seçin.
7. **Miktar** alanına bir sayı girin.
8. **Tedarik kataloğu düğümü bul** alanına, aradığınız kategorinin adının ilk bölümünü yazın ve **Enter** tuşuna basın. Örneğin `High` (vurgulayıcılar) yazın.  
9. **InvokeDefaultButton** kısayolunu kullanın.
10. Tedarik kataloğunda listelenmemiş bir ürün eklemek için **Listelenmemiş ürünü satırlara ekle**'yi seçin.
11. **Ürün adı** alanına bir değer yazın.
12. **Birim** alanına bir değer yazın.
13. **Tamam**'ı seçin.
14. **Madde açıklaması** alanına madde için bir açıklama yazın.
15. **Miktar** alanına bir sayı girin.
16. **Birim fiyatı** alanına bir sayı girin. Belirli bir satıcı için (satıcı hesabı alanında seçtiğiniz) fiyatı biliyorsanız bu fiyatı girebilirsiniz.   
17. **Satıcı hesabı** alanında, açılır listeyi açarak bir seçenek belirleyin. Bu alanda seçilebilecek satıcılar, satınalma ilkelerine ve satıcının geçerli tedarik kategorisinin durumuna bağlıdır. Burada bir satıcı seçmeye alternatif olarak, **Satıcı öner**'i seçebilirsiniz.    
18. Listede kullanmak istediğiniz satıcıyı seçin.
19. **Harici madde numarası** alanına bir değer yazın. Bu, satıcı tarafından bilinen bir ürün için referans numarasıdır. Örneğin, bu satıcının kendi kataloğundaki ürünün madde numarası olabilir.  
20. **Tamam**'ı seçin.

## <a name="distribute-amounts"></a>Tutarları dağıt
1. **Finansal Öğeler**'i seçin.
2. **Dağıtım tutarları**'nı seçin. Bu işlem ilk satır maliyetini 2 hesapları arasında dağıtmayı gösterir. Bu daha sonra, talep incelemede olduğunda da yapılabilir.  
3. Yeni dağıtım satırı oluşturmak için **Böl**'ü seçin.
4. **Genel muhasebe hesabı** alanında maliyetin bir kısmını üstlenecek ilk maliyet merkezini seçin.
5. Diğer dağıtım satırını seç.
6. Genel muhasebe hesabı alanında diğer maliyet merkezi belirtin.
7. **Eşit olarak dağıt**'ı seçin.
8. Sayfayı kapatın.

## <a name="view-line-details"></a>Satır ayrıntılarını görüntüle
1. **Satır ayrıntıları** bölümünün genişletilmiş görünümüne geçin.

## <a name="submit-the-requisition"></a>Talebi gönder
1. Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.
2. **Gönder**'i seçin.
3. Sayfayı kapatın.
4. **Yorum** alanına, talebin onaylayıcısı için bir not yazın.
5. **Gönder**'i seçin.
6. Sayfayı kapatın.
7. Sayfayı yenileyin.

