--- 
title: "Tedarik kategorisi hiyerarşisini ayarlama"
description: "Bu yordam, tedarik kategori hiyerarşisi içinde yeni düğümler oluşturmayı ve satın alma işleminde kullanılacak bir tedarik kategorisi yapılandırmayı gösterir."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
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
ms.sourcegitcommit: 6ad5c8552a6989e9093d0b1325754bc0f6d19372
ms.openlocfilehash: 4541d029c9c3be3ee42332e5d8ff183dd503f13e
ms.contentlocale: tr-tr
ms.lasthandoff: 11/06/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Tedarik kategorisi hiyerarşisini ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, tedarik kategori hiyerarşisi içinde yeni düğümler oluşturmayı ve satın alma işleminde kullanılacak bir tedarik kategorisi yapılandırmayı gösterir. Bu görevler genellikle Satınalma yöneticisi tarafından yerine getirilir. Bu yordama başlamadan önce tedarik türünde bir kategori hiyerarşisi mevcut olmalıdır. Eğer bir demo verisi şirketi kullanıyorsanız, bu prosedürü USMF şirketinde çalıştırabilirsiniz.


## <a name="add-a-new-procurement-category"></a>Yeni bir tedarik kategorisi ekleyin
1. Tedarik ve kaynak > Tedarik kategorileri'ne gidin.
2. Kategori hiyerarşisi düzenle'ye tıklayın.
    * Geçerli tedarik kategori hiyerarşisi sayfanın sol tarafında görüntülenir. Hiyerarşide değişiklik yapmak üzeresiniz.  
3. Yeni kategori düğümü'ne tıklayın.
    * Sistem varsayılan olarak üst düğümü seçer. Bu yordamı bir görev kılavuzu olarak çalıştırıyorsanız, Kilidi Aç düğmesine tıklayıp, yeni düğümü içine eklemek için başka bir üst düğümü seçin. Bunu yaptıktan sonra, görev kılavuzunu kilitleyin ve sonrasında Yeni kategori düğümü'nü tıklatın.  
4. İsim alanına bir değer yazın.
5. Açıklama alanına bir değer girin.
6. Kolay ad alanına bir değer girin.
    * Kolay ad isteğe bağlıdır. Bu kategori aramalarında, kategori adı ile birlikte görüntülenir.  
7. Kaydet'e tıklayın.

## <a name="add-products-to-your-new-procurement-category"></a>Yeni tedarik kategorinize ürünler ekleyin
1. Tedarik ve kaynak > Tedarik kategorileri'ne gidin.
    * Yeni eklediğiniz düğümü seçin. Bu yordamı bir görev kılavuz olarak çalıştırıyorsanız, düğümü seçmek için görev kılavuzunun kilidini açmanız gerekebilir.  
2. Ürünler bölümünün genişletilmiş görünümüne geçin.
3. Tedarik kategorisiyle ürün ilişkilendirmek için Ekle'yi tıklatın.
4. Tedarik kategorisine eklemek istediğiniz ürünü seçin.
5. Ürünü seçmek için oku tıklatın.
6. Tedarik kategorisine eklemek istediğiniz başka bir ürünü seçin.
7. Ürünü seçmek için oku tıklatın.
8. Tamam'a tıklayın.

## <a name="add-approved-and-preferred-vendors"></a>Tercih edilen ve onaylanan satıcılar ekleyin
1. Satıcılar bölümünün genişletilmiş görünümüne geçin.
2. Ekle öğesini tıklatın.
    * Bir satıcıyı bir tedarik kategorisine ekleyebilir ve satıcının kategori için tercih edilen mi yoksa sadece onaylanan mı olduğunu belirtebilirsiniz. Bir kategoriden bir satıcıyı sildiğinizde, satıcıyla ait bu kategorideki geçmiş hareketler silinmez.   
3. Tedarik kategorisine eklemek istediğiniz satıcıyı bulun.
4. Satıcıyı seçmek için oku tıklatın.
5. Tamam'ı tıklatın.
6. Değiştirmek istediğiniz satıcı satırını seçin.
7. Satıcı durumu alanında, bir seçenek seçin.
    * Kategori ilke kuralındaki tedarikçi seçimi ayarı, tercih edilen mi, onaylanmış olan mı, yoksa tüm satıcıların mı satınalma talepleri üzerinde kullanılabilir olduğunu yönetir.   

## <a name="add-additional-information-to-the-category"></a>Kategoriye ilave bilgiler ekleyin
1. Tedarikçi değerlendirme ölçüt grupları bölümünün genişlemesini değiştir.
    * Bu sekme, tedarik kategorisindeki satıcıların hangi ölçütlere göre değerlendirileceğini tanımlamanıza olanak sağlar. Bunu yapmak için Ekle'yi tıklayıp sonra istediğiniz ölçütü içeren bir tedarikçi Değerlendirme grubu seçin.  
2. Soru formları bölümünün genişlemesini değiştir.
    * Bu sekme, faaliyet türünü "Talep" olarak seçtiğiniz sürece, taleplerde yer alacak bir soru formu eklemenizi sağlar. Buna göre, talepte bulunan kişinin, belirli bir ürün veya tedarik kategorisindeki ürünler için talep göndermeden önce bir soru formu doldurması gerekir.  
3. Madde satış vergisi grupları bölümünün genişlemesini değiştir.
4. Madde Satış vergisi grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Satış vergisi grubu seçin.
6. Kategori sayfası bölümünün genişlemesini değiştir.
    * Kategori sayfaları kategori hiyerarşisi sayfasında oluşturulur. Bunlar tedarik kategorisi hakkında, örneğin bir kategorideki ürünlerin türü, kategorideki ürünlerin fotoğrafları, kategoride bulunan indirimler gibi duyuruların bilgilerini içerir. Kategori sayfasındaki bilgiler, satınalma talepleri üzerinde görüntülenir.  
7. Sayfayı kapatın.


